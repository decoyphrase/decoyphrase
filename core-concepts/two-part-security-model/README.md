# Two-Part Security Model

## Model overview

The Two-Part Security Model is a security approach that splits sensitive information into two fully independent components.

In Decoy Phrase, these two components are:

1. **Decoy Text** — ordinary-looking text that appears normal and holds no security value
2. **Mapping File** — a private file that serves as the only key to recover the original data

The Original Secret is never stored in its complete form. System security does not rely on a single storage point, but on the requirement that both components must be present at the same time for recovery to be possible.

## Security assumptions

This model is built on several core assumptions:

* **One part alone is insufficient**

> Decoy Text without the Mapping File is meaningless. The Mapping File without the Decoy Text is also unusable.

* **The two parts are stored separately**

> Separation across locations, media, or access contexts makes full compromise extremely difficult.

* **No central point of trust**

> There is no server, backend, or third party holding the recovery key.

* **Processing is performed offline**

> The risk of network-based leakage is minimized because no sensitive data is transmitted outside the device.

This model assumes that attackers are rarely able to access two locations, two contexts, and two different forms of data at the same time.

## Failure scenarios

The Two-Part Security Model is designed to eliminate a single point of failure, but it still has limitations that must be clearly understood:

* **Decoy Text is exposed or known to others**

> No failure occurs. Decoy Text contains no sensitive information and cannot be used for anything without the corresponding Mapping File.

* **Mapping File is exposed without the Decoy Text**

> No failure occurs. The Mapping File has no meaning or function without the correct Decoy Text.

* **One part is lost (Decoy Text or Mapping File)**

> Recovery failure occurs. The Original Secret can never be recovered. This is a deliberate design consequence, not a system weakness.

* **Decoy Text and Mapping File are exposed together**

> Total failure occurs. The Original Secret can be fully recovered. This is the only condition under which security collapses.

* **User error (human error)**

> For example, storing both parts in the same location, using the same password, or sharing both with the same party. This risk comes from usage practices, not from the security model itself.

The system fails only when two components that are meant to remain separate are brought together. As long as this separation is maintained, practical failure is extremely unlikely.
