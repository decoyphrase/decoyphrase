# Text Generator

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

The **Text Generator** is a component within Decoy Phrase Generator that is used to perform **data recovery**. Through the Text Generator, users can:

* Restore original data such as **seed phrases, passwords, or other sensitive information**
* Retrieve **Decoy Text** from original data (typically for testing or verification purposes)

All processes in the Text Generator run **entirely on the user’s device (offline)** and do not involve servers, cloud services, or third parties.

## Components in the Text Generator

#### 1. Generate Modes

The Text Generator provides two generate options:

{% tabs %}
{% tab title="1. Decoy → ASCII" %}
This process is used to restore the **original data**, such as seed phrases, passwords, or other sensitive information.

* This is the **primary recovery process**
* Requires:
  * Decoy Text
  * Mapping File
{% endtab %}

{% tab title="2. ASCII → Decoy" %}
This process is used to generate or retrieve **Decoy Text** from original data (ASCII Text).

* Commonly used for **testing, validation, or mapping verification**
* Requires:
  * ASCII Text
  * Mapping File
{% endtab %}
{% endtabs %}

#### 2. ASCII Text Field

{% hint style="info" %}
**This field is used to:**

* Display or input **original data** (seed phrase, password, or sensitive text)
* The behavior of this field depends on the selected generate mode
{% endhint %}

#### 3. Decoy Text Field

{% hint style="info" %}
**This field is used to:**

* Display or input **Decoy Text**
* The behavior of this field also depends on the selected generate mode
{% endhint %}

#### 4. Update Mapping

Used to **upload the Mapping File** that will be applied during the generate or recovery process.

#### 5. Current Mapping

Displays basic information about the currently active Mapping File.

## How the Text Generator Works

#### 1. Original Data Recovery (Decoy → ASCII)

To recover the ASCII Text (seed phrase, password, or original sensitive data), **two mandatory components** are required:

* Decoy Text
* Mapping File

Without either component, the Text Generator **cannot** restore the original data.

{% hint style="info" %}
**Process:**

* The generator reads the Decoy Text **token by token**
* Each token is matched against the Mapping File
* The order of the Decoy Text is critical, as the mapping is created sequentially
* Through this process, the original ASCII Text is reconstructed accurately
{% endhint %}

***

#### 2. Retrieving Decoy Text (ASCII → Decoy)

To retrieve or generate Decoy Text (typically for testing purposes), **two components** are also required:

* ASCII Text
* Mapping File

{% hint style="info" %}
**Process:**

* The generator reads each character of the ASCII Text
* Each character is matched with its corresponding entry in the Mapping File
* The output is assembled following the **original ASCII Text order**
* Through this process, the Decoy Text is generated
{% endhint %}

{% hint style="warning" %}
Important Notes

* The Text Generator **does not store any data**
* All operations are performed **locally and offline**
* Without the correct combination of Decoy Text and Mapping File, recovery is **technically impossible**
* This design keeps the Text Generator secure and consistent with the **Zero Knowledge** and **No Seed Storage** principles
{% endhint %}
