# Overview of System Electronics

```plantuml
@startuml Functional System Components
node "Sensor Package" {
  [Software Defined Radio] as sdr
  [Low-Noise Amplifier] as lna
  [VHF Antenna] as ant
  [Data Storage] as recorder
  [GPS Receiver] as gps
  [Magnetometer] as compass
  package "On-Board Computer" {
    [Ping Detector] as detector
    [Georeferencing] as georeferencing
    [Controller] as controller
  }
  [Telemetry Link] as node_telem

  ant --> lna : RF Signal
  lna --> sdr : Amplified RF Signal
  sdr --> detector : Digitized RF Signal
  detector -> georeferencing : Pings
  gps --> georeferencing : Location and Timing
  compass --> georeferencing : Orientation
  georeferencing -r-> node_telem : Pings
  node_telem -u-> controller : Control Signals
  georeferencing -u-> recorder : Recorded Data
}

node "Control Node" {
  [Control Software] as gcs
  [Telemetry Link] as gcs_telem

  gcs_telem <-> gcs : Control Signals and Pings
}

node_telem <-l-> gcs_telem : Control Signals and Pings

@enduml
```

- UP 7000 single-board computer
  - requires 12V 5A power supply
- USRP B200mini software-defined radio (SDR)
  - Also connected to low-noise amplifier (LNA)
- NMEA GPS
- HMC-5983 magnetometer
- Communication device, ex:
	- WiFi antenna (or other comms)
	- SiK radio
- LEDs

puml for system, as of Dec 2023 (throw into plantuml to view diagram):
```plantuml
@startuml Implemented Electronic Components
node "Sensor Package" {
  [UP 7000] as obc
  [USRP B200mini] as sdr
  [NooElec LANA] as lna
  [VHF Antenna] as ant
  [900 MHz SiK Radio] as node_telem
  [USB Thumb Drive] as recorder
  [UBlox GPS Receiver] as gps
  [HMC5983 Magnetometer] as compass

  [Power Supply] as psu

  ant --> lna : RF Signal
  lna --> sdr : Amplified RF Signal
  sdr --> obc : Digitized RF Signal
  gps --> obc : Location and Timing
  compass --> obc : Orientation
  obc <-> node_telem : Control Signals and Pings
  obc --> recorder : Recorded Data

  psu -> lna : 5V
  psu -> obc : 12V
}

node "Control Node" {
  [Control Software] as gcs
  [900 MHz SiK Radio] as gcs_telem

  gcs_telem <-> gcs : Control Signals and Pings
}

node_telem <-> gcs_telem : Control Signals and Pings
@enduml
```