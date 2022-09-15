# Boat-Rover

The focus of this project is an attempt to develop a suitable solution to survey the subsurface topography of a water body. This was done by creating a semi-autonomous rover capable of mapping its subsurface environment to a depth of 30m, as well as a base station controller.

## Rover Design

The rover is built completely from the ground up. The chassis consists of PVC piping sealed to create an airtight frame using PVC wet cement. The rover takes inspiration from catamaran designs to bolster stability and airboats to decrease draft. Pool floats were attached to the twin hulls to increase bouyancy and adjust the trim of the craft, however. A platform of acrylic layed across the middle section of the chassis supports a watertight box within which the control circuitry resides. Affixed to the supporting acrylic are wooden beams to which motor are attached. All together, the rover looks like this:

![Image 1](https://github.com/Michael-117/Boat-Rover/blob/main/IMG_20200714_203957.jpg)
![Image 2](https://github.com/Michael-117/Boat-Rover/blob/main/IMG_20200714_204042.jpg)

The rover's control circuitry uses the following components:
* 1 x ESP-32 Microcontroller
* 2 x Brushless DC motors
* 2 x Electronic Speec Controllers
* 2 x LiPo Batteries
* 1 x HC-12 433MHz Radio
* 1 x 3dBi RF Antenna
* 1 x BNO-055 IMU Module
* 1 x NEO-6M GPS Module
* 1 x 28dB GPS Antenna
* 1 x DC-DC Buck Converter
* 1 x BlueRobotics Ping Sonar

The navigation of the rover is managed by the pairing of the IMU and GPS module. Differential motors are employed with the resulting heading and speed data to navigate to the target waypoints in turn. These waypoints are communicated to the rover through RF from the base station. As the rover traverses the area, mapping is carried out using the sonar at a sampling rate of 1Hz. Telemetry readings are continuously sent back to the base station to be archived and processed into a 3-D diagram. 


## Base Station Design
