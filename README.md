# Radio Telemetry Tracker (RTT) Project Handbook

Welcome to the Radio Telemetry Tracker (RTT) project! This handbook serves as a centralized resource for users and contributors, consolidating everything from repository structure and setup instructions to meeting notes and order forms.

## Table of Contents

- [Radio Telemetry Tracker (RTT) Project Handbook](#radio-telemetry-tracker-rtt-project-handbook)
  - [Table of Contents](#table-of-contents)
  - [Project Overview](#project-overview)
  - [System Architecture](#system-architecture)
    - [VHF Wildlife Transmitters](#vhf-wildlife-transmitters)
    - [Drone-Based Tracking](#drone-based-tracking)
      - [Drone Field Device](#drone-field-device)
      - [Drone Ground Control](#drone-ground-control)
    - [Tower-Based Tracking](#tower-based-tracking)
  - [Repository Layout](#repository-layout)
    - [Documentation (`docs/`)](#documentation-docs)
    - [Root Files](#root-files)
  - [Contributing](#contributing)
    - [Becoming a Project Member](#becoming-a-project-member)
    - [Other Contributors](#other-contributors)
  - [License](#license)


## Project Overview

Since 2012, RTT has been developing wildlife tracking by replacing time-consuming, on-foot radio telemetry with automated systems. Our solutions enable researchers to monitor animals carrying VHF transmitters more efficiently, reducing field time and improving data quality.

Currently, the project includes two complementary tracking approaches:
- **Drone-Based Tracking:** Quick, mobile deployments using unmanned aerial vehicles (UAVs).
- **Tower-Based Tracking:** Fixed installations for long-term, large-area monitoring.

Both systems collect signal pings from tagged wildlife, estimate locations, and visualize results in real time.


## System Architecture 

### VHF Wildlife Transmitters

RTT is built for On-Off Keying (OOK) VHF transmitters operating between **138 MHz** and **235 MHz**. We have tested with Holohil transmitters.

### Drone-Based Tracking

A drone flies over the study area with a downward-facing omni-directional antenna. As animals ping, the system triangulates their positions and streams data back to a Ground Control.

#### Drone Field Device

![Image](/docs/assets/diagrams/img/drone-hardware-setup.png)

While the system can support other hardware, these are our recommendations for the core components: 

- **Single Board Computer:** [UP 7000](https://up-shop.org/default/up-7000-series.html) (Intel N100, 8 GB RAM, 64 GB eMMC) 
- **GPS & Compass:** [SparkFun NEO‑M9N Breakout](https://mou.sr/3Pt2lmy)
- **Software Defined Radio:** [USRP B200mini‑i](https://www.ettus.com/all-products/usrp-b200mini-i-2/)
- **Low Noise Amplifier:** [Nooelec LaNA](https://www.nooelec.com/store/lana.html)
- **Telemetry Radio (900 MHz):** [SiK V3 Telemetry Radio](https://www.sparkfun.com/sik-telemetry-radio-v3-915mhz-100mw.html)
- **Drone Interface:** DJI Skyport + Extension Board

Drone Field Device Software: `radio-telemetry-tracker-drone-fds`
Runs on the single board computer, interfaces with sensors and radios, and sends processed data to the GCS.

GitHub: https://github.com/UCSD-E4E/radio-telemetry-tracker-drone-fds

#### Drone Ground Control

The Ground Control can be a laptop running Windows 10+ or Ubuntu 24.04. Additionally the laptop will have the aditional telemetry radio that the Field Device uses.

Drone GCS Software: `radio-telemetry-tracker-drone-gcs`
Desktop application for real-time map visualization and data management.

GitHub: https://github.com/UCSD-E4E/radio-telemetry-tracker-drone-gcs

### Tower-Based Tracking

Coming Soon

## Repository Layout

The repository is organized into several directories:

### Documentation (`docs/`)
- **Processes** (`docs/processes/`): Contains documentation about development workflows, repository setup, and naming conventions
- **Assets** (`docs/assets/`): Stores project assets including diagrams and images
- **References** (`docs/references/`): Contains bibliographic references and related research papers
- **Project Management** (`docs/project-management/`): 
  - Meeting notes and agendas
  - Purchase records and order forms
  - Project proposals and planning documents

### Root Files
- `README.md`: This main project handbook
- `LICENSE.md`: Project license information

Each documentation directory contains its own README file explaining its specific contents and purpose in more detail.

## Contributing

### Becoming a Project Member

If you are a student at Univeristy of California San Diego or another univiersity and would like to contribute to this project, please check out Engineers for Exploration's website for more information about the lab and how to join.

Website: https://e4e.ucsd.edu/


### Other Contributors 

Non-project members are welcome to contribute to software for the project through pull requests.

## License

This project is licensed under the terms specified in the [LICENSE](LICENSE.md) file.

