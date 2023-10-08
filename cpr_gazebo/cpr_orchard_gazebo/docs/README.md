# cpr_orchard_gazebo

Outdoor orchard simulation world for Gazebo

## Supported Platforms

### Husky
<img src="https://clearpathrobotics.com/wp-content/uploads/2015/07/husky.jpg" width="20%">

[![Launch Stack](launch-stack.png)](
https://console.aws.amazon.com/cloudformation/home#/stacks/create/review?region=us-east-2&templateURL=https://cpr-gazebo-public.s3.us-east-2.amazonaws.com/CPR-Kinetic-Simulation-Stack.yaml&stackName=cpr-orchard-gazebo&param_SimWorld=cpr_orchard_gazebo&param_SimLaunch=orchard_world.launch&param_RoboticPlatform=husky)

### Jackal
<img src="https://clearpathrobotics.com/wp-content/uploads/2015/07/jackal.jpg" width="20%">

[![Launch Stack](launch-stack.png)](
https://console.aws.amazon.com/cloudformation/home#/stacks/create/review?region=us-east-2&templateURL=https://cpr-gazebo-public.s3.us-east-2.amazonaws.com/CPR-Kinetic-Simulation-Stack.yaml&stackName=cpr-orchard-gazebo&param_SimWorld=cpr_orchard_gazebo&param_SimLaunch=orchard_world.launch&param_RoboticPlatform=jackal)

### Warthog
<img src="https://s3.amazonaws.com/assets.clearpathrobotics.com/wp-content/uploads/2016/08/25085714/warthog-menu.jpg" width="20%">

[![Launch Stack](launch-stack.png)](
https://console.aws.amazon.com/cloudformation/home#/stacks/create/review?region=us-east-2&templateURL=https://cpr-gazebo-public.s3.us-east-2.amazonaws.com/CPR-Kinetic-Simulation-Stack.yaml&stackName=cpr-orchard-gazebo&param_SimWorld=cpr_orchard_gazebo&param_SimLaunch=orchard_world.launch&param_RoboticPlatform=warthog)

## Launching

```roslaunch cpr_orchard_gazebo orchard_world.launch```

Optionally, you can specify a platform using the platform variable:

```roslaunch cpr_orchard_gazebo orchard_world.launch platform:=jackal```

Supported values for the platform variable are:
* husky (default)
* jackal
* warthog

The spawn location for the robot can be specified by setting the `x`, `y`, `z`, and `yaw` variables.  The Z value should be set
to be above ground-level; otherwise the robot may fall through the ground plane as the environment renders.

## Features

This is a large, open, outdoor world for Gazebo that has:

Many rows of trees separated by dirt paths

<img src="husky-orchard.png">

<img src="whole-world.png">

There are a few wider, flat areas at each end of the orchard.  The terrain has small bumps, but overall is very flat.
