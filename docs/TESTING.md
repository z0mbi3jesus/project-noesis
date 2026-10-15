# NOESIS tester guide

## Availability

Tester downloads are currently on hold. This public documentation package contains
neither the app nor an installer. The protocols below describe how future testers
can participate once a reviewed build and its distribution terms are published.
Support for other operating systems has not been established.

## First session

1. Follow the actual release's installation and launch instructions. Record the
   displayed application version and your operating system.
2. Select a benchmark tab, then choose **Initialize → Start**.
3. Submit one character at a time and select encounters to inspect recorded evidence.
4. Stop when finished and export that benchmark's diagnostics before initializing
   another session. Initialization resets its retained encounter history.

## Protocol 001 — original baseline

Start a fresh Benchmark 001 session. Submit `A`, `B`, `A` individually.

| Encounter | Input | Expected result | Previous matching encounters | Occurrence at encounter |
| --- | --- | --- | --- | --- |
| 1 | A | New | none | 1 |
| 2 | B | New | none | 1 |
| 3 | A | Previously encountered | 1 | 2 |

Lowercase letters and digits remain unsupported in this benchmark.

## Protocol 002 — case distinction

In a fresh Benchmark 002 session, submit `A`, `a`, `A`, `a` individually.
Expected references: `[]`, `[]`, `[1]`, `[2]`. Classification should distinguish
uppercase and lowercase alphabetic characters. No case conversion should occur.

## Protocol 002 — complete repetition references

In another fresh session, submit `A` five times. Expected references:

```text
[]
[1]
[1, 2]
[1, 2, 3]
[1, 2, 3, 4]
```

Occurrence at each encounter should be 1, 2, 3, 4, and 5. This historical count
includes the selected encounter, not future occurrences.

## Protocol 002 — rejected-input isolation

In a fresh session, submit `A`, `!`, `A`, `AB`, `A`. There should be five submissions
but only three retained encounters, with references `[]`, `[1]`, `[1, 2]`.
The two rejections should have distinct submission IDs and expected warnings.
An expected rejection warning is not an application crash.

## Lifecycle and assessment

Pause blocks submissions. Resume preserves history. Stop blocks submissions while
leaving results inspectable. Reinitialization creates a fresh session. Each benchmark
has a separate history. Restart does not restore cognitive history, even though
diagnostic evidence may remain on disk.

Distinguish successful execution, correct individual results, explicit functional
assessment, a stopped session, and formal research acceptance. Stopped does not
automatically mean passed. Manual exports remain unassessed unless checks were
explicitly attached. Do not invent speed requirements when reporting measurements.

## Reporting

Use the bug or experiment-report form. Include exact input order, fresh-session
status, observed evidence, and version. Review exports for personal data before
attaching them. Absence of a detailed crash report does not prove an abrupt
termination did not occur.
