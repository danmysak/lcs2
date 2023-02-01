# lcs
`lcs` is a Python package for computing longest common subsequences.

## Installation
```
pip install lcs
```

## Reference
The package provides the following functions:

| Function      | Signature                                           | Result                           |
|:--------------|:----------------------------------------------------|:---------------------------------|
| `lcs`         | `Iterable[T], Iterable[T] -> list[T]`               | Longest common subsequence (LCS) |
| `lcs_indices` | `Iterable[T], Iterable[T] -> list[tuple[int, int]]` | Indices of the LCS               |
| `lcs_length`  | `Iterable[T], Iterable[T] -> int`                   | Length of the LCS                |

Calling `lcs_length(a, b)` is somewhat more efficient than simply using `len(lcs(a, b))`.

## Sample Usage
```python
from lcs import lcs, lcs_indices, lcs_length

a = 'Hello, world!'
b = 'Foobar'
print(lcs(a, b))  # ['o', 'o', 'r']
print(lcs_indices(a, b))  # [(4, 1), (8, 2), (9, 5)]
print(lcs_length(a, b))  # 3
```
