# Repository Naming Conventions

This guide outlines naming conventions for branches in the Radio Telemetry Tracker project to maintain consistency.

## Branch Naming Guidelines

- **Feature branches**: `feature/[brief-description]`
    - Example: `feature/add-drone-comm-module`
- **Release branches**: `release/[version-number]`
    - Example: `release/v1.2.0`
- **Hotfix branches**: `hotfix/[brief-description]`
    - Example: `hotfix/fix-gps-issue`

## Repository Naming Conventions

Our repositories follow a specific naming pattern to indicate their purpose and relationship within the project:

### Software Repositories
`radio-telemetry-tracker-[system]-[software-type]-[package]-[tools]`

- `radio-telemetry-tracker`: The project name
- `[system]`: The system it's made for (e.g., 'drone' or 'tower'), or omitted if shared
- `[software-type]`: The type of software (e.g., 'fds', 'gcs', 'comms', 'tools')
- `[package]`: Appended if it's a supporting package rather than standalone software
- `[tools]`: Appended if it's a tool for the project

For example:
- `radio-telemetry-tracker-drone-fds`: Field Device Software for the drone system
- `radio-telemetry-tracker-drone-comms-package`: A communication package for the drone system

### Binary File Repositories

For repositories dedicated to binary files such as CAD designs or PCB layouts, we use the following naming convention:

`radio-telemetry-tracker-[system]-[component]-[file-type]`

- `[component]`: The specific component or function (e.g., 'casing', 'antenna', 'power-supply')
- `[file-type]`: The type of binary files (e.g., 'cad', 'pcb')

For example:
- `radio-telemetry-tracker-drone-antenna-cad`: CAD files for the drone system's antenna
- `radio-telemetry-tracker-tower-interface-pcb`: PCB design files for the tower system's part interface

Note: Some repositories may not strictly follow these conventions due to historical reasons or specific requirements.

For detailed workflow steps, refer to the [Git Workflow](git-workflow.md) document.