imagezero\_transport [![Build Status](https://travis-ci.org/swri-robotics/imagezero_transport.svg?branch=master)](https://travis-ci.org/swri-robotics/imagezero_transport)
==========================================================================================================================================================================

ImageZero is a fast, lossless compression algorithm for 24-bit color photographic
images developed by [Christopher Feck](christoph@maxiom.de).  This repository
repackages it as a catkin package, has a package that implements convenience
functions for manipulating ROS images, and has a package that implements a ROS
image\_transport plugin that uses it.

Catkin packages in this repository include:

## imagezero

The [ImageZero](http://imagezero.maxiom.de/) image compression library, restructured into a catkin package.  ImageZero is a high-performance lossless compression algorithm designed for natural photos.

## imagezero\_ros

A library that contains a few convenience methods for using ImageZero to convert between `sensor_msgs/Image`s and `sensor_msgs/CompressedImage`s.

## imagezero\_image\_transport

A ROS [image\_transport](http://wiki.ros.org/image_transport) plugin that uses ImageZero as its compression mechanism.  It can be used like any other ROS image\_transport by setting the `image_transport` param for your client node to `imagezero`.


Travis CI Build Status
----------------------


Building From Source (ROS Indigo, Jade, Kinetic)
------------

These directions assume you have already set up a catkin workspace. See [this tutorial](http://wiki.ros.org/catkin/Tutorials/create_a_workspace) on the ROS Wiki for help setting up a catkin workspace.

### Checking out the source code (wstool)

If you're using wstool, add this repository to your wstool workspace:

    # Replace <ros_distro> with indigo or jade as appropriate
    wstool set mapviz --git https://github.com/swri-robotics/imagezero_transport.git -v <ros_distro>-devel

### Checking out the source code (git)

If you're not using wstool, you can check out the repositories with git:

    # Replace <ros_distro> with indigo or jade as appropriate
    git clone https://github.com/swri-robotics/imagezero_transport.git --branch <ros_distro>-devel

### Installing dependencies and building

Install all of the dependencies using rosdep by running the following command from the root of your catkin workspace:

    rosdep install --from-paths src --ignore-src

Build the workspace with catkin_make:

    catkin_make

