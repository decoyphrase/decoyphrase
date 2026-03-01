# What Is Decoy Phrase?

## Definition

Decoy Phrase is an [**offline-first**](core-principles/offline-first.md) **method** with [**permanent storage**](../products-and-features/permanent-storage/) **provisioning** designed to protect and back up seed phrases or any digital keys (passwords, private keys, recovery codes, and similar keys) **without ever storing the original data**.

Instead of storing the real secret, Decoy Phrase **transforms it into** [**ordinary text**](../core-concepts/two-part-security-model/decoy-text.md) that can be freely customized by the user—so it appears normal, non-suspicious, and **has no meaning or value** if viewed or accessed by others.

The original data can only be recovered using a **separate** [**mapping file**](../core-concepts/two-part-security-model/mapping-file.md), and the entire creation and recovery process can be performed **fully offline—without servers, cloud services, or third parties**.

For long-term storage, Decoy Phrase can optionally store the generated decoy text and related files in [**permanent storage**](../products-and-features/permanent-storage/) **built on** [**Arweave**](https://www.arweave.org/). This storage is [**immutable**](core-principles/immutable.md) **by design**, addressing the problem of backups that may survive physically but can still be **lost, altered, or deleted over time**.

## Problem it solves

Decoy Phrase addresses core problems in protecting and backing up seed phrases or sensitive data:

* **Traditional backups are inherently risky**\
  Seed phrases are often written down directly or stored as photos, notes, or plain files—formats that are easy to copy, steal, or read.
* **Reliance on third parties increases exposure**\
  Cloud services, online password managers, and custodial solutions introduce risks such as data breaches, account lockouts, service shutdowns, or policy changes.
* **Single exposure leads to total loss**\
  Once a seed phrase or sensitive secret is leaked, control over the associated assets is usually lost permanently.
* **Long-term durability is poorly addressed**\
  Many backup methods focus on short-term convenience, but fail to ensure that data remains intact, unaltered, and accessible over long periods of time.

## High-level explanation

Decoy Phrase works on a **transform & separate** principle:

* Users transform their seed phrase or sensitive text into **decoy text** that appears ordinary, harmless, and freely customizable.
* The system generates a mapping file—the only component that can restore the original data from its decoy text.
* Without the mapping file, the decoy text is useless.
* Without the decoy text, the mapping file is also meaningless.

No single file or component contains usable sensitive information on its own.

## What Decoy Phrase is not

Decoy Phrase is **not**:

* A crypto wallet or wallet replacement
* An online password manager or cloud vault
* A custodial service that stores or holds users’ seed phrases
* A system that can read, access, or collect users’ secrets
* An automatic recovery service if files or passwords are lost
* A trust-based system that relies on intermediaries or administrators

If a mapping file or required password is lost, recovery is impossible by design.\
All responsibility and control remain entirely with the user.

## Long-term vision

Decoy Phrase is designed not only for today’s security, but for **decades to centuries** into the future. Its long-term vision is to:

* Eliminate direct storage of seed phrases and sensitive secrets
* Treat sensitive data as something that is **never seen, never shared, and never stored in full**
* Use offline-first architecture to remove server and third-party risks
* Rely on immutable storage to ensure long-term availability without trust assumptions

With Decoy Phrase, sensitive digital data can remain **self-sovereign, time-resilient, and private**—without sacrificing user control.
