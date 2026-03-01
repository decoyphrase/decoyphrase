# Changelog

All notable changes to the **DecoyPhrase** ecosystem (Web, Mobile, Core) will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

{% updates format="full" %}
{% update date="2026-03-01" %}
## \[Unreleased]

#### Added

* **Web:** **Modernized Landing Page & Navigation** - Designed and integrated a comprehensive, visually appealing landing page equipped with an updated navigation structure to enhance user journey and site discoverability (`f806499`).
* **Web:** **Dynamic Platform Download Links** - Re-engineered platform download links to dynamically point to GitHub releases, while refining the metric-fetching logic for more accurate GitHub statistics display (`2c11c9b`).
* **Web:** **Core Web Initialization** - Initialized the fundamental React/Next.js client web architecture for the DecoyPhrase web platform (`95b73c5`).
* **Backend:** **Premium API Landing Page** - Developed a minimalist, premium-tier API landing page to better serve API consumers and clearly outline available endpoints (`1047a85`).
* **Backend:** **Secure Turbo Operations Backend** - Bootstrapped the core backend framework equipped with top-tier security measures, specifically tailored for high-speed 'turbo' operations (`0d0cf0f`).
* **Core:** **Sidebar Enhancement** - Introduced direct 'Donate' and 'Download' links within the application sidebar to boost conversion rates and user accessibility (`dc9540e`).
* **Core:** **Production Ready Configuration** - Finalized the initial secure backend integration setup alongside a robust, production-ready configuration pipeline (`d5aae5d`).
* **App:** **Mobile Application Bootstrap** - Successfully established the foundational codebase for the DecoyPhrase mobile application (`e7be1f2`).
* **Docs:** **Documentation Updates** - Added initial documentation structure and GitBook integration (`09ae0d8`, `25b2b54`).

#### Changed

* **Web:** **L7 Code Quality Standards Alignment** - Executed a sweeping refactor across all client services to strictly adhere to the rigorous L7 code quality and maintainability standards (`494ff35`).
* **Web:** **Client-Side Service Migration** - Fully transformed our data-fetching paradigm by completing the migration to entirely client-side services, paving the way for seamless static exports (`964b4bc`).
* **Web:** **Arlink Static Export Configuration** - Finely tuned the build configuration specifically for optimized static exports deployed onto the Arlink decentralized network (`126d6b5`).
* **Core:** **Layout & Menu Polish** - Executed minor UI layout changes and updated menu structures for better responsive scaling and visual harmony (`a402450`).
* **Core:** **Global Code Formatting** - Applied stringent global code formatting and generic codebase cleanups to improve developer velocity (`ea7e262`).

#### Fixed

* **Web:** **Real-Time Data Metric Inaccuracies** - Patched critical bugs affecting the real-time calculation and display of total users and live donation metrics, ensuring accurate public-facing statistics (`d256b58`).
{% endupdate %}

{% update date="2026-02-01" %}
## \[1.0.0] - 2026-02-01

**Milestone:** Initial Public Release (MVP)

#### Added

* **Web:**
  * Full encryption/decryption suite using `crypto-js` (AES-256-GCM).
  * Integration with Upstash Redis for ephemeral session storage.
  * Responsive UI built with Tailwind CSS v4 and Framer Motion.
  * Zero-knowledge key generation logic in `lib/crypto`.
* **Mobile:**
  * Complete offline-first architecture using Flutter 3.10+.
  * Secure storage implementation via `flutter_secure_storage` (Keychain/Keystore).
  * Biometric authentication (`local_auth`) for app access.
  * Bundled wordlists in `assets/words/` for offline phrase generation.
* **Core:**
  * Arweave permaweb integration for immutable documentation.
  * Comprehensive documentation site (this repo).
  * Shared TypeScript utility library for cryptographic standards.

#### Changed

* **Repo:** Restructured project into a monorepo-style organization (`web`, `mobile`, `core`) for better maintainability.
* **CI/CD:** Enforced strict linting rules (`eslint` for web, `flutter_lints` for mobile) on all Pull Requests.

#### Fixed

* **Mobile:** Resolved padding issues on iOS devices with Dynamic Island.
* **Web:** Fixed hydration mismatch errors in Next.js App Router for dark mode toggles.

#### Security

* **Audit:** Validated that no private keys are ever transmitted to the backend server.
* **Deps:** Pinned all critical cryptographic dependencies to specific versions to prevent supply-chain attacks.
{% endupdate %}
{% endupdates %}
