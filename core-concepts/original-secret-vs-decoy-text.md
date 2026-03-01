# Original Secret vs Decoy Text

## Definitions

1. **Original Secret**

The Original Secret is the original, highly sensitive data, such as a seed phrase, private key, password, recovery code, or other critical information. This data has real value and can be used directly to access assets, accounts, or systems. If the Original Secret is exposed, the consequences are typically permanent and irreversible.

2. **Decoy Text**

Decoy Text is the transformed output of the Original Secret, converted into ordinary text that looks normal and non-suspicious. Decoy Text holds no direct value, cannot be used to access anything, and has no security meaning on its own. Without the mapping file, Decoy Text is simply meaningless text from a security perspective.

## Key differences

| Aspect                | Original Secret                             | Decoy Text                           |
| --------------------- | ------------------------------------------- | ------------------------------------ |
| **Value**             | Extremely high                              | No value                             |
| **Function**          | Directly usable                             | Not usable                           |
| **Sensitivity Level** | Highly sensitive                            | Not sensitive                        |
| **Risk if Exposed**   | Loss of access / assets                     | No impact                            |
| **Form**              | Specific patterns (seed phrase, keys, etc.) | Normal, free-form text               |
| **Storage**           | Must be strictly limited                    | Safe to store anywhere               |
| **Dependency**        | Stands alone                                | Meaningless without the mapping file |

The Original Secret is the real key, while Decoy Text is only a disguise. Decoy Phrase security does not rely on hiding the Original Secret, but on removing the Original Secret from storage entirely.
