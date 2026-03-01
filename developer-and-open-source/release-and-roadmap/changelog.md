# Changelog

All notable changes to the **DecoyPhrase** ecosystem (Web, Mobile, Core) will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

{% updates format="full" %}
{% update date="2026-02-08" %}
## \[Unreleased]

#### Added

* **Web:** Initial research on Chrome Extension manifest V3 compatibility.
* **Mobile:** Placeholder localization files for Spanish (`es`) and French (`fr`).
{% endupdate %}

{% update date="2026-02-01" %}
## \[1.0.0] - 2026-02-01

**Milestone:** Initial Public Release (MVP)

#### Added

* **Web:**
  * Full encryption/decryption suite using `crypto-js` (AES-256-GCM).
  * Integration with Upstash Redis for ephemeral session storage.
  * Responsive UI built with Tailwind CSS v4 and Framer Motion.
  * Zero-knowledge key generation logic in `lib/crypto`.
* **Mobile:**
  * Complete offline-first architecture using Flutter 3.10+.
  * Secure storage implementation via `flutter_secure_storage` (Keychain/Keystore).
  * Biometric authentication (`local_auth`) for app access.
  * Bundled wordlists in `assets/words/` for offline phrase generation.
* **Core:**
  * Arweave permaweb integration for immutable documentation.
  * Comprehensive documentation site (this repo).
  * Shared TypeScript utility library for cryptographic standards.

#### Changed

* **Repo:** Restructured project into a monorepo-style organization (`web`, `mobile`, `core`) for better maintainability.
* **CI/CD:** Enforced strict linting rules (`eslint` for web, `flutter_lints` for mobile) on all Pull Requests.

#### Fixed

* **Mobile:** Resolved padding issues on iOS devices with Dynamic Island.
* **Web:** Fixed hydration mismatch errors in Next.js App Router for dark mode toggles.

#### Security

* **Audit:** Validated that no private keys are ever transmitted to the backend server.
* **Deps:** Pinned all critical cryptographic dependencies to specific versions to prevent supply-chain attacks.
{% endupdate %}
{% endupdates %}
