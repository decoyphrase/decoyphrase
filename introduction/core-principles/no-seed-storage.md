# No Seed Storage

Both [**Decoy Phrase Generator**](../../products-and-features/decoy-phrase-generator/) and [**Permanent Storage**](../../products-and-features/permanent-storage/) are designed to allow users to protect sensitive data—such as seed phrases, digital keys, or other confidential information—**without ever exposing the original data to Decoy Phrase servers**.

#### Decoy Phrase Generator (Offline)

* Operates **entirely offline**, ensuring that sensitive inputs are never transmitted or stored externally.
* Users transform their seed phrases, digital keys, or other confidential data into decoy text locally.
* The original sensitive data **remains private** and is never uploaded or exposed to any online system.

#### Permanent Storage

* Does **not require users to store sensitive data directly**. Instead, users can store:
  * **File mappings**, or
  * **File mappings plus decoy text**,\
    while leveraging the offline generator for secure transformation.
* Security is further enhanced through [**Multi-Password Management**](../../how-decoy-phrase-works.md#c.-multi-password-management-in-permanent-storage), which provides **two separate storage spaces under a single account** to isolate mapping file from decoy text.

#### Key Benefits

1. Sensitive data is **never stored in plaintext** on any server.
2. Users maintain full **control over original data**.
3. Decoy and mapping structures enable secure retrieval while minimizing exposure.

**In summary:** The combination of offline transformation and multi-layered storage ensures maximum privacy and security while allowing users to safely manage seed phrases, digital keys, and other sensitive information.

## Why this removes attack vectors

Most digital security attacks focus on obtaining the original data—seed phrases, private keys, or passwords—whether through server breaches, database leaks, malware, or abuse of internal access.

With the No Seed Storage principle, Decoy Phrase eliminates the primary attack target from the outset:

* There is no database of seed phrases or secrets to hack
* There is no vault containing original data, even in encrypted form
* There is no backend or administrator with access to user secrets
* There is no high-value single point of failure

Because the original seed phrase never exists within the system, even if file leaks occur, permanent storage is accessed, or public metadata is exposed, there is no information that can be used to take over user assets.

{% hint style="success" %}
This approach shifts the security model from **“protecting valuable data”** to **“eliminating the existence of valuable data.”**
{% endhint %}

## Comparison with password managers

| Aspect                | Traditional Password Managers                                               | Decoy Phrase                                                                |
| --------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| Original data storage | Stores original passwords or secrets inside a vault                         | Does not store seed phrases or original sensitive data at all               |
| System architecture   | Typically relies on a backend and cloud synchronization                     | Does not rely on servers or a backend                                       |
| Security model        | Depends on vault encryption and a master password                           | Has no vault containing secrets that the system can decrypt                 |
| Attack target value   | High-value target because it contains original data                         | Has no high-value objects that can be stolen                                |
| Impact of a breach    | If the vault or master password is compromised, all contents may be exposed | Leaking a single component is never sufficient to recover the original data |
| Stored data           | Encrypted original secrets                                                  | Separate decoy text and mapping file                                        |
