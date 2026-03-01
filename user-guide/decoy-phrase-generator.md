# Decoy Phrase Generator

<p align="center"><a href="https://www.youtube.com/watch?v=d07MDSrPE1E&#x26;t=1s"><img src="https://docs.decoyphrase.com/~gitbook/image?url=https%3A%2F%2F2072286647-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FaV4lmBtlwYvsQLPxi2KC%252Fuploads%252FUC8Uuefm81wiT60OePUQ%252Fyoutub11.png%3Falt%3Dmedia%26token%3D183da3c9-3db2-4f6f-800d-d20ba411d700&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=3c8d8cd3&#x26;sv=2" alt="Decoy Phrase – Secure Your Keys"></a>                                   <a href="https://www.youtube.com/watch?v=9w2Pb9w6hkU&#x26;t=5s"><img src="https://docs.decoyphrase.com/~gitbook/image?url=https%3A%2F%2F2072286647-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FaV4lmBtlwYvsQLPxi2KC%252Fuploads%252FYBnt6cf2fgwr34qChzAT%252Fyoutube13.png%3Falt%3Dmedia%26token%3D77a47ac1-318a-4bd3-b9de-080853b74ea0&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=70e5361a&#x26;sv=2" alt="Decoy Phrase – Secure Your Keys"></a></p>

Inside the Decoy Phrase Generator, there are two main components: **Mapping Maker** and **Text Generator.** Both have different function

| Mapping Maker                                                                                                 | Text Generator                                                              |
| ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| Transform sensitive text into decoy text. _(such as seed phrases, passwords, private keys, and similar data)_ | Recover the original sensitive text                                         |
| Create decoy text and generate the Mapping File                                                               | Recover or test decoy text to verify and preview the transformation results |

## How to Use Mapping Maker

{% stepper %}
{% step %}
### Enter Your Sensitive Text in the ASCII Text Field

Place your seed phrase, password, private key, or other sensitive text into the **ASCII Text** field.
{% endstep %}

{% step %}
### Click “Generate Draft Mapping”

Click the **“Generate Draft Mapping”** button to display the Draft Mapping table.
{% endstep %}

{% step %}
### Fill in the Decoy Text Column in Draft Mapping

Fill the decoy text column in the Draft Mapping with the characters or words you want.

{% hint style="info" %}
* To make this easier, use the **“Bulk Edit”** feature, then enter your characters or words horizontally in the bulk field according to the number of ASCII columns shown in the draft mapping.
* The draft mapping is arranged sequentially based on the ASCII characters found in the entered sensitive text, making it easier for users to fill in decoy values.
* At this stage, you can already view and download your decoy text in decoy preview, which will be used as one of the required elements to recover your sensitive text later.
{% endhint %}
{% endstep %}

{% step %}
### Fill in the Decoy Text Column in Final Mapping

After completing the Draft Mapping, it will automatically be transferred into the Final Mapping and filled according to the system order. Your task is to fill in the remaining empty decoy text columns.

{% hint style="info" %}
Decoy text entered in the Draft Mapping is automatically mapped into the Final Mapping according to the standard ASCII order:

* Uppercase letters (A–Z)
* Lowercase letters (a–z)
* Numbers
* Spaces
* Symbols
{% endhint %}

{% hint style="warning" %}
You may use **Auto Fill** if the decoy text you entered in Draft Mapping consists of English words and random characters (1–4 characters).
{% endhint %}

{% hint style="danger" %}
**If you used a different language or pattern that is not available in the Auto Fill options**, you must manually fill the Final Mapping using the same language and pattern. This ensures that if the Final Mapping is found independently, it does not form a different or suspicious pattern.

To make this easier, use the **“Bulk Edit”** feature by selecting the target **“Final”** to quickly fill the remaining empty decoy columns.
{% endhint %}
{% endstep %}

{% step %}
### Download Final Mapping and Decoy Text

Download the **Final Mapping** and **Decoy Text** by clicking the download icon.&#x20;

{% hint style="danger" %}
Store both files in separate locations for long-term storage and easy access. For permanent storage, use **Decoy Phrase Permanent Storage**.
{% endhint %}
{% endstep %}
{% endstepper %}

## How to Recover Your Original Sensitive Text

{% stepper %}
{% step %}
### Upload Your Mapping File

Upload the corresponding **Mapping File** that was generated when you created the decoy text.

{% hint style="info" %}
This file contains the transformation rules required to reconstruct your original sensitive text.
{% endhint %}

{% hint style="warning" %}
Without the correct mapping file, recovery is not possible.
{% endhint %}
{% endstep %}

{% step %}
### Select Decoy → ASCII Mode

Choose the **Decoy → ASCII** mode to indicate that you are recovering sensitive text from a decoy text using an ASCII-based mapping.

{% hint style="info" %}
This mode tells the system to interpret the decoy text according to the ASCII mapping rules.
{% endhint %}
{% endstep %}

{% step %}
### Enter Your Decoy Text

Paste or type your generated **Decoy Text** into the input field.

{% hint style="warning" %}
Make sure the decoy text matches exactly the text generated during the mapping process, as any difference may prevent correct recovery.
{% endhint %}
{% endstep %}

{% step %}
### Click “Generate Result”

Click the **“Generate Result”** button to start the recovery process.

{% hint style="info" %}
The system will reconstruct and display your original sensitive text based on the uploaded mapping file and the provided decoy text.
{% endhint %}
{% endstep %}
{% endstepper %}

