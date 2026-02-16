# .github Shared Workflows

This repository hosts top-level workflow templates used across the `vm2` set of projects.

## Contents

- `workflow-templates/` – reusable CI/CD workflow templates and configuration, consumed by downstream repositories:
  - **CI** – Continuous Integration: build, test, benchmark, and package verification. Triggered on pull requests and pushes
    to any branch, and on manual dispatch. To suppress a CI run, include the fragment `[skip ci]` in the commit message.
  - **Prerelease** – Pre-release workflow: pre-release tagging and versioning, changelog, NuGet packaging, and publishing
    pre-release versions. Triggered on pull request merges to main or on manual dispatch.
  - **Release** – Release workflow: changelog, NuGet packaging, and publishing release versions. Triggered on manual dispatch
    only from the main branch. The workflow computes the SemVer version from the commits since the previous release
    and includes a manual approval step to ensure releases are intentional and controlled.
  - **ClearCache** – Clears workflow caches to ensure fresh builds. Triggered manually.
  - **dependabot** – Dependabot configuration for automated dependency updates. Triggered on a schedule.

## Usage

- Instantiate workflow templates from this repository in consuming repos using GitHub Actions UI
  (Actions tab → New workflow → Set up a workflow yourself → Choose "Use a workflow from another repository") and specify this
  repository as the source.
- Adjust Customization Points marked with `*TODO*` inside each template.

## Support

- Issues and updates are managed centrally in this repo. Align changes with vm2.DevOps reusable workflows when updating templates.
