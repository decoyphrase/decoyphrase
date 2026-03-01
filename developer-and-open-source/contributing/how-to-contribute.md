# How to Contribute

### Development Workflow

We use the standard Fork & Pull Request workflow.

1. **Fork** the target repository (Web, Mobile, or Core) to your GitHub account.
2. **Clone** your fork locally:

{% code title="Clone" %}
```bash
git clone https://github.com/decoyphrase/decoyphrase-web.git
cd decoyphrase-web
```
{% endcode %}

3. **Create a Branch**:\
   Always create a new branch for your work. Do not commit directly to `main`.

* For features:

{% code title="Feature branch" %}
```bash
git checkout -b feat/your-feature-name
```
{% endcode %}

* For fixes:

{% code title="Fix branch" %}
```bash
git checkout -b fix/issue-description
```
{% endcode %}

{% hint style="info" %}
Use clear, focused branches for single concerns (one feature or one fix) to simplify reviews.
{% endhint %}

### Commit Message Convention

We adhere strictly to **Conventional Commits**. This allows us to generate changelogs automatically.

**Format:** `<type>: <description>`

| Type       | Description           | Example                                          |
| ---------- | --------------------- | ------------------------------------------------ |
| `feat`     | A new feature         | `feat: add biometric login support`              |
| `fix`      | A bug fix             | `fix: resolve overflow on mobile landscape mode` |
| `docs`     | Documentation changes | `docs: update environment setup guide`           |
| `chore`    | Maintenance tasks     | `chore: upgrade flutter dependencies`            |
| `refactor` | Code restructuring    | `refactor: simplify encryption utility`          |

Rules:

* Use lowercase for the description.
* Do not end the description with a period.
* Keep the first line under 72 characters.



### Testing & Validation

You **must** run tests locally before submitting a Pull Request. CI/CD pipelines will automatically fail if these checks do not pass.

```
{% tab title="Web & Core (`decoyphrase-web`, `decoyphrase`)`" %}
```

Run the unified validation script:

{% code title="Validate (Web & Core)" %}
```bash
# Run all validation checks
npm run validate
```
{% endcode %}

Under the hood, this runs:

* `tsc --noEmit` (TypeScript validation)
* `eslint .` (Linting)
*   `prettier --check .` (Formatting)



For the Flutter application, run the standard test suite:

\{% code title="Flutter tests" %\}

```bash
# Run unit and widget tests
flutter test
```

```
{% endtab %}
```

{% hint style="danger" %}
Do not submit a PR if local validation or tests fail — CI will block merging.
{% endhint %}

### Pull Request Guidelines

When opening a PR, please use the provided template.

* **Link Issues**: Use "Fixes #123" to auto-close related issues.
* **Screenshots**: For UI changes (Web/Mobile), include screenshots or a screen recording.
* **Self-Review**: Review your own code diff before asking for a review.

#### PR Template Snapshot

{% code title="P R Template" %}
```markdown
## Description
Clearly explain what this PR does.

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update

## Verification
- [ ] I have run `npm run validate` (Web) or `flutter test` (Mobile).
- [ ] I have tested this on [Device/Browser].
```
{% endcode %}
