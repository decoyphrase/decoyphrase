---
description: >-
  To maintain maximum security and avoid accidental data exposure or loss,
  please avoid the following common mistakes
---

# Common Mistake

<details>

<summary><strong>Not Protecting the Decoy Phrase Generator</strong></summary>

Failing to protect the Decoy Phrase Generator on your device is a serious security risk.\
The Generator should always be protected using at least biometric authentication or a PIN built into the application.

{% hint style="danger" %}
When you create a Mapping Maker project, the system automatically saves your progress to simplify the creation of Decoy Text and Mapping Files. These projects contain your sensitive data. Without proper device-level protection, anyone with access to your device may access your sensitive data.
{% endhint %}

</details>

<details>

<summary><strong>Mixxing Decoy Patterns in Final Mapping</strong></summary>

A common mistake is using a custom language or pattern that is not supported by Auto Fill, but failing to apply the same language and pattern consistently when completing the Final Mapping.

If the Final Mapping is later found or inspected independently, inconsistent decoy languages or patterns can create detectable or suspicious structures.

To avoid this, ensure that all remaining empty decoy slots in the Final Mapping are filled using the same language and pattern as the existing decoy values. For faster and more consistent input, use the **Bulk Edit** feature with the target set to **Final** to complete the remaining decoy columns.

</details>

<details>

<summary><strong>Not Deleting Mapping Maker Projects After Completion</strong></summary>

Leaving Mapping Maker projects on your device after finishing is strongly discouraged, especially when using a non-personal device.

{% hint style="danger" %}
Mapping Maker projects store sensitive information used to reconstruct your original text. If these projects remain on the device, they can become a potential source of data leakage.
{% endhint %}

</details>

<details>

<summary><strong>Not Clearing Browser Cache When Using a Non-Personal Device</strong></summary>

Always clear your browser cache or use Incognito / Private Mode when accessing Permanent Storage on a shared or non-personal device.

{% hint style="warning" %}
Browsers may automatically save usernames, passwords, or session data locally. This can unintentionally expose your Decoy Phrase Permanent Storage credentials to other users of the same device.
{% endhint %}

</details>

<details>

<summary><strong>Storing Decoy Text and Mapping File in the Same Location</strong></summary>

A critical mistake is storing the Decoy Text and its corresponding Mapping File in the same location, including the same permanent storage.

Both files must be stored in separate locations to avoid a single point of failure. If only one of the files is found, it should remain completely useless.

**For example:**

* The **Decoy Text** may be stored as plain text (e.g., notes, social media drafts, or private text storage).
* The **Mapping File** (JSON format) should be stored securely on a device or protected storage medium.

When using **permanent storage**, it is strongly recommended to enable **multi-password management**. This adds an additional security layer by ensuring that access to the stored file requires more than a single password, reducing the risk of unauthorized access even if one credential is compromised.

Permanent storage should be treated as a durability layer, not a trust layer. Separation and layered access controls remain essential, as security failures often result from human error rather than flaws in the system architecture itself.

</details>

<details>

<summary><strong>Not Saving the Mapping File with the <code>.json</code> Extension</strong></summary>

Always ensure that your Mapping File is saved with the `.json` file extension.

{% hint style="warning" %}
If the file name does not end with `.json`, the Mapping File may not function correctly during recovery.
{% endhint %}

This commonly happens when users rename the file or manually change the file name in the **Save Location dialog used when saving the Mapping File directly from the generator**, causing the system to fail to recognize the file format.

</details>
