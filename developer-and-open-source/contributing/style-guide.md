# Style Guide

To maintain a codebase that is secure, readable, and maintainable across our three repositories, we enforce strict style guides. Automated tools are used wherever possible to catch violations before code reviews.

## 1. Web & Core (`decoyphrase-web` / `decoyphrase`)

Our web projects rely on the TypeScript ecosystem's standard tooling.

### A. Linting & Formatting

We use **ESLint** for code quality and **Prettier** for code formatting.

* **Configuration**:
  * `eslint.config.mjs`: Defines our rule sets.
  * `.prettierrc`: Defines formatting preferences (e.g., single quotes, no semi-colons).

{% hint style="info" %}
Key Rules:

* **No `any`**: Explicitly type variables. If you truly need flexibility, use `unknown` and type guard it.
* **Imports**: Sorted automatically. Absolute imports (e.g., `@/components/...`) are preferred over relative paths.
* **React Hooks**: Exhaustive deps rule is enabled. Do not suppress it without a documented reason.
{% endhint %}

### B. Tailwind CSS Sorting

We use the **Prettier plugin for Tailwind CSS** (`prettier-plugin-tailwindcss`) to enforce class order.

**Correct:**

```tsx
<div className="flex h-full w-full items-center justify-center bg-gray-50">
```

**Incorrect (Will be auto-fixed):**

```tsx
<div className="bg-gray-50 justify-center w-full flex items-center h-full">
```

### C. Automation

Run the following command to check and fix issues:

```bash
npm run validate
# Or specifically:
npm run lint:fix
npm run format
```

***

## 2. Mobile (`decoyphrase_mobile`)

The Flutter application follows the official Dart style guide with additional strictness for security.

### A. Static Analysis

Our rules are defined in `analysis_options.yaml`. We adhere to `flutter_lints` with additional custom rules.

{% hint style="info" %}
Rigid Typing:

* **Explicit Types**: Always specify types for public members.
  * Good: `final String name = 'Decoy';`
  * Bad: `final name = 'Decoy';` (Allowed only for local variables where type is obvious)
* **Strict Inference**: We disable `implicit-dynamic` types to prevent runtime errors.
{% endhint %}

### B. State Management (GetX)

* **Logic Separation**: UI code (Views) must **never** contain business logic. All logic belongs in the `GetxController`.
* **Bindings**: Always use Bindings for dependency injection. Do not instantiate controllers directly in the View.

### C. Asset Safety

* **No Magic Strings**: Use the generated asset classes (if configured) or defined constants for image paths.
  * Good: `Image.asset(AppAssets.logo)`
  * Bad: `Image.asset('assets/images/logo.png')`

### D. Automation

Run the analyzer locally to catch issues:

```bash
flutter analyze
```
