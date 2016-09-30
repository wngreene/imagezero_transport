# ImageZero ROS image\_transport implementation

This repository contains the following catkin packages:

## imagezero

The [ImageZero](http://imagezero.maxiom.de/) image compression library, restructured into a catkin package.  ImageZero is a high-performance lossless compression algorithm designed for natural photos.

## imagezero\_ros

A library that contains a few convenience methods for using ImageZero to convert between `sensor_msgs/Image`s and `sensor_msgs/CompressedImage`s.

## imagezero\_image\_transport

A ROS [image\_transport](http://wiki.ros.org/image_transport) plugin that uses ImageZero as its compression mechanism.  It can be used like any other ROS image\_transport by setting the `image_transport` param for your client node to `imagezero`.
