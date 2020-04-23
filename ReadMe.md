# Concurrent Traffic Simulation

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

In this project, I have simulated a traffic situation where cars move along the street. Each intersection has traffic lights and cars have to act due the status of the traffic lights. In this simulation, the thread-safe communication protocol between cars can help to do this project proper. This project needs the OpenCV library and some other dependencies for C++ that I have explained below how you can install them.

## Dependencies for Running Locally
* cmake >= 2.8
    * All OSes: click here for installation instructions
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
    * Linux: make is installed by default on most Linux distros
    * Mac: install Xcode command line tools to get make
    * Windows: Click here for installation instructions
* gcc/g++ >= 5.4
    * Linux: gcc / g++ is installed by default on most Linux distros
    * Mac: same deal as make - install Xcode command line tools
    * Windows: recommend using MinGW

## Installing OpenCV
Here, I am going to explain how you can install the OpenCV library in Ubuntu for C++. As you know, OpenCV is a crucial library which is used in Image Processing and Computer Vision project.   It is a collection of C functions and a few C++ classes that implement some popular Image Processing and Computer Vision algorithms. OpenCV is available on Mac, Windows, Linux.

#### Updating Ubuntu
```bash 
$ sudo apt-get update
```
```bash 
$ sudo apt-get upgrade
```

### Install dependencies
```bash 
$ sudo apt-get install build-essential cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
```

```bash 
$ sudo apt-get install python3.5-dev python3-numpy libtbb2 libtbb-dev
```

```bash 
$ sudo apt-get install libjpeg-dev libpng-dev libtiff5-dev libjasper-dev libdc1394-22-dev libeigen3-dev libtheora-dev libvorbis-dev libxvidcore-dev libx264-dev sphinx-common libtbb-dev yasm libfaac-dev libopencore-amrnb-dev libopencore-amrwb-dev libopenexr-dev libgstreamer-plugins-base1.0-dev libavutil-dev libavfilter-dev libavresample-dev
```

### Get OpenCV
```bash 
$ sudo -s
```
```bash 
$ cd /opt
```
```bash 
/opt$ git clone https://github.com/Itseez/opencv.git
```
```bash 
/opt$ git clone https://github.com/Itseez/opencv_contrib.git
```

### Build and install OpenCV
```bash 
/opt$ cd opencv
```
```bash 
/opt/opencv$ mkdir release
```
```bash 
/opt/opencv$ cd release
```
```bash 
/opt/opencv/release$ cmake -D BUILD_TIFF=ON -D WITH_CUDA=OFF -D ENABLE_AVX=OFF -D WITH_OPENGL=OFF -D WITH_OPENCL=OFF -D WITH_IPP=OFF -D WITH_TBB=ON -D BUILD_TBB=ON -D WITH_EIGEN=OFF -D WITH_V4L=OFF -D WITH_VTK=OFF -D BUILD_TESTS=OFF -D BUILD_PERF_TESTS=OFF -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D OPENCV_EXTRA_MODULES_PATH=/opt/opencv_contrib/modules /opt/opencv/
```
```bash 
/opt/opencv/release$ make -j4
```
```bash 
/opt/opencv/release$ make install
```
```bash 
/opt/opencv/release$ ldconfig
```
```bash 
/opt/opencv/release$ exit
```
```bash 
/opt/opencv/release$ cd ~
```

Now to check if OpenCV is installed on a machine, run the following commands
```bash 
pkg-config --modversion opencv
```

## Reference
[Installing OpenCV on the Ubuntu](http://www.codebind.com/cpp-tutorial/install-opencv-ubuntu-cpp/)

