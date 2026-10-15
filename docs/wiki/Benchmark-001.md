# Benchmark 001 — Elementary Symbol Recognition

## Purpose and input

Investigate symbol distinction, exact comparison, and within-session retention.
Each submission must be exactly one uppercase ASCII letter A–Z. No trimming or
case conversion occurs. Lowercase, digits, punctuation, whitespace, and longer
strings are unsupported.

## Reference experiment

Initialize and start a fresh Benchmark 001 session, then submit individually:

| Encounter | Input | Expected result | All previous matches | Occurrence at encounter |
| --- | --- | --- | --- | --- |
| 1 | A | New | none | 1 |
| 2 | B | New | none | 1 |
| 3 | A | Previously encountered | 1 | 2 |

Verify the ordered history and inspect the recorded language identification,
cognitive comparison, and CAC retention contribution. Do not infer unrecorded
internal reasoning from the final result.

## Boundaries

A submission is not an individual keyboard press. Rejected submissions do not
become accepted encounters, although they retain diagnostic submission identities.
Each new initialization starts fresh cognitive history. Stop preserves results for
inspection but does not certify benchmark success.

The original uppercase-only rules remain in place alongside Benchmark 002.
Functional success demonstrates explicit symbol processing and retention, not
learned meanings or intelligence.
