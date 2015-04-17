# ardrone_autonomy

ardrone_autonomy is a [ROS](http://ros.org/ "Robot Operating System") driver for [Parrot AR-Drone](http://ardrone2.parrot.com/) 1.0 & 2.0 quadrocopter. This driver is based on official [AR-Drone SDK](https://projects.ardrone.org/) version 2.0.1. "ardrone_autonomy" is a fork of [AR-Drone Brown](http://code.google.com/p/brown-ros-pkg/wiki/ardrone_brown) driver. This package has been developed in [Autonomy Lab](http://autonomylab.org) of [Simon Fraser University](http://www.sfu.ca) by [Mani Monajjemi](http://mani.im) ( +other [contributors](#contributors)).

## Updates

- *April 2014*: 1.4
-- Publish Odometry (#123)
-- Support for multiple instances of the driver on a single machine (#98)
-- Use reception time for video streams (#89)
-- Refactoring of source code and build system
-- Deprecated setting TF root frame (6afa19729b4faf)
-- Deprecated auto IMU calibration (6afa19729b4faf)
- *September 3 2014*: 1.3.5 [Bug Fixes & Minor Improvements](https://github.com/AutonomyLab/ardrone_autonomy/milestones/1.3.5)
- *March 14 2014*: The binary packages of the driver are now built on [ROS build farm](http://wiki.ros.org/BuildFarm). You can install the driver for ROS _Hydro_ and _Groovy_ using `apt-get` on _Ubuntu_.
- *January 17 2014*: Fully _catkinized_ package ([#75](https://github.com/AutonomyLab/ardrone_autonomy/pull/75) & [#79](https://github.com/AutonomyLab/ardrone_autonomy/pull/79)). ARDroneLib has been configured to be built as an external project. The ARDroneLib is replaced by the vanilla SDK's stripped tarball. ([More info](https://github.com/AutonomyLab/ardrone_autonomy/pull/80)).
- *October 22 2013*: Update to Parrot SDK 2.0.1 (Fixes crashes on 2.4.x firmwares, no support for flight recorder (yet). **Please check the FAQ section for instructions on how to re-compile the SDK**. (Tested on 2.3.3 and 2.4.x firmwares) 
- *February 13 2013*: Support for USB key recording ([More info](https://github.com/AutonomyLab/ardrone_autonomy/pull/53)). Motor PWM added to legacy Navdata.
- *January 9 2013*: ROS Groovy support. Support for zero-command without hovering ([More info](https://github.com/AutonomyLab/ardrone_autonomy/pull/34)). Full configurable Navdata support ([More info](https://github.com/AutonomyLab/ardrone_autonomy/pull/31)). Support for "Flight Animations". Support for Real-time navdata and video publishing ([More info](https://github.com/AutonomyLab/ardrone_autonomy/pull/44)). Support for configurable data publishing rate.
- *November 9 2012*: Critical Bug in sending configurations to drone fixed and more parameters are supported ([More info](https://github.com/AutonomyLab/ardrone_autonomy/issues/24)). Separate topic for magnetometer data added ([More info](https://github.com/AutonomyLab/ardrone_autonomy/pull/25)).
- *September 5 2012*: Experimental automatic IMU bias removal.
- *August 27 2012*: Thread-safe SDK data access. Synchronized `navdata` and `camera` topics.
- *August 20 2012*: The driver is now provides ROS standard camera interface.
- *August 17 2012*: Experimental `tf` support added. New published topic `imu`.
- *August 1 2012*: Enhanced `Navdata` message. `Navdata` now includes magnetometer data, barometer data, temperature and wind information for AR-Drone 2. [Issue #2](https://github.com/AutonomyLab/ardrone_autonomy/pull/2)
- *July 27 2012*: LED Animation Support added to the driver as a service
- *July 19 2012*: Initial Public Release
