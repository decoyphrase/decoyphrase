# Privacy Policy

**Decoy Phrase** is a secret-data protection application designed with an offline-first architecture. The application does not store sensitive data directly. Instead, it transforms secret data into decoy text and mapping files that can be stored separately by the user. All transformation and recovery processes are performed entirely on the user’s device without requiring an internet connection.

This approach ensures that no personal data is ever transmitted to any server or third party. Under the zero-knowledge principle, the service provider has no knowledge of the contents of your data. Only you have full control over your encryption keys and access to your data.

**For long-term storage**, users may optionally choose to store decoy text and mapping files permanently using the Arweave blockchain infrastructure. Although files are stored on a public network, all content and metadata are encrypted locally on your device before upload. This means only you can open and understand the files, as Decoy Phrase does not have access to any encryption keys. This feature is optional and designed to support data durability without compromising privacy or user autonomy.

This policy explains transparently how data is handled and affirms that no user tracking or personal data collection occurs without your consent.

## Information We Do Not Collect

Decoy Phrase does not collect, store, or track personal information. Specifically, we do **not**:

<details>

<summary><strong>Store sensitive data, including:</strong></summary>

* Seed phrases
* Private keys
* Recovery codes
* Passwords

</details>

<details>

<summary><strong>Collect personal identity information:</strong></summary>

* Name
* Email address
* Phone number
* Location
* Any other identifying data

</details>

<details>

<summary><strong>Track user activity:</strong></summary>

* Usage history
* Session duration
* Interaction patterns

</details>

<details>

<summary><strong>Use cookies or third-party trackers:</strong></summary>

* No Google Analytics
* No tracking pixels
* No fingerprinting
* No behavioral tracking mechanisms

</details>

Our architecture is intentionally designed so that we do not know who you are or what you store. We do not possess user data because we never collect it in the first place.

## Limited Information Stored Locally

Certain non-personal operational data may be stored locally on your device, such as:

* Interface preferences (dark mode, file ordering)
* File metadata cache (basic file attributes such as filename, size, and timestamps, without any file content or sensitive data, stored locally only to improve loading performance)
* Local session state (vault login status, last accessed file)

This information is never transmitted to any server and is stored only in local device storage (for example, browser localStorage). All processing and storage remain fully under your control.

## Permanent Storage (Optional Feature)

As an optional feature, Decoy Phrase provides permanent storage using the Arweave network — a blockchain specifically designed for permanent data storage.

**What is stored?**

Only the following files may be permanently stored:

* Decoy text (contains no original data)
* Mapping files that are fully encrypted on the user’s device

{% hint style="danger" %}
**Important:** Never upload seed phrases, private keys, or original data in plaintext form.
{% endhint %}

**Is it secure?**

Yes. The following protections apply:

* **End-to-end encryption:** All files are encrypted locally using AES-GCM 256-bit before upload
* **No provider access:** We do not possess, store, or have access to encryption keys
* **Zero-knowledge preserved:** Even on a public network, stored files are meaningless encrypted data without your keys
* **No user identity:** Uploads use an anonymous shared wallet system — no personal blockchain address, no private wallet, and no identity linkage

**Storage characteristics**

* **Immutable:** Files cannot be deleted or modified after upload
* **Permanent:** Files remain available indefinitely on the Arweave network
* **Non-custodial:** Only you can decrypt and access the files. We cannot assist if keys or files are lost

## Data Security

Decoy Phrase applies strict cryptographic and architectural principles to protect your data:

* All encryption and decryption processes occur locally on the user’s device
* No sensitive plaintext data ever leaves your device
* We have no system to store or recover user data

In other words, your data is not only encrypted — it is never in our possession.

## User Rights

With Decoy Phrase, you retain full control over your data. Your rights include:

* Full ownership of all files and encryption keys
* The ability to delete all files and local data at any time
* Control over file separation and password management under the two-component security model
* The option to avoid unencrypted cloud storage entirely

We cannot recover files, unlock data, or access your information — because only you have the technical ability to do so.

## Changes to This Privacy Policy

We may update this Privacy Policy from time to time. Material changes will be announced on the official website or application interface. You are responsible for reviewing updates periodically. The effective date will always be stated at the top of this policy.

## Contact

If you have any questions regarding privacy or data usage in Decoy Phrase, please contact us at:

📧 support@decoyphrase.com\
🌐 [https://decoyphrase.com](https://decoyphrase.com)

## Final Statement

Your privacy is our highest priority. By designing a system that cannot access or know your information, we ensure that only you — and no one else, including us — has control over your sensitive data.

