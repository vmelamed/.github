# .github Shared Workflows

This repository hosts organization-level workflow templates used across vm2 projects.

## Contents

- `workflow-templates/` – reusable CI/CD workflows,  consumed by downstream repositories:
  - CI - Continuous Integration: build, test, and benchmarks. Triggered on pull requests and pushes to main
  - Prerelease - Pre-release workflow: prerelease tagging and versioning, changelog, NuGet packaging, and publishing pre-release versions. Triggered on pull requests to main or on manual dispatch
  - Release - Release workflow: changelog, NuGet packaging, and publishing release versions. Triggered on manual tagging with a release version, e.g. v1.2.3 of main or on manual dispatch
  - ClearCache - Clears workflow caches to ensure fresh builds. Triggered manually
  - dependabot - Automates dependency updates. Triggered on a schedule or manually

## Usage

- Instantiate workflow templates from this repository in consuming repos using GitHub Actions UI (Actions tab → New workflow → Set up a workflow yourself → Choose "Use a workflow from another repository") and specify this repository as the source.
- Adjust Customization Points marked with `*TODO*` inside each template.

## Support

- Issues and updates are managed centrally in this repo. Align changes with vm2.DevOps reusable workflows when updating templates.
