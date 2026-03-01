# Architecture & Design

{% stepper %}
{% step %}
### System Overview

The ecosystem consists of three interconnected pillars:

* **Web Client (Zero-Knowledge):** A browser-based interface where all encryption happens client-side before any data touches the network.
* **Mobile App (Offline-First):** A standalone vault that operates without internet dependency, utilizing secure hardware storage.
* **Core Infrastructure (Permaweb):** Decentralized storage for non-sensitive public keys and immutable documentation using Arweave.
{% endstep %}

{% step %}
### Web Architecture (decoyphrase-web)

The web platform is designed for speed and security, leveraging the latest features of the React ecosystem.

#### Tech Stack

* **Framework:** Next.js 16 (App Router)
* **Styling:** Tailwind CSS v4
* **State Management:** Zustand
* **Data Persistence:** Upstash Redis (Ephemeral/Session data)

#### Key Design Patterns

**Server Actions & Security**

We utilize Next.js Server Actions for data mutations. However, strict boundaries are enforced:

* **Client-Side Encryption:** Payloads are encrypted in the browser using the shared `lib/crypto` utilities _before_ being sent to a Server Action.
* **Zero-Knowledge Server:** The Next.js server acts as a blind relay. It never sees raw private keys or unencrypted phrases.

**Global State (Zustand)**

We use Zustand for managing client state (e.g., wallet connection status, theme preferences). This avoids the "Prop Drilling" problem while keeping the bundle size smaller than Redux-based alternatives.
{% endstep %}

{% step %}
### Mobile Architecture (decoyphrase-app)

The mobile application is an air-gapped vault in your pocket. It is designed to function fully without network access.

#### Tech Stack

* **Framework:** Flutter (Dart)
* **State Management:** GetX
* **Local Storage:** `flutter_secure_storage` & `shared_preferences`
* **Security:** `local_auth` (Biometrics)

#### Offline-First Design

* **Asset Bundling:** All necessary dictionaries and wordlists are bundled in `assets/words/`. No API calls are needed to generate phrases.
* **Secure Storage:**
  * **iOS:** Uses the Keychain.
  * **Android:** Uses the Keystore (AES encryption).
  * Note: We use `flutter_secure_storage` to persist encrypted Master Keys, while standard preferences handle non-sensitive UI state.

#### GetX Pattern

We separate concerns using the Model-View-Controller (MVC) approach via GetX:

* **View:** Pure UI widgets. Stateless where possible.
* **Controller:** Business logic and observable state (`Rx` variables).
* **Bindings:** Dependency injection setup that lazy-loads controllers when routes are accessed.
{% endstep %}

{% step %}
### Core & Cryptography (decoyphrase-core)

The "Core" represents the shared brain of the ecosystem.

#### Tech Stack

* **Cryptography:** `crypto-js` (AES-256-GCM, SHA-256)
* **Storage:** Arweave (Permaweb)

#### Zero-Knowledge Principles

Our architecture adheres to the following rules:

* **Keys stay local:** Private keys are generated in memory and stored only in the device's secure enclave (Mobile) or LocalStorage (Web - strictly user controlled).
* **Verifiable Algorithms:** The `lib/crypto/` directory contains standard implementations of AES. We do not roll our own crypto.
* **Immutable Docs:** Documentation and public key registries are stored on Arweave, preventing censorship or silent tampering.
{% endstep %}
{% endstepper %}
