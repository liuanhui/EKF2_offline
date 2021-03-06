# Example using ECL offline

I use Myekf2.cpp. instead of main.cpp.  
This version use EKF without GPS velocity.  
If we have GPS velocity, we should cover the folder EKF with the  original code.   
In order to run normally, we need to have a folder called "data" in the root directory.
And the "data" should have :   

imu_data.txt  
gps_data.txt  
mag_data.txt  
baro_data.txt  


### Build
```
mkdir build/
cd build/
cmake ../EKF
make
```

### Usage
```
cd build
./myekf2
```


# ECL

**Very lightweight Estimation & Control Library.**

[![DOI](https://zenodo.org/badge/22634/PX4/ecl.svg)](https://zenodo.org/badge/latestdoi/22634/PX4/ecl) [![Build Status](https://travis-ci.org/PX4/ecl.svg?branch=master)](https://travis-ci.org/PX4/ecl)

This library solves the estimation & control problems of a number of robots and drones. It accepts GPS, vision and inertial sensor inputs. It is extremely lightweight and efficient and yet has the rugged field-proven performance.

The library is BSD 3-clause licensed.

## Building EKF Library

### Prerequisites:

  * Matrix: A lightweight, BSD-licensed matrix math library: https://github.com/px4/matrix - it is automatically included as submodule.


By following the steps mentioned below you can create a shared library which can be included in projects using `-l` flag of gcc:

```
mkdir Build/
cd Build/
cmake ../EKF
make
```

