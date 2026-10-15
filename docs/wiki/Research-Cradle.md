# Research Cradle

The cradle is a replaceable control and observation environment. Essential symbol
processing resides outside the interface. This separation is intended to support
future environments without making cognition depend on particular screens.

## Working with a session

The current app provides Initialize, Start, Pause, Resume, and Stop controls.

| Control | Current behavior |
| --- | --- |
| Initialize | Creates a fresh session and empty encounter history for the selected benchmark |
| Start | Enables submissions in that session |
| Pause | Blocks new submissions while retaining history |
| Resume | Enables input again without resetting history |
| Stop | Blocks input while leaving results inspectable and exportable |

Benchmark tabs have independent sessions, histories, and selections. Shared controls
target the last selected benchmark; diagnostic tabs do not silently switch that
target. Closing the app stops both sessions. Restart does not restore cognitive
history. These independent experiments are not a dynamically multiplied cortex.

## Observation tools

- Encounter history shows symbols, classifications, results, earlier matches, and
  occurrence at the selected encounter.
- The Processing Inspector shows actual recorded phases and contributions.
- All submissions includes rejected, blocked, failed, and incomplete attempts.
- Component cards show last recorded activity, not simulated ongoing thinking.
- Events support component, category, benchmark, and text filters.

Diagnostics separate routine events, warnings/recoverable failures, and detailed
reports for unexpected application-ending crashes. Hard termination or power loss
may prevent a crash report from being written.

## Exports

Export before reinitializing. The structured report concerns the selected session,
but supporting log files and crash reports may contain other sessions. Review the
whole ZIP for personal information before sharing it. A diagnostic journal may
persist even when cognitive memory resets.

Session execution, functional correctness, and formal benchmark assessment are
separate. A stopped session is not automatically a successful experiment.

Tester downloads remain on hold. See the
[tester guide](https://github.com/z0mbi3jesus/project-noesis/blob/main/docs/TESTING.md)
and [privacy notice](https://github.com/z0mbi3jesus/project-noesis/blob/main/PRIVACY.md).
