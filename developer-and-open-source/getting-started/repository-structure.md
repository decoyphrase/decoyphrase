# Repository Structure

{% stepper %}
{% step %}
### High-Level Overview

The DecoyPhrase ecosystem is architected as a monorepo-style collection of three distinct repositories. Each serves a specific role in ensuring privacy, accessibility, and auditability.

We split the codebase to maintain separation of concerns between the public-facing interface, the secure offline mobile environment, and the core cryptographic logic.

| Repository             | Tech Stack              | Purpose                                                                                                  |
| ---------------------- | ----------------------- | -------------------------------------------------------------------------------------------------------- |
| **`decoyphrase-web`**  | Next.js 16, Tailwind v4 | The public web interface. Optimized for speed, accessibility, and zero-knowledge client-side operations. |
| **`decoyphrase-app`**  | Flutter, Dart           | The offline-first mobile application. Handles secure hardware storage and biometrics.                    |
| **`decoyphrase-core`** | Next.js, Arweave        | The "Core". Houses the documentation, shared cryptographic utilities, and Arweave permaweb integrations. |
{% endstep %}

{% step %}
### Web Frontend (`decoyphrase-web`)

This repository contains the user-facing web application. It uses the Next.js App Router.

```
decoyphrase-web/
├── app/                  # Next.js 16 App Router (Pages & Layouts)
│   ├── page.tsx          # Home page entry
│   └── layout.tsx        # Root layout (fonts, providers)
├── components/           # Reusable UI components (React 19)
│   └── ui/               # Primitive components (buttons, inputs)
├── config/               # App-wide configuration
├── constants/            # Static constants
├── lib/                  # Business logic & Utilities
│   ├── api/              # API interaction layers
│   ├── hooks/            # Custom React hooks
│   ├── services/         # Service layer (e.g., Redis)
│   ├── store/            # Zustand state management
│   └── utils/            # Helper functions
├── public/               # Static assets (images, fonts)
├── middleware.ts         # Request processing (Auth/Routing)
└── next.config.ts        # Next.js configuration
```

#### Key Files

* **`middleware.ts`**: Handles edge-level logic before requests reach the page.
* **`tailwind.config.ts`**: Configuration for Tailwind CSS v4.
* **`lib/store/`**: Contains Zustand stores for managing global client state.
{% endstep %}

{% step %}
### Mobile Application (`decoyphrase-app`)

The mobile app is a standard Flutter project organized by feature using the GetX pattern.

```
decoyphrase-app/
├── android/ & ios/       # Native platform code (Gradle, Podfiles)
├── assets/               # Static resources
│   ├── icons/            # App launcher icons
│   ├── images/           # UI images
│   └── words/            # Wordlists for phrase generation
├── lib/                  # Dart source code
│   ├── app/              # GetX Modules
│   │   ├── modules/      # Feature-based folders (View + Controller + Binding)
│   │   └── routes/       # App pages and navigation definitions
│   ├── configuration/    # Environment config
│   ├── gen/              # Generated code (Assets, localizations)
│   └── main.dart         # Application entry point
├── test/                 # Unit and Widget tests
├── pubspec.yaml          # Dependencies and asset definitions
└── analysis_options.yaml # Linter rules (Pedantic/Flutter Lints)
```

#### Key Directories

* **`lib/app/modules/`**: Where the UI code lives. Each screen typically has a `view.dart` (UI) and `controller.dart` (Logic).
* **`assets/words/`**: The local dictionary files used to generate decoy phrases offline.
* **`pubspec.yaml`**: The source of truth for dependencies. Look here to see versions for `flutter_secure_storage` or `encrypt`.
{% endstep %}

{% step %}
### Core & Documentation (`decoyphrase-core`)

The core repository often acts as the "brain" for shared logic and documentation.

```
decoyphrase-core/
├── app/                  # Documentation site pages
├── lib/                  # Shared Core Logic
│   ├── arweave/          # Arweave transaction & wallet logic
│   ├── crypto/           # Standardized cryptographic implementations
│   │   └── aes.ts        # Verifiable AES encryption logic
│   ├── config/           # Core configuration
│   └── utils.ts          # Shared utility functions
├── public/               # Assets
└── next.config.ts        # Config for the docs site
```

#### Key Concepts

* **`lib/crypto/`**: This is the most critical directory for auditors. It contains the raw TypeScript implementations of the encryption standards used across the web ecosystem.
* **`lib/arweave/`**: Handles the interaction with the Permaweb, ensuring decentralized storage of keys or configs.
{% endstep %}
{% endstepper %}
