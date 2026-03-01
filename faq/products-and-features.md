# Products & Features

<details>

<summary><strong>What is the Decoy Phrase Generator and what are its components?</strong></summary>

The **Decoy Phrase Generator** is the core tool in the Decoy Phrase system, combining the **Mapping Maker** and the **Text Generator**.

The Mapping Maker transforms seed phrases or sensitive data into ordinary decoy text and generates a mapping file that serves as the recovery key, while the Text Generator uses that mapping file to restore the original data from the decoy text.

All processes run entirely on the user’s device without an internet connection, ensuring that no sensitive data is ever sent to any server.

</details>

<details>

<summary><strong>What is a Mapping File and why must it be stored separately?</strong></summary>

A **Mapping File** is a private (.json) file containing technical information and serves as the **only key** to recover the original data from the decoy text.

It does not contain sensitive data directly and is meaningless without its related decoy text.\
For this reason, the Mapping File must be stored separately from the decoy text. This separation prevents any single file from revealing secrets. Without the correct combination of both, recovery is impossible—meaning no single component contains exploitable sensitive information on its own.

</details>

<details>

<summary><strong>How does Permanent Storage work and what file formats are supported?</strong></summary>

**Permanent Storage** is an Arweave-based storage layer that stores decoy text and mapping files permanently and immutably.

It is designed as **write-once, read-forever** storage for long-term text backups without relying on traditional servers.

Permanent Storage supports **text-based files only**, such as `.txt`, `.md`, and `.json`. Other formats like images, videos, or audio files are not supported.

All uploads are managed through a single account using a **Shared Master Wallet**, so users do not need to create or manage a blockchain wallet or understand blockchain mechanics. The blockchain complexity is hidden behind a simple user interface.

</details>

<details>

<summary><strong>What are Multi-Password Vaults and how are they used?</strong></summary>

**Multi-Password Vaults** are a feature of Permanent Storage that allow a single account to contain multiple isolated storage vaults, each protected by a different password.\
For example, a user can store decoy text in Vault A and mapping files in Vault B, using separate passwords for each.

Each vault is logically isolated, meaning access to one vault does not grant access to others. As a result, compromising one password exposes only one vault, keeping other sensitive files secure.

</details>

<details>

<summary><strong>Can Decoy Phrase Generator be used on different devices?</strong></summary>

Yes. The **Decoy Phrase Generator** is available across platforms.\
It can run on major desktop operating systems (Windows, macOS, Linux) as well as on Android devices.

Because all processes run offline on the local device, Decoy Phrase can also be used in environments without internet access or on high-security systems such as air-gapped computers.

</details>

<details>

<summary><strong>Do users need to understand blockchain to use these features?</strong></summary>

No. Although Decoy Phrase uses blockchain technology (Arweave) behind the scenes for permanent storage, the interface is designed so users do not need to deal with any blockchain-related complexity.

By using a **Shared Master Wallet**, users only need to focus on managing their text and passwords—they do not need to create, store, or manage their own blockchain wallets.\
As a result, all Decoy Phrase features can be used without any prior knowledge of blockchain technology.

</details>
