# Repository Setup Checklist

This checklist ensures that all repositories in the Radio Telemetry Tracker project are set up consistently and follow best practices. Use this guide when creating a new repository or updating an existing one.

## 1. Branch Protection

- Repositories MUST enable branch protection for the `main` branch and MAY enable branch protection for the `develop` branch.
- Pull request reviews MUST be required before merging.
- Status checks MUST pass before merging is allowed.
- Branches MUST be up to date before merging.
- These restrictions SHOULD include administrators.

## 2. Linters and Code Formatting

- Python projects MUST use Ruff.

## 3. Workflows

- Repositories MUST set up a CI workflow using GitHub Actions that:
  - Runs linters
  - Runs unit tests (where applicable)
- Repositories SHOULD set up a CD workflow for automatic deployments (releases) where applicable.

## 4. Docker

- Projects SHOULD use Docker for local development and deployments unless project cannot be containerized and other options have been exhausted. 
    - Recommended files: 
        - `Dockerfile` or `Dockerfile.dev` and `Dockerfile.release`
        - `.devcontainer` folder with a `devcontainer.json` file.
        - `docker-compose.yml` or `docker-compose.dev.yml` and `docker-compose.release.yml`
- Note: For the time being, we assume users build release images locally instead of using a registry. 

## 5. Documentation

- Repositories MUST include a comprehensive README.md file.
- License information (LICENSE.md) MUST be present and use [The Regents of the University of California copyright notice](../../LICENSE.md). 

By adhering to these requirements, we ensure that all repositories in the Radio Telemetry Tracker project are set up consistently and adhere to best practices in software development.
