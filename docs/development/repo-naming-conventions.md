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

Note: Some repositories may not strictly follow this convention due to historical reasons or specific requirements.
