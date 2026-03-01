# Auditability

In a privacy-focused ecosystem like DecoyPhrase, "Don't Trust, Verify" is our guiding principle. This document provides a roadmap for security researchers and auditors to independently verify our claims.

## Verifiable Source Code

Our critical logic is open source and separated from UI code to make auditing easier.

### Cryptographic Core

The encryption/decryption logic is isolated in the `decoyphrase` (Core) repository.

* **Location:** `lib/crypto/`
* **Key Files:**
  * `aes.ts`: Implementation of AES-256-GCM.
  * `hash.ts`: SHA-256 hashing utilities.
  * `key_derivation.ts`: PBKDF2 logic.

{% hint style="info" %}
Note: The Web and Mobile projects import or replicate this standard logic strictly. We do not use proprietary or "home-rolled" algorithms.
{% endhint %}

### Mobile Security

For the mobile app, auditors should focus on how keys are stored at rest.

* **Location:** `decoyphrase_mobile/lib/`
* **Key Dependencies:**
  * `flutter_secure_storage`: Wrapper for iOS Keychain and Android Keystore.
  * `local_auth`: Biometric authentication implementation.

***

## Build Verification

We aim for reproducible builds. You can verify that the code on GitHub matches the deployed artifact.

### Web Build

{% stepper %}
{% step %}
### Clone the repository

Clone the `decoyphrase-web` repo.
{% endstep %}

{% step %}
### Install dependencies

Use the lockfile for exact versions.

{% code title="Install dependencies" %}
```bash
npm ci
```
{% endcode %}
{% endstep %}

{% step %}
### Build the project

{% code title="Build" %}
```bash
npm run build
```
{% endcode %}
{% endstep %}

{% step %}
### Inspect build artifacts

Inspect the `.next` output directory.

Tip: Check `page` chunks for any unauthorized external script injections (e.g., analytics trackers not disclosed in docs).
{% endstep %}
{% endstepper %}

### Mobile Build

{% stepper %}
{% step %}
### Clone the repository

Clone the `decoyphrase_mobile` repo.
{% endstep %}

{% step %}
### Verify dependencies

Check the `pubspec.lock` file hash to ensure no dependencies have been tampered with.
{% endstep %}

{% step %}
### Build the release APK/IPA

{% code title="Build APK (example)" %}
```bash
flutter build apk --release
```
{% endcode %}
{% endstep %}

{% step %}
### Compare build hashes

Compare the SHA-256 hash of your local build with the official release on GitHub Releases.

Note: Hash differences may occur due to timestamps/signing keys, but the DEX code content should be functionally identical.
{% endstep %}
{% endstepper %}

***

## Dependency Auditing

We minimize external dependencies to reduce the attack surface. However, we do use standard libraries.

### Automated Checks

We encourage all users to run their own audits on our dependency tree.

**For Web/Core (NPM):**

{% code title="Audit NPM dependencies" %}
```bash
# Checks for known vulnerabilities in the dependency tree
npm audit
```
{% endcode %}

**For Mobile (Pub):** We pin versions in `pubspec.yaml` to avoid surprise updates. You can review the full tree:

{% code title="List Flutter dependencies" %}
```bash
flutter pub deps
```
{% endcode %}

### Critical Third-Party Libraries

| Library                      | Usage               | Justification                                      |
| ---------------------------- | ------------------- | -------------------------------------------------- |
| **`crypto-js`**              | Web/Core Encryption | Standard, battle-tested JS crypto library.         |
| **`flutter_secure_storage`** | Mobile Storage      | Industry standard for accessing Keychain/Keystore. |
| **`arweave`**                | Core Storage        | Required for interacting with the Permaweb.        |
