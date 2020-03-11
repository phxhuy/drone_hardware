# drone_hardware
A collection of hardware, drone design knowledge, and CAD models

This page is a summary of basic quadrotor design for racing drones, commonly called FPV - First Person View - drones. The basic knowledge comes from various source, notably research groups like [uzh-rpg](https://github.com/uzh-rpg/rpg_quadrotor_control/wiki/RPG-Quadrotor-Setup), [ethz-asl](https://github.com/ethz-asl/mav_tools_public/wiki/Basic-MAV-Hardware), and dedicated communities and commercial pages like [getfpv.com](https://www.getfpv.com/learn/new-to-fpv-beginner/)

## Basic system design

*Drone Frame*
The most popular configuration for drone racing is 250 mm frame (hence, in the class of "mini" drones). Due to being light weight and durability, most drone frames are cut from carbon sheets, but note that carbon fiber is electrically conductive.

*Motor and propellers*
High-power motors with short propellers are selected. Typically the motor has around 2000 KV, and 5-inch propellers. However, longer propellers (e.g. 6") can also be used to provide extra payload for the drone to carry more sensors/computing units.

The recent protocol DShot for motor ESCs offers attractive [advantages](https://docs.px4.io/master/en/peripherals/dshot.html), such as reduced latency and better noise resistant, but particular details in wiring must be paid attention to, such as [this px4 guide](https://docs.px4.io/v1.9.0/en/assembly/quick_start_pixhawk4.html)

This [site](https://www.miniquadtestbench.com/motors/) provides a very good benchmark to compare the performance of different motors.

Generally,the larger the prop (by either increasing diameter, or pitch or both), the more energy it takes to spin it. Therefore, larger propeller or higher pitch length (4.8 – 5.1) will increase the aircraft’s speed but also use more power. [How to choose the right propeller](https://oscarliang.com/choose-propellers-mini-quad/)

A good tip from Oscar Liang's page:

- 5″ props for 210mm frame, use 2300KV-2700KV motors
- 6″ props for 250mm+ frame, use 1900KV-2300KV motors

*Autopilot board*
Pixhawk's PX4-based hardware and flight stack are selected due to its popularity and supports for autonomous flight. A good comparison between different open-source autopilot can be found in [this](https://dojofordrones.com/open-source-drone/)


*Computing Unit*
For main onboard computers, people usually using small, low-power computers such as [Intel Up Board](https://up-board.org/) (that has comparable performance as an [Intel Aero drone](https://click.intel.com/intel-aero-ready-to-fly-drone-2901.html)) or [Odroid XU4](https://www.hardkernel.com/shop/odroid-xu4-special-price/). Some also use a whole development kits such as [Qualcomm® Flight Pro™ Development Kit](https://www.intrinsyc.com/qualcomm-flight-pro-development-kit/)

## Weights

Normally racing drone is optimized so that it has minimum weight. Autonomous drones, however, require a bit more payload for additional processing computer(s), camera(s) and other sensor(s). The racing drone of [uzh-rpg], winner of IROS 2018 Drone Racing Event, has overall weight of around 900 g.

## Sensor suite


## Wiring diagrams for a PX4 drone
