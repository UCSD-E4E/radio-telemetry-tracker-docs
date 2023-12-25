# Overview of System Electronics

- UP Core single-board computer
  - requires 5V 1500mA-4000mA power supply
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
@startuml system
node "Payload" {
  5V - [UP Core]

  [USRP]
  5V - [LNA]
  [Antenna]

  [USB Splitter]
  [SiK Radio]
  [Thumb Drive]

  [PCB]
  [GPS]
  [Magnetometer]
}

[Antenna] --> [LNA]
[LNA] --> [USRP]
[USRP] --> [UP Core]

[SiK Radio] --> [USB Splitter]
[Thumb Drive] --> [USB Splitter]
[USB Splitter] --> [UP Core]

[GPS] --> [PCB]
[Magnetometer] --> [PCB]
[PCB] --> [UP Core]
@enduml
```