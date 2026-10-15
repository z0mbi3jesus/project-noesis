# Results and limitations

## Development validation — v0.4.1

- 47 automated tests passed, including Benchmark 001 regression.
- All 15 functional cases passed, including all 62 supported symbols and the
  100-, 500-, and 1,000-encounter histories.
- Complete prior-reference lists and recorded processing contributions were checked.
- No unexpected processing errors or export inconsistencies were found in that run.
  Unsupported-input cases intentionally produced rejection warnings.

These are developer-run observations, not independent scientific validation.
The implementation and private automated suite are not published, limiting external
source review and replication. Public protocols describe black-box checks for when
approved tester builds become available; downloads remain on hold.

## Single-run performance observations

| Accepted encounters | Elapsed seconds | CPU seconds | Current / peak traced Python MiB | Net diagnostic growth MiB |
| --- | --- | --- | --- | --- |
| 100 | 2.872 | 0.859 | 0.61 / 1.55 | 0.62 |
| 500 | 16.196 | 4.188 | 3.23 / 7.99 | 3.10 |
| 1,000 | 35.065 | 10.422 | 7.04 / 16.57 | 5.34 |

MiB means 1,048,576 bytes. The cases ran sequentially on one development machine.
Measurements included initialization, submissions, functional checks, evidence
auditing, diagnostic I/O, and Stop. They excluded ZIP/report generation and file-size
enumeration. The platform context was Windows with Python 3.13.3; detailed hardware
configuration was not captured in the published summary.

Memory tracing adds overhead and does not measure total process RAM or SQLite
native allocations. Diagnostic growth is net retained logical size, not total
disk writes; log rotation affects it. These are not isolated cortex timings,
speed requirements, statistical trends, or GUI responsiveness measurements.

Long cases cycle across the 62-symbol set, rather than repeating one symbol 1,000
times. That worst-case distribution has not been measured here. Full-history scans
and accumulated references can grow quadratically. No architectural optimization
was made in response to these preliminary observations.

## What remains unestablished

Programmed symbol handling is not proof of learned language, semantics, autonomous
reasoning, adaptive cognition, consciousness, or the entire theoretical CAC
architecture. Functional case success, stopped execution, and formal research
acceptance are different. Benchmark 002 still awaits project review.
