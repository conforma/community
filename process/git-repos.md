# Git Repositories

The [Conforma](https://github.com/conforma) GitHub organization hosts all the
git repositories that make up the Conforma ecosystem. This document describes the
managing processes for these git repositories.

## Repository Requirements

All git repositories within the organization must meet the following requirements:

1. Use the license `Apache License 2.0`. The full license must be included in a file named `LICENSE`
   at the root of the repository.
1. Include a `README.md` that introduces the repository and, if needed, references additional
   documentation.
1. Setup execution of [OpenSSF Scorecard](https://github.com/ossf/scorecard), see
   [example](https://github.com/enterprise-contract/ec-cli/blob/main/.github/workflows/scorecard.yml).
1. Setup automatic dependency updates with either
   [dependabot](https://docs.github.com/en/code-security/dependabot) or
   [renovatebot](https://docs.renovatebot.com/). Depending on the technology stack in the
   repository, both of these may be needed. See
   [dependabot](https://github.com/enterprise-contract/ec-policies/blob/main/.github/dependabot.yml)
   example and
   [renovatebot](https://github.com/enterprise-contract/golden-container/blob/main/renovate.json)
   example.
1. Setup branch protection for the default branch, usually `main`. At a bare minimum "require a pull
   request before merging."
1. Access must be granted to a [team](https://github.com/orgs/conforma/teams), not to
   an individual.

The [.github](https://github.com/conforma/.github) repository contains common files that
apply to all repositories within the organization, i.e. `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`,
and `SECURITY.md`. These should be excluded from other repositories unless there is a strong reason
to overwrite those policies for a particular repository.

The [.github](https://github.com/conforma/.github) repository also defines required
workflows across all the repositories in the organization.

