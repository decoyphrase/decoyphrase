# Zero Knowledge

## What zero-knowledge means in Decoy Phrase

In Decoy Phrase, **Zero Knowledge** means that the system has no technical ability to know, access, or reconstruct any digital keys (sensitive data) transformed by the decoy phrase generator, nor any file contents, file names, or user passwords stored in permanent storage.

This is not merely a privacy policy—it is a **direct consequence of the system’s architecture :**

<details>

<summary><strong>All sensitive data is processed fully offline</strong></summary>

Seed phrases and sensitive text are transformed locally within the Decoy Phrase Generator. No sensitive input is ever sent to a server or processed online.

</details>

<details>

<summary><strong>Data-Minimized Registration</strong></summary>

Decoy Phrase follows a **data-minimization principle by design**.

* The system **does not request or collect any personal or sensitive information**, such as:
  * Email addresses
  * Phone numbers
  * Government IDs
  * Real names or identity documents
* During registration, users are only required to:
  * Choose a **username**
  * Create a **password**

No additional identity verification, personal profiling, or recovery contact data is collected.

</details>

<details>

<summary><strong>Passwords are never transmitted or stored in plaintext</strong></summary>

Passwords used for permanent storage are processed locally on the user’s device.\
The application performs **hashing and key derivation entirely in the browser** to generate:

* an **Encryption Key**
* a **Wallet Key**

{% hint style="info" %}
**Technology used:**\
PBKDF2 (Password-Based Key Derivation Function 2) with high iteration counts (typically hundreds of thousands) and SHA-256, transforming user passwords into secure cryptographic keys.
{% endhint %}

</details>

<details>

<summary><strong>Client-side encryption before upload</strong></summary>

Before any file is uploaded to permanent storage, its **contents, metadata (including title), and owner identifiers** are encrypted on the user’s device using **AES-GCM 256-bit encryption**.

</details>

<details>

<summary><strong>No decryption keys are ever held by the system</strong></summary>

Decoy Phrase does not store, receive, or have access to any encryption or decryption keys in any form. All encryption, decryption, and recovery processes run entirely on the user’s device.

</details>

<details>

<summary><strong>Cookie-Free &#x26; Serverless by Design</strong></summary>

Decoy Phrase **does not use cookies at all**.\
The application is built with a **serverless, client-side architecture**, meaning there is no central server responsible for managing user sessions.

Instead, the app relies on **browser LocalStorage** for local session management, including:

* Login and wallet session state
* File metadata cache (to speed up loading without repeated blockchain requests)
* UI preferences (dark mode, file ordering, etc.)

No session data is transmitted to or synchronized with any external server.

</details>

<details>

<summary><strong>Permanent storage only receives encrypted data</strong></summary>

The permanent storage layer never sees plaintext data—only encrypted files that are meaningless without the user’s keys.

</details>

## What the system never knows

By design, Decoy Phrase never knows:

* Sensitive Data & Content
* Seed phrases, private keys, passwords, recovery codes
* User file contents
* File title/name contents
* The relationship between decoy text and mapping files
* User passwords, encryption keys, or wallet keys

All files are encrypted in the browser before upload, so permanent storage only stores ciphertext (random data).

{% hint style="info" %}
&#x20;[Learn more about the architecture and design here!](../../developer-and-open-source/project-internals/architecture-and-design.md)
{% endhint %}

## What Decoy Phrase can see

* Username / public identifier — stored as a public text string
* Total files uploaded
* Total files locked

All files are encrypted in the browser before upload, so permanent storage only stores ciphertext (random data).

{% hint style="info" %}
**Explanation:**

* Because a public blockchain (Arweave) is used, usernames are stored as public identifiers in a registry so files can be rediscovered
* Usernames are not linked to real-world identities (email, phone number, real name, etc.)
* Account registration is permissionless and does not request personal identity data
{% endhint %}
