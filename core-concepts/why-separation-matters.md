# Why Separation Matters

## Threat analysis

Most security failures occur because the entire secret exists in a single form and a single location. Once a file or system is compromised, the real value is immediately exposed.

The Two-Part Security Model avoids this by separating:

1. [**Decoy Text**](two-part-security-model/decoy-text.md) — ordinary text with no value
2. [**Mapping File**](two-part-security-model/mapping-file.md) — a structured technical file that contains no sensitive data and is meaningless on its own

No single component is valuable or dangerous by itself. Value only emerges when both parts are combined in the correct context.

## Single-point-of-failure comparison

In traditional systems:

* One seed phrase, one password, one backup = one point of failure
* A single leak results in total compromise
* Data is directly usable

In the separation model:

* Decoy Text has no value if exposed
* The Mapping File remains meaningless without the corresponding Decoy Text
* There is no single artifact that can be abused
* Failure occurs only when two separate artifacts are deliberately combined

This model eliminates single points of failure not by hiding data, but by removing value from each component individually.

> Mapping File → the logic> \
> Decoy Text → the sequence
>
> Logic without sequence cannot reconstruct anything.> \
> Sequence without logic reveals nothing.
