# Naming Conventions

Our repositories follow a specific naming pattern to indicate their purpose and relationship within the project:

`radio-telemetry-tracker-[system]-[software-type]-[package]`

- `radio-telemetry-tracker`: The project name
- `[system]`: The system it's made for (e.g., 'drone' or 'tower'), or omitted if shared
- `[software-type]`: The type of software
  - `fds`: Field Device Software
  - `gcs`: Ground Control Software
  - `comms`: Communication
- `[package]`: Appended if it's a supporting package rather than standalone software

For example:
- `radio-telemetry-tracker-drone-fds`: Field Device Software for the drone system
- `radio-telemetry-tracker-drone-comms-package`: A communication package for the drone system

## Binary File Repositories

For repositories dedicated to binary files such as CAD designs or PCB layouts, we use the following naming convention:

`radio-telemetry-tracker-[system]-[file-type]-[component]`

- `[file-type]`: The type of binary files
  - `cad`: Computer-Aided Design files
  - `pcb`: Printed Circuit Board design files
- `[component]`: The specific component or function (e.g., 'casing', 'antenna', 'power-supply')

For example:
- `radio-telemetry-tracker-drone-cad-casing`: CAD files for the drone system's casing
- `radio-telemetry-tracker-tower-pcb-interface`: PCB design files for the tower system's part interface

Note: Some repositories may not strictly follow these conventions due to historical reasons or specific requirements.
