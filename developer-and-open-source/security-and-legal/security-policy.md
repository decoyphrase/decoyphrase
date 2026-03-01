# Security Policy

We take the security of DecoyPhrase seriously. Because our software handles sensitive cryptographic keys and private data, we appreciate the community's help in disclosing vulnerabilities responsibly.

## 1. Supported Versions

We only provide security updates for the latest stable release.

| Project              | Version | Supported            |
| -------------------- | ------- | -------------------- |
| **decoyphrase-web**  | 1.x.x   | :white\_check\_mark: |
| **decoyphrase-app**  | 2.x.x   | :white\_check\_mark: |
| **decoyphrase-core** | 2.x.x   | :white\_check\_mark: |
| _Older versions_     | < 1.0.0 | :x:                  |

## 2. Reporting a Vulnerability

{% hint style="warning" %}
Do NOT open a public GitHub issue for security vulnerabilities.
{% endhint %}

If you discover a security vulnerability in any part of the DecoyPhrase ecosystem, please report it **privately** through one of the channels below.

**Email**

* Address: support@decoyphrase.com
* Subject: `[VULN] Short description`
* Body (please include):
  * Steps to reproduce
  * Affected versions
  * Proof of Concept (PoC) code or screenshots

**Discord (Private Message)**

* You may also report vulnerabilities via **direct message** on our official Discord server: [https://discord.gg/yqVt2YwN](https://discord.gg/yqVt2YwN)

### Response Timeline

{% stepper %}
{% step %}
### Acknowledgment

We will acknowledge your report within **48 hours**.
{% endstep %}

{% step %}
### Assessment

We will provide an initial assessment and estimated fix timeline within **5 business days**.
{% endstep %}

{% step %}
### Fix & Disclosure

Once a fix is verified and deployed, we will coordinate a public disclosure.
{% endstep %}
{% endstepper %}

## 3. Scope

We are interested in:

* **Crypto flaws:** Weak key generation, improper IV usage, or side-channel leaks in `lib/crypto`.
* **Data leakage:** Private keys being persisted insecurely (e.g., in `localStorage` without encryption, or sent to a server).
* **Injection:** XSS or other injection attacks in the Web client.
* **Bypass:** Methods to bypass biometric authentication on the Mobile app.

We are **NOT** interested in:

* UX bugs or typos.
* DDoS attacks on our documentation site.
* Issues related to third-party Arweave gateways (unless it compromises client security).

## 4. Safe Harbor

If you conduct security research within the scope of this policy, we consider your activities authorized and will not initiate legal action against you. We ask that you:

* Do not destroy or corrupt data.
* Do not interrupt or degrade our services.
* Give us reasonable time to fix the issue before making it public.
