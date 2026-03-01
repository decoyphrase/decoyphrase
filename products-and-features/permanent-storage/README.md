# Permanent Storage

<figure><img src="../../.gitbook/assets/Permanent Storage Icon.png" alt="" width="375"><figcaption></figcaption></figure>

**Permanent Storage** is a component of Decoy Phrase that enables the permanent, time-resistant, and immutable storage of decoy text and mapping files, without requiring users to interact directly with the complexity of blockchain technology.

This storage layer is specifically designed for long-term text archival, covering both sensitive data that has been transformed into decoy form and non-sensitive data, while strictly preserving the zero-knowledge principle, and is powered by the Arweave blockchain.

## Purpose of Permanent Storage

Permanent Storage is designed to:

* Store data **once and forever** (uploud-once, access-forever)
* Eliminate reliance on traditional cloud services or centralized servers
* Reduce the risk of data loss caused by service shutdowns, system migrations, or forgotten accounts
* Provide a simple user experience without requiring users to understand or manage blockchain infrastructure

## Supported File Types

Decoy Phrase Permanent Storage supports **text-based files only**.

| Supported formats | Unsupported formats                   |
| ----------------- | ------------------------------------- |
| `.txt`            | Images (`.jpg`, `.png`, `.svg`, etc.) |
| `.md`             | Videos (`.mp4`, `.mov`, etc.)         |
| `.json`           | Audio (`.mp3`, `.wav`, etc.)          |
| Folder            | Binary or executable files            |

{% hint style="warning" %}
Decoy Phrase is focused on securing sensitive data such as seed phrases, passwords, private keys, and similar information, as well as long-term text archival.
{% endhint %}

## Shared Master Wallet Model

**Decoy Phrase Permanent Storage** uses a **Shared Master Wallet Model**, where a single master wallet is used to store data on the Arweave network.

#### Why use a Shared Master Wallet?

This approach is deliberately chosen because:

<details>

<summary><strong>User convenience</strong></summary>

Users do not need to:

* Create or manage a blockchain wallet
* Store additional private keys
* Interact directly with Arweave

</details>

<details>

<summary><strong>Focus on data, not blockchain</strong></summary>

Users can focus on:

* Separating decoy text and mapping files
* Managing passwords, vaults, and timelocks
* Planning long-term storage strategies

</details>

<details>

<summary><strong>Permanent Storage is free to use</strong></summary>

Using a single master wallet is more efficient and sustainable for a free permanent storage service.

</details>

#### [Zero Knowledge](../../introduction/core-principles/zero-knowledge.md) Remains Intact

The use of a shared master wallet does **not** mean that Decoy Phrase has access to user data or user credentials.

All data stored in Permanent Storage has the following characteristics:

* **Immutable** — cannot be modified or deleted after upload
* **Permanent** — remains available indefinitely
* **Text-only archival** — designed specifically for long-term text storage
* **Logically non-custodial** — access control remains entirely with the user
* **Meaningless if exposed** — without context, the data cannot be used

## File Upload Flow

Files uploaded via Decoy Phrase follow a secure and optimized flow before being permanently stored on the Arweave blockchain. This process includes **end-to-end encryption**, **efficient bundling**, and **reliable on-chain storage**. Here's how it works:

{% stepper %}
{% step %}
### End-to-End Encryption (via Web Crypto API)

Before your file is sent anywhere, it is **securely encrypted on your device** using the browser’s native **Web Crypto API**—a modern cryptographic standard supported in all major browsers (Chrome, Firefox, Safari, Edge).

* **True client-side encryption**: Your file is encrypted **in the browser**, not on the server.
* **No third-party libraries**: Unlike legacy tools like `crypto-js`, Web Crypto API is faster and more secure, running at system-level performance.
* **More secure by design**: Encryption is handled directly by the browser vendor (e.g., Google, Mozilla), minimizing bugs or weak implementations.

{% hint style="success" %}
Result: Even Decoy Phrase cannot read your files — only you hold the decryption key.
{% endhint %}
{% endstep %}

{% step %}
### Bundling & Upload via Turbo

Once encrypted, your file is **tagged with metadata** (e.g. `App-Name`, `Account-ID`, `Encrypted`) and sent to [**Turbo**](https://turbo.ar.io/)—an enterprise-grade bundling and transmission layer for Arweave.

Turbo provides:

* **Ultra-high-throughput uploads**: Supports efficient bundling of many files.
* **Flexible payments**: Accepts credit cards and crypto (AR, ETH, SOL, USDC).
* **Turbo Credits**: Prepaid credit units for precise storage control.
* **Reliable data pipeline**: Guarantees successful transmission to Arweave.

Turbo converts your file into a **data item** and groups it with others using the **ANS-104** bundling standard.

<details>

<summary><strong>ANS-104 Bundling (Arweave Native Standard)</strong></summary>

To reduce cost and improve efficiency, Turbo uses the **ANS-104** specification to bundle multiple data items into **a single Arweave transaction**.

Benefits of ANS-104:

* **Batch upload**: Sends many files in one blockchain transaction.
* **Standardized format**: Each file remains independently accessible and tagged.
* **Improved indexing**: Easier to search and retrieve structured files.
* **Better network efficiency**: Reduces network congestion and transaction overhead.

Each file inside the bundle maintains:

* A unique **transaction ID (TxID)**
* Its own **tags and metadata**
* **Individual accessibility** via `https://arweave.net/[TxID]`

</details>
{% endstep %}

{% step %}
### Permanent Storage on Arweave

Turbo submits the bundled transaction to the [**Arweave blockchain**](https://ao.arweave.net/), where it becomes:

* **Immutable** – Cannot be deleted or altered
* **Permanently accessible** – Through public gateways like `arweave.net`
* **Individually indexed** – Thanks to preserved ANS-104 structure
{% endstep %}
{% endstepper %}

#### After Upload: File Detail and Access

After upload, each file has a detail page in Decoy Phrase with a direct link to `https://viewblock.io/arweave/tx/[TxID]`, allowing users to verify the file on-chain and view all associated tags and transaction metadata.

{% hint style="warning" %}
**Notes on File Delivery to Arweave via Turbo**

* **Files uploaded through Decoy Phrase are first sent to Turbo**, which bundles multiple files into efficient transactions before submitting them to the Arweave blockchain.
* **There may be a short delay** between uploading a file and its appearance on the Arweave network. This is because Turbo waits to batch files before pushing them on-chain.
* **Getting a TxID immediately does not mean the file is already on-chain.**\
  When users see a transaction ID right after uploading, it means the file is successfully registered in Turbo — but not yet finalized on Arweave.
* **If users visit ViewBlock.io and see the file status as “Pending”,** this means the transaction has not yet been mined into the Arweave blockchain. The file is still waiting in the bundling queue.
* Turbo guarantees delivery: even if there’s a delay, files submitted to Turbo **will be sent to Arweave reliably**, and will eventually become fully accessible and permanent.
* 🔗 To check if a file has been finalized, users can monitor its TxID via:
  * `https://arweave.net/[TxID]`
  * `https://viewblock.io/arweave/tx/[TxID]`
{% endhint %}

## Security & Privacy

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
