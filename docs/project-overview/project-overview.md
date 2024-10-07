# Project Overview

Radio Telemetry Tracker (RTT) was established back in 2012 as an effort to track animals using radio telemetry. Traditional on-foot methods require researchers to trek through difficult terrain with unwieldy antennae, so a new drone-based system was developed to fly over an area in which animals equipped with transmitters can be found. An omni-directional antenna pointing downward beneath the drone picks up pings from the transmitters and sends that data back to a machine running our ground control station (GCS).

Recently, the project has been working on a new, tower-based system, in which several towers would be set up around a predetermined area and collect pings regularly throughout a deployment. Both the drone and tower systems are currently in development.

## Drone System Architecture

![Drone Hardware Diagram](../../diagrams/img/drone_hardware_setup.png)


## Repository Structure

![Repository Relationship Diagram](../../diagrams/img/repo_relationship.png)

1. **[radio-telemetry-tracker-docs](https://github.com/UCSD-E4E/radio-telemetry-tracker-docs)**: Central project documentation and coordination

2. **[radio-telemetry-tracker-drone-comms-package](https://github.com/UCSD-E4E/radio-telemetry-tracker-drone-comms-package)**: Shared communication package for drone-related components

3. **[radio-telemetry-tracker-drone-fds](https://github.com/UCSD-E4E/radio-telemetry-tracker-drone-fds)**: Field Device Software for drone operations

4. **[radio-telemetry-tracker-drone-gcs](https://github.com/UCSD-E4E/radio-telemetry-tracker-drone-gcs)**: Ground Control Software for drone operations

5. **[radio_collar_tracker_dsp2](https://github.com/UCSD-E4E/radio_collar_tracker_dsp2)**: Digital Signal Processing package

6. **[radio-telemetry-tracker-tower-solar-tools](https://github.com/UCSD-E4E/radio-telemetry-tracker-tower-solar-tools)**: Tools for calculating optimal solar panel and battery configurations for the tower system

7. **[radio-telemetry-tracker-drone-casing-code](https://github.com/UCSD-E4E/radio-telemetry-tracker-drone-casing-code)**: CAD files for the drone casing

Each repository has its own README with more detailed information about its specific role and setup instructions.

## References

The `references` directory contains bibliography files for project-related publications:

1. **project_publications.bib**: Contains citations for publications directly about the Radio Telemetry Tracker project.
2. **related_papers.bib**: Contains citations for papers related to the field of radio telemetry tracking but not specifically about this project.

These .bib files can be used with reference management software and LaTeX to easily cite relevant literature in project documentation and publications.