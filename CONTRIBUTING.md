# Contributing to pydnz

Contributions improve this Python client for the DigitalNZ API, including query construction, pagination, response handling, and examples.

## Before you start

Read the [README](README.md), [Makefile](Makefile), and package configuration before changing behavior. Preserve upstream attribution and explain any compatibility change to the existing API.

Search existing issues and pull requests to avoid duplicating work. Describe substantial proposals before implementation, and use repository issue or pull request templates when available. Small corrections can go directly into a focused pull request.

For bug reports, include the affected version or commit, environment, minimal reproduction, expected and actual behavior, and sanitized diagnostics. For feature requests, explain the use case and intended outcome.

## Development and validation

The repository's existing test target is:

```sh
make test
```

It invokes the legacy `setup.py nosetests` path. Check the supported environment and dependency requirements before running it, and record incompatibilities rather than reporting an unexecuted check as passing. The Makefile's historical style targets contain error-suppressing commands, so inspect their diagnostics instead of relying only on a zero exit code.

Use synthetic or sanitized API response fixtures to cover field selection, pagination, facets, geographic filters, and failures without requiring a contributor's live key. Keep dependency or runtime modernization in a separate, justified change. Do not embed keys or private responses in tests, examples, or recorded output.

Update affected documentation and examples alongside behavior changes. Add a focused regression case for a bug fix where executable tests are appropriate. Record checks that were not run and the reason.

## Submitting a pull request

Create a focused branch from the current `master` branch and open a pull request back to it. Keep unrelated formatting, refactoring, and dependency changes separate.

Include:

- The problem, proposed change, and resulting behavior.
- Related issues or existing track references.
- Exact validation commands or inspection steps, results, and limitations.
- Compatibility implications and any data or dependency provenance.

Inspect the complete diff before submission. Required automated checks must pass before merge. Follow the existing repository and account policies; this guide does not introduce a second-person approval requirement or relax existing checks.

## Security and sensitive information

Follow the [account security policy](https://github.com/edithatogo/.github/blob/main/SECURITY.md). Report vulnerabilities privately through GitHub's **Report a vulnerability** option if available. Otherwise request a private reporting contact without disclosing the vulnerability publicly. Keep credentials, personal data, and unredacted logs out of commits, issues, and examples.

## Licensing and conduct

Respect the [existing license](license.txt) and preserve third-party notices. Submit only material you are entitled to contribute, and document unclear permissions before adding third-party content. Follow the [account code of conduct](https://github.com/edithatogo/.github/blob/main/CODE_OF_CONDUCT.md). This guide adds no CLA, mandatory sign-off, or relicensing condition.

## Reference guidance

- [GitHub contributor guidelines](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors)
- [OpenSSF Best Practices criteria](https://www.bestpractices.dev/en/criteria)
