# Decoy Phrase Generator

<figure><img src="../../.gitbook/assets/Decoy Phrase Generator Icon.png" alt="" width="375"><figcaption></figcaption></figure>

**Decoy Phrase Generator** is the core tool within the Decoy Phrase system, combining a [**Mapping Maker** ](mapping-maker.md)for creating decoy text and mapping files, and a [**Text Generator**](text-generator.md) for recovering the original data. All operations run fully offline and remain entirely under the user’s control.

## Purpose

The primary purposes of the Decoy Phrase Generator are:

* **To transform seed phrases or sensitive data** into decoy text that appears normal and holds no meaningful value to others.
* **To generate a mapping file** that serves as the only key required to recover the original data from the decoy text.

Without the mapping file, the decoy text cannot be used to infer, guess, or reconstruct the original secret in any way.

## Offline Guarantees

The Decoy Phrase Generator is built on an [**offline-first**](../../introduction/core-principles/offline-first.md) principle.

This means:

* All processes run 100% on the user’s device
* No data is sent to servers, cloud services, or third parties
* No logging, telemetry, or data collection is performed
* Seed phrases or sensitive text never leave the device

With this approach, the Decoy Phrase Generator ensures that even Decoy Phrase itself never knows or stores the user’s secret.

## Supported Platforms

The Decoy Phrase Generator is designed to be widely accessible and flexible.

**Supported platforms:**

* Desktop
  * Windows
  * macOS
  * Linux
* Android

{% hint style="info" %}
[Click here download the Decoy Phrase Generator for your platform](https://decoyphrase.arweave.net/download)
{% endhint %}

Because all logic runs locally and does not rely on any backend infrastructure, the generator can be used:

* Without creating an account
* Without an internet connection
* In high-security environments (air-gapped devices)

This approach allows users to choose a security setup that fits their needs, from everyday use to long-term and cross-generation storage.

{% hint style="info" %}
[LEARN HOW TO USE IT!](../../user-guide/decoy-phrase-generator.md)
{% endhint %}
