# Privacy and experimental data

Effective: October 15, 2026

## Scope

This notice describes the current NOESIS Research Cradle v0.4.1 and the public
GitHub research hub. Tester downloads remain on hold. Future releases may have
different capabilities and will require an updated notice before distribution.

## Local application

The current application has no network client, telemetry, automatic upload, or
external AI service integration. Processing and diagnostic storage are local.
This describes application behavior, not an operating-system sandbox or what
other software on your computer may do.

Local records can include submitted text, accepted symbols, rejected submissions,
classifications, encounter and submission identifiers, processing phases,
timestamps, application version, lifecycle transitions, and tester-entered issues.
Crash reports can contain exception details, stack traces, and local file paths.
Report metadata includes Python version and operating-system family.

Routine and warning logs rotate. The research journal and crash reports remain
until manually removed; resetting a cognitive session does not delete diagnostic
evidence. Session memory and diagnostic retention are different. Close the app
before managing its configured data directory, and preserve anything needed for
an experiment before deleting it.

## Exports and sharing

Exports are created only when requested. They are not uploaded automatically.
The structured experiment report concerns the selected session, but supporting
rotating logs and crash reports in the same ZIP can include other sessions.

Review the entire archive before sharing it. Remove personal text, credentials,
usernames/paths, and unrelated records; explain redactions that affect an experiment.
Do not submit health, financial, identity, or other sensitive personal information
as test data or in public attachments.

## GitHub participation

Public issues, pull requests, comments, and attachments can be viewed and copied
by others. GitHub also processes account and platform data under its own
[privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).
The current project does not add a separate analytics service to this repository.

For a privacy concern, request a private contact method from the repository
maintainer without repeating the sensitive content in a public issue. The maintainer
can review project-controlled material, but cannot promise deletion from third-party
copies, forks, caches, or GitHub's own records. Use GitHub's reporting mechanisms
where the platform itself must act.
