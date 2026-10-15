# Research status — v0.4.1

NOESIS is in initial experimental development. Current experiments investigate
symbol processing through explicit, developer-supplied rules.

## What has been tested

- Benchmark 001: uppercase ASCII symbol distinction and within-session retention.
- Benchmark 002: all 62 ASCII letters/digits, classification, case distinction,
  complete previous-encounter references, and rejection isolation.
- Separate sessions, lifecycle restrictions, diagnostic traces, and exports.
- Deterministic headless histories of 100, 500, and 1,000 accepted encounters.

Development validation recorded 47 passing automated tests and 15 passing functional
cases. This is a developer-run result, not independent replication. The public
protocols support future black-box checks; source-level inspection and reproduction
of the private automated suite are not currently available from this package.

## What these results do not establish

They do not demonstrate semantic understanding, generalized learning, autonomous
reasoning, consciousness, or adaptive creation of cortexes. Multi-character input,
word recognition, arithmetic, and Benchmark 003 are outside the current work.

## Measurement limitations

Measurements included runtime processing, diagnostics, check storage, and evidence
auditing with memory tracing enabled. They excluded ZIP/report generation. Traced
Python allocations are not total process RAM. Net diagnostic growth is not total
disk writes. Single runs do not establish statistical trends, architectural
scalability, or GUI responsiveness. No performance thresholds were used for success.

Benchmark 002 remains under review. Future capabilities and release availability
will be communicated separately rather than inferred from a roadmap.
