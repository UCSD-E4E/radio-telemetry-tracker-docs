# Git Workflow

The Radio Telemetry Tracker project uses the Gitflow workflow for version control and collaboration. This workflow helps us maintain a structured development process and manage releases effectively.

## Gitflow Overview

Gitflow is a branching model that uses multiple branches to record the history of the project. The two main branches are:

1. `main` (or `master`): Contains production-ready code
2. `develop` (or `dev`): Serves as an integration branch for features

In addition to these, we use the following supporting branches:

- Feature branches
- Release branches
- Hotfix branches

## Branch Naming Convention

- Feature branches: `feature/[feature-name]`
- Release branches: `release/[version-number]`
- Hotfix branches: `hotfix/[hotfix-name]`

## Workflow Steps

1. **Feature Development**
   - Create a feature branch from `develop`
   - Work on the feature
   - Create a pull request to merge back into `develop`

2. **Preparing a Release**
   - Create a release branch from `develop`
   - Make any final adjustments and bug fixes
   - Merge the release branch into both `main` and `develop`
   - Tag the release in `main`

3. **Hotfixes**
   - Create a hotfix branch from `main`
   - Fix the critical bug
   - Merge the hotfix into both `main` and `develop`
   - Tag the new version in `main`

## Best Practices

1. Always create pull requests for merging feature branches
2. Regularly update your feature branch with changes from `develop`
3. Use meaningful commit messages
4. Delete feature branches after merging

## Releases and Versioning

The Radio Telemetry Tracker project uses semantic versioning for releases. Our version numbers follow the format `MAJOR.MINOR.PATCH`.

### Version Number Significance

1. **MAJOR**: Incremented when there are software changes dependent on hardware changes. Previous hardware (and by consequence, software) may not be compatible and needs evaluation before updating.

2. **MINOR**: Indicates compatibility at the software level. All software components in the system need to be updated to the same minor version.

3. **PATCH**: Signifies non-compatibility breaking changes (bugfixes or minor features). Can be updated as long as the MAJOR and MINOR numbers match the rest of the system.

### Release Process

1. Ensure all changes for the release are merged into the `develop` branch.
2. Create a release branch: `release/vX.Y.Z`
3. Update version numbers in all relevant files.
4. Commit changes and push the release branch.
5. Create a pull request to merge the release branch into `main`.
6. After approval and merging, tag the release in the `main` branch: `vX.Y.Z`
7. Merge the release branch back into `develop`.

### Automated Release Workflow

Releases are automated using a GitHub Actions workflow. When a new version is triggered in the main repository:

1. The workflow checks out the code.
2. It builds and tests the project.
3. If successful, it creates a new release with the specified version number.
4. Release artifacts are automatically generated and attached to the release.

For detailed information on the release workflow, refer to the `.github/workflows/release.yml` file in each repository.

For more detailed information on the Gitflow workflow, refer to the [Atlassian Gitflow Tutorial](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow).
