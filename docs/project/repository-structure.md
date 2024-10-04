# Repository Structure

Our project is structured across multiple repositories, each serving a specific purpose in the Radio Telemetry Tracker ecosystem.

## Main Repositories

![Repository Relationship Diagram](../../diagrams/img/repo_relationship.png)

1. **[radio-telemetry-tracker-docs](https://github.com/UCSD-E4E/radio-telemetry-tracker-docs)** (This repository)
   - Purpose: Central project documentation and coordination
   - Relationship: Parent repository, links to all other repositories

2. **[radio-telemetry-tracker-drone-comms-package](https://github.com/UCSD-E4E/radio-telemetry-tracker-drone-comms-package)**
   - Purpose: Shared communication package for drone-related components
   - Relationship: Used by both drone-fds and drone-gcs for communication

3. **[radio-telemetry-tracker-drone-fds](https://github.com/UCSD-E4E/radio-telemetry-tracker-drone-fds)**
   - Purpose: Field Device Software for drone operations
   - Relationship: Uses drone-comms-package for communication and radio_collar_tracker_dsp2 for signal processing

4. **[radio-telemetry-tracker-drone-gcs](https://github.com/UCSD-E4E/radio-telemetry-tracker-drone-gcs)**
   - Purpose: Ground Control Software for drone operations
   - Relationship: Uses drone-comms-package for communication with drone-fds

5. **[radio_collar_tracker_dsp2](https://github.com/UCSD-E4E/radio_collar_tracker_dsp2)**
   - Purpose: Digital Signal Processing package
   - Relationship: Used by drone-fds for signal processing

Each repository has its own README with more detailed information about its specific role and setup instructions.

## Version Control

All repositories in the Radio Telemetry Tracker project follow the Gitflow workflow (with some exceptions to older repositories that have not been updated to the new workflow). For more information on our Git workflow, please refer to the [Git Workflow](git-workflow.md) document.


