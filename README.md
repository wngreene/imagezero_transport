# ImageZero ROS image\_transport implementation

ImageZero is a fast, lossless compression algorithm for 24-bit color photographic
images developed by (Christopher Feck)[christoph@maxiom.de].  This repository
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
