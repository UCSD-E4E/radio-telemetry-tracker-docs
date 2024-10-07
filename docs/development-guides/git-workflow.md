# Git Workflow

Our project follows the Gitflow workflow for structured version control and collaboration. This allows us to manage feature development, bug fixes, and releases efficiently.

## Branching Model Overview
Gitflow uses multiple branches to maintain a clean history and facilitate collaboration. The key branches are:

- `main`: Production-ready code
- `develop`: The integration branch for features

Additional branches:
- **Feature**: `feature/[feature-name]`
- **Release**: `release/[version-number]`
- **Hotfix**: `hotfix/[hotfix-name]`

## Workflow Steps

1. **Feature Development**
   - Branch: `feature/[feature-name]`
   - Merge: Into `develop` after approval

2. **Preparing a Release**
   - Branch: `release/[version-number]`
   - Merge: Into both `main` and `develop` after bug fixes
   - Tag the release: `vX.Y.Z`

3. **Hotfixes**
   - Branch: `hotfix/[hotfix-name]`
   - Fix the issue in `main`, then merge into both `main` and `develop`
   - Tag the version

## Versioning and Release Process

We follow [semantic versioning](https://semver.org) for releases with some changes:
- **MAJOR.MINOR.PATCH**

- **MAJOR**: Major changes that break compatibility with previous versions in the entire system (i.e. change hardware communication or protocol)
- **MINOR**: New features that only breaks compatibility with previous versions of the same system (i.e. changing GPS on the drone and updating the software, but exchanged data is the same)
- **PATCH**: Bug fixes or features that do not change exchanged data (i.e. fixing the GPS getting signal but not updating the co-ordinates)

For more about Gitflow, visit the [Atlassian Gitflow Tutorial](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow).
