# Core Principles

## Principles overview

Decoy Phrase is built on a set of **core principles** that are inseparable from its system architecture.\
These principles are not additional features, but **foundational design decisions** that define how the system works, what is possible, and what is intentionally never done.

The core principles of Decoy Phrase include:

* [**Offline-First**](offline-first.md) — sensitive processes never depend on an internet connection
* [**Zero Knowledge**](zero-knowledge.md) — the system has no technical knowledge of user data contents
* [**No Seed Storage**](no-seed-storage.md) — the original seed phrase or digital keys is never stored, anywhere
* [**No Third Parties**](no-third-parties.md) — no custodians, administrators, or intermediaries
* [**Immutable**](immutable.md) — stored data and system components are permanent and cannot be altered or erased

These principles are designed to **complement one another** and together form a unified security and durability model.

## Why principles matter

In traditional security systems, protection often depends on:

* Privacy policies
* Trust in service providers
* The strength of server-side encryption
* Operational procedures and human factors
* Institutional control over access and recovery

Decoy Phrase takes a fundamentally different approach by **eliminating the need for trust altogether**.

These principles matter because:

* Security does not rely on the goodwill of third parties
* Risk is not merely reduced, but **eliminated at the architectural level**
* There is no high-value single point of failure
* The system remains secure even if public infrastructure, storage layers, or metadata are exposed
* Long-term availability does not depend on service continuity or human intervention

In other words, Decoy Phrase’s security and durability are not determined by **who operates the system**, but by **what the system is technically incapable of doing**.

## How principles shape the system

The entire Decoy Phrase architecture is a direct consequence of these core principles:

* **Offline-First** ensures that seed phrase transformation, mapping file creation, and recovery always run on the user’s device, without any backend or server dependency.
* **Zero Knowledge** guarantees that neither the website, permanent storage, nor the developers ever have access to file contents, file names, passwords, or seed phrases.
* **No Seed Storage** removes the existence of vaults containing original secrets, eliminating high-value targets that could be stolen or hacked.
* **No Third Parties** places ownership and control entirely in the hands of the user, with no resets, overrides, approvals, or human intervention.
* **Immutable** ensures that once data or system components are stored on permanent infrastructure, they cannot be modified, censored, or silently removed—providing long-term integrity, availability, and resistance to tampering.

## The Result

The result is a system that:

* Does not store secrets
* Does not know secrets
* Cannot access secrets
* Cannot modify stored data
* Does not require trust

These core principles make Decoy Phrase not just a security tool, but **a new model for protecting sensitive data over time**—built on cryptography, architecture, permanence, and user sovereignty.

## Consequences of the Principles

Because Decoy Phrase is built on non-negotiable architectural principles, the system carries **intentional and irreversible consequences**. These consequences are not flaws or limitations—they are the natural outcomes of designing a system that removes trust, custody, and discretion entirely.

#### 1. No Recovery by Anyone Else

<details>

<summary><strong>Explanation</strong></summary>

There is **no password reset**, no customer support recovery, and no administrative override.

If a user loses:

* Their decoy text
* Their mapping file
* Permanent storage password

Then **recovery is mathematically impossible**.

This is a direct consequence of:

* Offline-First
* Zero Knowledge
* No Third Parties

The system cannot help—because it was never designed to be able to.

</details>

#### 2. User Responsibility Is Absolute

<details>

<summary><strong>Explanation</strong></summary>

Decoy Phrase transfers **full ownership and responsibility** to the user.

There is:

* No guardian
* No custodian
* No fallback authority

The system does not make decisions on behalf of the user, and it does not protect users from their own operational mistakes.

This consequence is inseparable from **user sovereignty**.

</details>

#### 3. No Silent Changes, Fixes, or Interventions

<details>

<summary><strong>Explanation</strong></summary>

Because the system and stored components are immutably written to permanent storage:

* Data cannot be edited or deleted after upload
* Errors cannot be retroactively patched
* Mistakes cannot be quietly corrected

What is uploaded is final.

This guarantees integrity and censorship resistance—but removes flexibility.

</details>
