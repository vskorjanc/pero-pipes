# File naming convention
Measurement names generally consist of three parts:
1. Substrate name
2. Pixel name (optional)
3. Other

The substrate and the pixel name are separated by an underscore. The rest of the file name is delimited by a dot. This allows you to add **additional info** relevant only for you in the file name by separating it from the first part by a dot. Substrate names should therefore **not contain** an **underscore** or a **dot**.

## ✔ Valid file names:

| name                         | substrate  | pixel                                                             |
| ---------------------------- | ---------- | ----------------------------------------------------------------- |
| `VikA01_a.txt`               | `VikA01`   | `a`                                                               |
| `VikA01_a.extra-bromide.txt` | `VikA01`   | `a`                                                               |
| `VikA01.TQL`                 | `VikA01`   |                                                                   |
| `Vik-B-01_1.txt`             | `Vik-A-01` | `1`^[Numbers are used for marking different dots measured for PL] |

## ❌ Invalid file names
- `Vik.A.01_a.txt`
- `Vik_A_01.txt`
---
## How does the script work?
Everything up to the first dot is considered as metadata, while the rest is disregarded. If the metadata string contains an underscore, it is split into two parts around the underscore. The first part of the string is the substrate name, while the second is the pixel. If there is no underscore, the pixel field is left empty.