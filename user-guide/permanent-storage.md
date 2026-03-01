# Permanent Storage

## How to Use Permanent Storage

{% stepper %}
{% step %}
### Create a Decoy Phrase Account

Create your Decoy Phrase account to access the Permanent Storage feature.\
This account is only used to manage your uploads and storage references.

{% hint style="danger" %}
We do not recommend and never advise storing any sensitive data, seed phrases, or original texts on Decoy Phrase Permanent Storage
{% endhint %}
{% endstep %}

{% step %}
### Create a Secondary Password using [Multi-Password Management](../products-and-features/permanent-storage/multi-password-management.md)

Set up a secondary password using Multi-Password Management to create multiple secure vaults, each protected by a different password.

{% hint style="info" %}
Each vault functions as an independent storage space with its own access credentials.\
This separation allows you to isolate different decoy sets, mapping files, or security levels within one account.&#x20;
{% endhint %}
{% endstep %}

{% step %}
### Upload Your Decoy Text and Mapping File

Upload your Decoy Text and Mapping File separately, each into a different vault protected by a different password. Store one file under the Primary Password and the other under the Secondary Password.

{% hint style="info" %}
The Decoy Text and Mapping File are intentionally stored in separate vaults to prevent single-point of failure. Each vault is protected by a different password and access layer.
{% endhint %}

{% hint style="success" %}
Without access to both vaults and the correct passwords, the data remains completely useless. Only by combining the correct Decoy Text, Mapping File, and corresponding passwords can the original sensitive text be recovered.
{% endhint %}
{% endstep %}
{% endstepper %}
