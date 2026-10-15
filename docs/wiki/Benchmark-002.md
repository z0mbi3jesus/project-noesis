# Benchmark 002 — Expanded Symbol Recognition and Retention

## Domain

Each submission contains exactly one of 62 ASCII symbols:

| Classification | Symbols |
| --- | --- |
| Uppercase alphabetic | A–Z |
| Lowercase alphabetic | a–z |
| Numeric digit | 0–9 |

Original characters are preserved. `A` and `a` have distinct histories; `7` remains
a symbol rather than an arithmetic value. Words, expressions, punctuation,
whitespace, padded characters, and non-ASCII lookalikes are unsupported.

## Reference protocols

Use a fresh Benchmark 002 session for each row and submit characters individually.

| Inputs | Expected complete prior references |
| --- | --- |
| A, a, A, a | [], [], [1], [2] |
| A, A, A, A, A | [], [1], [1,2], [1,2,3], [1,2,3,4] |
| A, b, 7, A, b, 7, A, b, 7 | [], [], [], [1], [2], [3], [1,4], [2,5], [3,6] |
| 1, 2, 3, 1, 2, 3, 1 | [], [], [], [1], [2], [3], [1,4] |
| A, !, A, AB, A | Three retained encounters: [], [1], [1,2]; two rejected submissions |

Occurrence at an encounter is the number of earlier exact matches plus one. It is
not the encounter's overall position or the symbol's final total in a later history.

## Extended validation

The development runner includes all-symbol coverage, the above deeper-history
checks, rejection isolation, and Benchmark 001 regression reference behavior.
Optional longer cases contain 100, 500, and 1,000 accepted encounters.

Those longer inputs use this fixed ordered set:

```text
ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789
```

For zero-based input index i, select symbol index `(i * 17) % 62`. This specifies
the experimental dataset independently of the withheld implementation. The cases
check complete matching-reference lists and diagnostic evidence, not only a repeat
boolean. The full private automated regression suite is a separate check.

## Interpretation

Current results concern classification, exact recognition, and retention. They do
not establish relationships between cases of a letter, alphabetical ordering,
mathematics, sequence recognition, semantic understanding, or generalized learning.
Benchmark 002 remains under review; Benchmark 003 has not started.

See [results and limitations](https://github.com/z0mbi3jesus/project-noesis/wiki/Results-and-Limitations).
