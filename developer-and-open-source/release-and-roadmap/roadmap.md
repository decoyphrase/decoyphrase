# Roadmap

Our development is driven by a commitment to privacy, security, and community feedback. This document outlines the current state of the DecoyPhrase ecosystem and our plans for the future.

## 1. Current Status (v1.0 - MVP)

We have successfully launched the Minimum Viable Product (MVP) across all three pillars of our ecosystem.

* ✅ Web Client: A fully functional, zero-knowledge interface built with Next.js 16 and Tailwind v4. Users can generate keys and encrypt payloads in the browser.
* ✅ Mobile App: A stable, offline-first Flutter application for Android and iOS. It includes secure hardware storage and biometric authentication.
* ✅ Core Infrastructure: We have established the Permaweb integration using Arweave for immutable documentation and public key registries.

## 2. Upcoming Features&#x20;

We are actively working on the following features. Priorities may shift based on community contribution and feedback.

{% stepper %}
{% step %}
### Decoy Phrase Generator 2.0 <mark style="color:$warning;">(Q1 2026)</mark> <mark style="color:yellow;">\[Progress]</mark>

An updated version of the Decoy Phrase Generator with an additional **Split ASCII Text** feature. This enhancement allows decoy phrases to be generated in a more **human-readable** form, enabling users to customize repeated or familiar words while maintaining structural plausibility. The goal is to produce decoy seed phrases that look natural and believable to humans, without exposing real cryptographic secrets.

> ### **Use Case**
>
> * Creating realistic decoy seed phrases for wallet backups and security drills
> * Protecting real seed phrases during coercion or social engineering attempts
> * Allowing users to customize decoy text while preserving entropy distribution
> * Improving memorability and plausibility of decoy phrases without compromising security
{% endstep %}

{% step %}
### Decoy Autofill Browser Extension <mark style="color:$warning;">(Q2 2026)</mark> <mark style="color:$danger;">**\[In Research]**</mark>

A browser autofill extension designed to prevent sensitive credentials from being visually exposed. Even when autofill fields are unhidden, the displayed password remains **encrypted or substituted**, while the real credential is silently injected only at the moment of legitimate form submission. This design ensures that sensitive data is never visible on screen.

> ### **Use Case**
>
> * Preventing credential theft during screen sharing or remote access sessions
> * Protecting users when their device is temporarily accessed by others
> * Mitigating social engineering attacks that rely on visual confirmation of passwords
> * Reducing the risk of credential leakage from shoulder surfing or malicious assistance tools
{% endstep %}

{% step %}
### Proof of History Time Capsule <mark style="color:$warning;">(Q3 2026)</mark> <mark style="color:$danger;">**\[In Research]**</mark>

A decentralized, trustless application that enables users to lock encrypted digital content (text, messages, or cryptographic keys) in time. Digital capsules can only be accessed after a specific, predetermined moment, ensuring that sensitive information remains sealed until the exact time intended—without relying on third parties.

> **Use Case**
>
> * Securely inheriting digital keys or sensitive text without involving third parties
> * Scheduling the release of confidential information at a specific future date
> * Creating cryptographically verifiable digital legacies
> * Ensuring time-based access control resistant to manipulation or early disclosure
{% endstep %}
{% endstepper %}

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
