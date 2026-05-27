# Chainguard Actions Demo

This is a repository to be used to demo Chainguard Actions. It leverages actions from `chainguard-actions` and is configured to run Dependabot weekly to update the actions' hashes. Please visit [`DEMO.md`](DEMO.md) for the steps.

## Actions in Repo
Current actions are `chainguard-actions/sigstore-cosign-installer` and `chainguard-actions/iamjasonh-setup-crane` since these are publicly accesible. Workflow installs cosign and crane, and Dependabot updates by SHA.

## Prerequisites

- Entitle your organization by running the following command: `chainctl actions entitlement create` and select your organization.
- Fork the project to show in the `Settings` that you can restrict where actions come from.

## Notes:
To get the SHA of any action, run this command with the `gh` CLI.
- `gh api repos/{ORG}/{REPO}/commits/{TAG} --jq '.sha'`
- Example: `gh api repos/imjasonh/setup-crane/commits/v0.5 --jq '.sha'`