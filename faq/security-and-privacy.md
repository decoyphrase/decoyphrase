# Security & Privacy

<details>

<summary><strong>How does the system protect user data?</strong></summary>

Decoy Phrase applies **offline-first** and **zero-knowledge** principles, meaning that all sensitive data transformation and encryption are performed entirely on the user’s device—without requiring an internet connection or any server.

Data is processed and encrypted on the client side (for example, using AES-256-GCM) before being stored in Permanent Storage, so public storage only ever contains encrypted data that cannot be read without the user’s keys.

In addition, no seed phrases or original sensitive data are ever stored on any server, meaning there is no central “vault” that could become a high-value attack target. This approach removes reliance on third parties and shifts security from trust-based protection to a technical architecture that makes external access impossible by design.

</details>

<details>

<summary><strong>Can Decoy Phrase delete my files in Permanent Storage?</strong></summary>

No. **Decoy Phrase cannot delete your files once they are stored in Permanent Storage.**\
Permanent Storage is built on the Arweave blockchain, where data is **immutable by design**. Once a file is uploaded, it cannot be removed, modified, or erased by Decoy Phrase—or by anyone else.

</details>

<details>

<summary><strong>How does the system ensure that no sensitive data is stored?</strong></summary>

Decoy Phrase uses a **“transform and separate”** principle.\
Original data is converted offline into ordinary decoy text that appears random and contains no secret meaning. The generated mapping file contains technical recovery information but does not include the original sensitive data.

These two components must be stored separately (for example, in different locations or protected by different passwords). As a result, no single component ever contains the original secret. Without the mapping file, the decoy text is useless—and without the decoy text, the mapping file is meaningless.

This method ensures that original sensitive data is never directly stored in the application or on any server.

</details>

<details>

<summary><strong>What does the system know and not know in Permanent Storage?</strong></summary>

Decoy Phrase is **zero-knowledge**, meaning the system never knows the contents of user data.

It cannot see seed phrases, passwords, or original file contents because all data is fully encrypted in the user’s local browser before upload.

The only information visible to the system is **non-sensitive public metadata**, such as a username (used as a public identifier) and the number of stored files.

The relationship between decoy text and its mapping file is also unknown to the system. In short, user content and secrets are never exposed—only encrypted data and limited public metadata exist.

</details>

<details>

<summary><strong>How does Decoy Phrase’s security approach differ from traditional systems (such as password managers)?</strong></summary>

* **Original data storage**\
  Traditional password managers store user secrets (passwords, seeds, etc.) inside an encrypted vault. Decoy Phrase **never stores original data at all**.
* **Architecture**\
  Password managers typically rely on servers or cloud infrastructure for synchronization. Decoy Phrase is **offline-first**, with no backend and no third-party dependency.
* **Security model**\
  In password managers, security depends on vault encryption and a master password—if the vault or master password is compromised, all data may be exposed.\
  Decoy Phrase has no such vault. Leaking a single file (either decoy text or mapping file) is not sufficient to recover the original data, because each component has no value on its own.
* **Single point of failure**\
  A password manager’s vault is a high-value target. Decoy Phrase has no single object that contains secrets; until both components (decoy text and mapping file) are compromised together, there is no primary point of failure to attack.

</details>

<details>

<summary><strong>What happens if a decoy file or mapping file falls into someone else’s hands</strong></summary>

* If **only the decoy text** is exposed, no secret is revealed. The decoy text is ordinary data with no sensitive meaning and cannot be used without the mapping file.
* If **only the mapping file** is exposed, the original data remains safe. The mapping file contains only technical character patterns, not secret content, and is useless without its related decoy text.
* **Only if both are exposed together** can the original data be recovered. In that case, security fully collapses because the attacker has both required components.

</details>

<details>

<summary><strong>What is the risk of failing to separate files?</strong></summary>

The primary risk occurs if the decoy text and mapping file are **not stored separately** (for example, in the same location or protected by the same password).

If this happens, anyone who gains access to both components can directly recover the original data. In other words, the system fails only when the two components are unintentionally brought together.

For this reason, strict separation is essential: store decoy text and mapping files in different locations or protect them with different passwords. When properly separated, such failure is extremely unlikely.

</details>
