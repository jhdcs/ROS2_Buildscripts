ROS2_Buildscripts

These are just some bash scripts that I use on Ubuntu 18.04 as I try to develop for ROS 2. They aren't perfect, but they're what I've got so far.
Feel free to use them, and feel free to suggest changes. I want to help make ROS 2 development as accessible as I can.

NOTE: These scripts assume you're working with a base directory of "~/ros2_ws". You have been warned!

Brief description of each:

**buildall** : runs "colcon build --symlink-install" on the base directory
> EXAMPLE USAGE:
  $ buildall
  
**buildtest_dep** : runs "colcon build --symlink-install --packages-above <package>" followed by "colcon test --packages-above <package>" on the base directory
> EXAMPLE USAGE:
  $ buildtest_dep rclcpp

**buildtest_one** : runs "colcon build --symlink-install --packages-select <package>" followed by "colcon test --packages-select <package>" on the base directory
> EXAMPLE USAGE:
  $ buildtest_one rclcpp

**rebuildall** : Basically runs the steps defined at https://index.ros.org/doc/ros2/Installation/Maintaining-a-Source-Checkout/ on your main repository. Useful if you're getting build errors and think it might be from someone updating other repositories.
> EXAMPLE USAGE:
  $ rebuildall

**testall** : runs "colcon test" on your main repository. Yes, I am actually that lazy.
> EXAMPLE USAGE:
  $ testall
