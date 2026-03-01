# Roadmap

Our development is driven by a commitment to privacy, security, and community feedback. This document outlines the current state of the DecoyPhrase ecosystem and our plans for the future.

## 1. **Initial Implementation** <a href="#id-1.-initial-implementation" id="id-1.-initial-implementation"></a>

We have successfully launched the Minimum Viable Product (MVP) across all three pillars of our ecosystem.

* ✅ Web Client: A fully functional, zero-knowledge interface built with Next.js 16 and Tailwind v4. Users can generate keys and encrypt payloads in the browser.
* ✅ Mobile App: A stable, offline-first Flutter application for Android and iOS. It includes secure hardware storage and biometric authentication.
* ✅ Core Infrastructure: We have established the Permaweb integration using Arweave for immutable documentation and public key registries.

## 2. Upcoming Features&#x20;

We are actively working on the following features. Priorities may shift based on community contribution and feedback.

{% updates format="full" %}
{% update date="2026-02-14" %}
## Decoy Phrase Generator 2.0

STATUS: [<mark style="color:$success;">**Delivered**</mark>](https://decoyphrase.arweave.net/download)

An updated version of the Decoy Phrase Generator with an additional **Split ASCII Text** feature. This enhancement allows decoy phrases to be generated in a more **human-readable** form, enabling users to customize repeated or familiar words while maintaining structural plausibility. The goal is to produce decoy seed phrases that look natural and believable to humans, without exposing real cryptographic secrets.
{% endupdate %}

{% update date="2026-04-01" %}
## <mark style="color:$primary;">Decoy Autofill Browser Extension</mark>

STATUS: <mark style="color:$danger;">**In Research**</mark>

A browser autofill extension designed to prevent sensitive credentials from being visually exposed. Even when autofill fields are unhidden, the displayed password remains **encrypted or substituted**, while the real credential is silently injected only at the moment of legitimate form submission. This design ensures that sensitive data is never visible on screen.
{% endupdate %}

{% update date="2026-06-01" %}
## <mark style="color:$primary;">Decoy Phrase Generator – Play Store & App Store Availability</mark>&#x20;

STATUS: <mark style="color:$danger;">**Planned (Community-Driven)**</mark>

This roadmap outlines the planned availability of the Decoy Phrase Generator on the Play Store and App Store. It provides visibility into the development, review, and release stages required before the application can be officially downloaded from mobile app marketplaces. Until then, the generator remains accessible through supported distribution channels while maintaining the same security and privacy guarantees.
{% endupdate %}

{% update date="2026-08-01" %}
## <mark style="color:$primary;">Proof of History Time Capsule</mark>

STATUS: <mark style="color:$danger;">**In Research**</mark>

A decentralized, trustless application that enables users to lock encrypted digital content (text, messages, or cryptographic keys) in time. Digital capsules can only be accessed after a specific, predetermined moment, ensuring that sensitive information remains sealed until the exact time intended—without relying on third parties.
{% endupdate %}
{% endupdates %}

## 3. Contributing to the Roadmap

Want to see a feature that isn't listed here?

{% stepper %}
{% step %}
Check our GitHub Issues to see if it has already been requested:

* https://github.com/muhvarriel/decoyphrase/issues
{% endstep %}

{% step %}
Open a new Feature Request issue with the tag `enhancement`.
{% endstep %}

{% step %}
Better yet, fork the repo and submit a PR! See How to Contribute:

* ./how\_to\_contribute.md
{% endstep %}
{% endstepper %}

You can contribute to the roadmap in several ways. One way is to join our Discord and share your ideas, feature suggestions, or security considerations. Join [here!](https://discord.com/invite/q9cYTxtagJ)
