# MotoMonkey EU
## Introduction
I wanted to find a solid data acquisition and telemetry system for track motorcycle riding. Like everything else, commercially available kits are either too expensive for feature rich models or too basic for lower cost models.  MotoMonkey is born. My goal for MotoMonkey is to create an open-source feature-rich data system that is low cost and can be built by anyone with some technical savvy.  

## Simple Requirements
1. Cheap, cheap, cheap - Price point to build a MotoMonkey will be about a few hundred bucks.
2. Extensible - attempt to make so that sensor integration can be customized and software can be tailored to individual needs.
3. Data rich - interfaces for the ECU and BlueTooth, sensors for inertial measurement, GPS, and generic IO (analog and digital) for custom sensors and interfaces.
4. Telemetry - need to do some exploration here - would really like the system to use an ad-hoc network - that may be too far to reach - a simple point to point radio model may be the most achievable.

## System Design
The MotoMonkey consists of two major pieces - 1) The on-board data acquisition system and 2) a ground station laptop.
![Alt text](https://cloud.githubusercontent.com/assets/3347351/15641098/427cf59a-25f3-11e6-8442-03b79fd1e716.png)

### On-Board Data Acquisition System
#### CPU/MCU
I have choosen Beaglebone Black for this project. Cost effective. Runs linux and has 2 programmable real time units. BeagleBone Black has a video output which enables a screen to be used to present data.

Tentative functions identified for the CPU (and not limited to):
- A true inertial navigation system (INS) with GPS aiding - the INS provides accurate orinetations, position and velocity information (this is in contrast to an attitude and heading reference system, or AHRS, that only provides orientations)
- High capacity data logging to a M2 SSD
- Time synchronization with a GoPro

### GPS
A GPS receiver and antenna will be used for accurate position, velocity and time (PVT) information. GPS time will be used as the reference time on the system. GPS to be choosen needs to be accurate and fast (10Hz) to be able to log cornering on tracks

### Inertial Measurement Unit (IMU)

## Bill of Materials (BOM)
This table lists the parts I am using for the prototype - cost will come down when a PCB is designed and parts can be co-located on a single - compact board.

| Index | Item Name    | Description | Manufacturer | Part Number | Qty | Cost   | Total   |
| :---: | :--------    | :---------- | :----------- | :---------- | :-: | ---:   | ----:   |
| 1     | Black        | CPU/MCU     | Beaglebone   | N/A         | 1   |        |         |
| 2     | XBee Pro 868 | Data Link   | XBee         | N/A         | 2   |        |         |
| 3     | UBlox GPS    | GPS         | UBlox        | N/A         | 1   | $49.00 | $49.00  |
| 4     | AltIMU-10    | IMU         | Pololu       | N/A         | 1   | $23.00 | $22.00  |
|       |              |             |              |             |     | Total  | $231.00 |



## Installation
TODO: Describe the installation process

## Usage
TODO: Write usage instructions

## Contributing
1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History
TODO: Write history

## Credits
TODO: Write credits

## License
TODO: Write license
