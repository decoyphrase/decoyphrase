# Offline-First

## Definition

Offline-First means that all core [**Decoy Phrase Generator**](../../products-and-features/decoy-phrase-generator/) processes—including decoy text creation, mapping file generation, and original data recovery—are designed to run entirely on the user’s device without an internet connection. No servers, backends, or third-party services are involved in processing sensitive data.

## What runs offline vs online

**Runs Offline:**

* Input of seed phrases or sensitive text
* Transformation process into decoy text
* Mapping file generation
* Recovery of the original data from decoy text and the mapping file

**Runs Online (Optional):**

* Uploading non-sensitive files (decoy text or mapping files) to permanent storage
* Management of public metadata (e.g., timestamps, file type)
* Accessing and distributing files from permanent storage

{% hint style="danger" %}
Do NOT upload original seed phrases or sensitive data to permanent storage.\
Permanent storage is immutable. Any data uploaded cannot be deleted, edited, or revoked.
{% endhint %}

## Why offline matters for security

The offline-first approach drastically reduces the attack surface:

* No data ever transits over a network
* No risk of logging, sniffing, or man-in-the-middle (MITM) attacks
* No backend that can be compromised
* No administrators or systems with access to the data

In other words, there is no central point of attack, because the secret never leaves the user’s device.

## User implications

For users, the offline-first principle means:

* Users have full control over their sensitive data
* There are no accounts that can be hacked to access seed phrases
* There is no password reset or recovery by the system
* Security depends on the user’s discipline in storing files and passwords

Offline-first provides maximum freedom—but also requires full responsibility from the user.
