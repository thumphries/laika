# laika

Laika is an extremely simple CI system. It is intended for use by
individuals or small teams. It is currently very tightly coupled to
Github and AWS, making use of their very convenient SQS integration.

The plan, should it ever actually come to fruition:

- Reads Github messages off SQS
- Checks if it should build the project (git ref whitelist to exclude forks and PRs)
- Clones the repository into a clean temporary directory
- Builds the project according to shell scripts inside the repository
- Provides helper executables to set Github build status
- Provides helper scripts to publish versioned artifacts to S3

Unfortunately, this is just a README. I badly need a system like this,
and each step is relatively simple, so hopefully I grind it out. If I
don't and you do implement such a system, please do let me know!