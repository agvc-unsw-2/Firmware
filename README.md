# A badly hacked fork of the PX4 Pro Drone Autopilot Firmware
A hacked version of the PX4 1.9.2 Firmware based on [ethz-asl](https://github.com/ethz-asl) hacked version on [ethzasl_mav_px4](https://github.com/ethz-asl/ethzasl_mav_px4)

## See https://github.com/PX4/Firmware for the original

# PX4 Drone Autopilot

[![Releases](https://img.shields.io/github/release/PX4/Firmware.svg)](https://github.com/PX4/Firmware/releases) [![DOI](https://zenodo.org/badge/22634/PX4/Firmware.svg)](https://zenodo.org/badge/latestdoi/22634/PX4/Firmware)

[![Build Status](http://ci.px4.io:8080/buildStatus/icon?job=PX4/Firmware/master)](http://ci.px4.io:8080/blue/organizations/jenkins/PX4%2FFirmware/activity)

[![Slack](https://px4-slack.herokuapp.com/badge.svg)](http://slack.px4.io)

This repository holds the [PX4](http://px4.io) flight control solution for drones, with the main applications located in the [src/modules](https://github.com/PX4/Firmware/tree/master/src/modules) directory. It also contains the PX4 Drone Middleware Platform, which provides drivers and middleware to run drones.

* Official Website: http://px4.io (License: BSD 3-clause, [LICENSE](https://github.com/PX4/Firmware/blob/master/LICENSE))
* [Supported airframes](https://docs.px4.io/en/airframes/airframe_reference.html) ([portfolio](http://px4.io/#airframes)):
  * [Multicopters](https://docs.px4.io/en/airframes/airframe_reference.html#copter)
  * [Fixed wing](https://docs.px4.io/en/airframes/airframe_reference.html#plane)
  * [VTOL](https://docs.px4.io/en/airframes/airframe_reference.html#vtol)
  * many more experimental types (Rovers, Blimps, Boats, Submarines, etc)
* Releases: [Downloads](https://github.com/PX4/Firmware/releases)

 ## Changes

 ### Filtering
* The highrate IMU topic has a 10 Hz butterworth filter applied to it.

### Control
* In offboard mode desired yaw is ignored allowing the sending of roll, pitch yawrate commands.

### Safety
* The kill switch also disarms the system
* Arming also controls the aux ports

### IO
* Highres IMU is published at 100 Hz
* Most non-esential messages are broadcast at a much reduced rate
