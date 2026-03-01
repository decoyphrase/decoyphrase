# Environment Setup

Welcome to the **DecoyPhrase** developer ecosystem. This guide ensures you have the correct tools and configurations to contribute to the Web, Mobile, and Core projects.

## 1. Prerequisites

Before cloning the repositories, ensure your local machine meets the following requirements. We enforce strict versioning to prevent "it works on my machine" issues.

### Global Tools

* **Node.js**: `v20.0.0` or higher (Required for Web & Core).\
  Verify: `node -v`
* **Package Manager**: `npm` (bundled) or `pnpm` (recommended for speed).
* **Git**: For version control.
* **VS Code** (Recommended): Install the **Flutter** and **Prettier** extensions.

### Mobile-Specific

* **Flutter SDK**: `3.10.4` or higher.\
  Verify: `flutter doctor`
* **Dart SDK**: Compatible with your Flutter version.
* **Xcode** (macOS only): For iOS simulation.
* **Android Studio**: For Android emulation (Min SDK 21).

***

## 2. Repository Cloning

We recommend organizing your workspace into a single directory to manage the three interconnected projects easily.

{% stepper %}
{% step %}
### Prepare workspace

```bash
mkdir ~/workspace/decoyphrase
cd ~/workspace/decoyphrase
```
{% endstep %}

{% step %}
### The Frontend (Web Client)

```bash
git clone https://github.com/decoyphrase/decoyphrase-web.git
```
{% endstep %}

{% step %}
### The Mobile App (Flutter)

```bash
git clone https://github.com/decoyphrase/decoyphrase-app.git
```
{% endstep %}

{% step %}
### The Core (Docs & Utilities)

```bash
git clone https://github.com/decoyphrase/decoyphrase-core.git
```
{% endstep %}
{% endstepper %}

***

## 3. Project Configuration & Installation

Each project requires specific environment variables to function correctly. **Do not commit `.env` files to version control.**

### A. Web & Core Setup (Node.js)

Both `decoyphrase-web` and `decoyphrase` use the Next.js ecosystem.

{% stepper %}
{% step %}
### Install Dependencies

```bash
# For Web
cd decoyphrase-web
npm install

# For Core (in a separate terminal)
cd ../decoyphrase
npm install
```
{% endstep %}

{% step %}
### Environment Variables (.env)

You must create a `.env.local` file in the root of **both** directories.

For `decoyphrase-web` (relies on Upstash Redis):

```bash
cp .env.example .env.local
```

Edit `.env.local` to include:

```ini
# Required for server-side state
UPSTASH_REDIS_REST_URL="https://your-db-url.upstash.io"
UPSTASH_REDIS_REST_TOKEN="your-secret-token"
```
{% endstep %}

{% step %}
### Core (.env) — Arweave integration

For `decoyphrase` (Core):

```bash
cp .env.example .env.local
```

Edit `.env.local` to include:

```ini
# Required for Arweave transactions
NEXT_PUBLIC_MASTER_WALLET_JWK="your-wallet-jwk-json-string"
```
{% endstep %}

{% step %}
### Start Development Servers

```bash
npm run dev
```

* Web: `http://localhost:3000`
* Core: `http://localhost:3001` (Ensure ports do not conflict)
{% endstep %}
{% endstepper %}

### B. Mobile Setup (Flutter)

The mobile app is designed to be **offline-first**, so it requires minimal environment configuration but strict dependency management.

{% stepper %}
{% step %}
### Install Dependencies

```bash
cd decoyphrase-app
flutter pub get
```
{% endstep %}

{% step %}
### Asset Generation

If icons or wordlists appear missing, regenerate the assets:

```bash
flutter pub run flutter_launcher_icons
```
{% endstep %}

{% step %}
### Run the App

Select your target device (Simulator or Physical Device) and run:

```bash
flutter run
```
{% endstep %}
{% endstepper %}

***

## 4. Troubleshooting

| Issue                       | Solution                                                                                |
| --------------------------- | --------------------------------------------------------------------------------------- |
| **Node Version Warning**    | Ensure you are on Node `v20+`. Use `nvm use 20` if you use NVM.                         |
| **CocoaPods Error (iOS)**   | Run `sudo gem install cocoapods` then `cd ios && pod install`.                          |
| **Missing Assets**          | Verify `pubspec.yaml` assets section and run `flutter pub get`.                         |
| **Arweave Connection Fail** | Check that your `NEXT_PUBLIC_MASTER_WALLET_JWK` in `.env.local` is a valid JSON string. |
