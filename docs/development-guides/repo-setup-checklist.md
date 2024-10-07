# Repository Setup Checklist (Software)

This checklist ensures consistent setup across all repositories in the Radio Telemetry Tracker project.

## 1. Branch Protection

- Enable branch protection for `main`
- Require pull request reviews and passing status checks
- Branches must be up to date before merging

## 2. Linters & Package Management

### Python

- Use `ruff` for linting
- Use `poetry` for package management

## 3. Workflows

- Set up CI with GitHub Actions to run linters and unit tests
- Optional: Set up CD for automated deployments

## 4. Docker

- Use Docker for local development and deployment
- Include appropriate Dockerfiles and `docker-compose` configurations

## 5. Documentation

- Include `README.md` and `LICENSE.md` in each repository

By following these practices, we ensure consistency across all repositories.
