# Immutable

In Decoy Phrase, **immutability applies to Permanent Storage** as well as to its associated domains (website and storage domain). **Immutable** means that data, once stored, **cannot be modified or deleted**. This core principle ensures that information within the Decoy Phrase system remains available forever and protected from unauthorized changes.

To achieve this level of permanence and security, Decoy Phrase leverages [**Arweave**](https://www.arweave.org/) and the [**AR.IO Network**](https://ar.io/)—permaweb technologies built on top of Arweave—so that Decoy Phrase data and websites are stored permanently and are **tamper-proof**. In other words, once data is uploaded, it continues to exist on the network in its original form and cannot be altered by any party.

## Permanent Decentralized Storage with Arweave

Arweave is a decentralized storage network specifically designed for **permanent data storage**. It can be thought of as Bitcoin, but for data: its primary focus is ensuring that information remains stored forever. Once data—whether a tweet, NFT, document, or website—is uploaded to Arweave, it becomes **permanent** and **immutable**, preserved without time limits. The network functions like a global, tamper-resistant hard drive, where stored files remain accessible far into the future.

## How Does Arweave Ensure Data Permanence?

Arweave guarantees long-term data availability through several key mechanisms:

<details>

<summary><strong>Blockweave Architecture</strong></summary>

Unlike traditional blockchains that use a linear chain of blocks, Arweave employs a _blockweave_ architecture. Each new data block links not only to the previous block, but also to a randomly selected older block. Uploaded data is split into 256 KB chunks and organized into a secure Merkle tree. This design requires miners to store the entire historical dataset in order to add new blocks, ensuring that all past data continues to be preserved by the network.

</details>

<details>

<summary><strong>Succinct Proofs of Random Access (SPoRA)</strong></summary>

Arweave uses a proof mechanism in which miners must demonstrate that they are storing multiple copies of data through random access challenges. Periodically, miners are required to retrieve random data chunks they store, verified using _Verifiable Delay Functions (VDFs)_. This combination of proof-of-work and proof-of-storage makes data loss extremely unlikely, as miners who fail to store data correctly cannot participate in block production.

</details>

> **Simple analogy:**\
> Imagine a library where every new book must reference older books, forcing librarians to keep all previous volumes in order to add new ones. SPoRA acts like random inspections that ensure librarians truly retain the entire collection. As a result, the library’s books—its data—remain safely preserved forever.

## Guaranteed Data Security and Integrity

Immutability also implies **strong security and data integrity guarantees**. Data stored on Arweave is distributed across many nodes and protected by cryptography, ensuring that no single entity can manipulate or delete it at will. Any unauthorized modification would be invalid, as it would not match the original recorded data hash—making Arweave inherently **tamper-proof**.

Additionally, replication across multiple nodes eliminates single points of failure. Even if individual nodes go offline, identical copies of the data remain available elsewhere on the network. This makes stored data resistant to censorship, loss, and accidental deletion. Data integrity is preserved over time: data retrieved in the future will be **identical to the data originally stored**.

## Immutable as a Core Principle of Decoy Phrase

By adopting the **Immutable** principle, Decoy Phrase ensures that both user-related data artifacts and system components are stored permanently on the Arweave/AR.IO network. This data is protected from unwanted modification, cannot be censored or erased by external parties, and remains accessible whenever needed.

This principle provides a strong guarantee of **long-term durability and security**, allowing users to place lasting trust in the integrity and availability of their data within the Decoy Phrase ecosystem.
