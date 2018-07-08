# Image Processing on System on Chip FPGA devices using LabVIEW

A research project to implement a real-time image processing system on a System on Chip device in the LabVIEW graphical programming language.

**Author: Gergő Papp-Szentannai**

## Description

This work is the practical part of my License Thesis, entitled "Image Processing on System on Chip FPGA devices using LabVIEW". This project was documented at the Technical University of Cluj-Napoca, Computer Science Department under the supervision of Mihai Negru and Vlad Miclea. The thesis was delivered at July 9, 2018.


## Getting Started

These instructions will get you a copy of the project up and running.

### Requirements

#### Hardware

Development PC:
  - You must develop from a Windows-based PC (I used Windows 10 (64 bit), gut other versions should work as well).

Target device:
  - NI myRIO-1900, with the following "extras":
    - a generic USB webcam
    - USB cable to connect the myRIO to the PC
    - power source for the myRIO

#### Software

The following software must be installed on the Windows development PC:
  - LabVIEW 2017* Development Edition, including the following modules:
    - LabVIEW Real-time module
    - LabVIEW FPGA module
    - myRIO add-on
    - LabVIEW Vision Development module
  - LabVIEW 2017 FPGA Module Xilinx Compilation Tool for Vivado 2015.4

On the myRIO, we must also install necessary software (beside the software packages that are automatically shipped):
  - NI Vision RT
  - LabVIEW Real-Time
  - NI IMAQdx (image acquisition drivers for the webcam)
  
* I used LabVIEW 2018, but later versions should also work.

### Installing and running

#### Setting up the development environment
  * Clone or download the source
  * Open SoC Image Processing Project.lvproj
  * Configure the IP address of the connected myRIO device under the properties of the "NI-myRIO-1900-Gergo" target
  * Connect to the myRIO target 
#### Building and Deploying
  * Run the “RT Main” VI under the "NI-myRIO-1900-Gergo" target
  * The RT VIs will probably be recompiled, however the FPGA VI should be ready to be used (if not, recompile the missing FPGA VI - an error should indicate what to do)
#### Validating results
  * Once the VI is running you can visualize the result of the system on the front panel
  * You can also notice the FPS indicator, that indicates the performance of the system
  * On the right image you should see a “blurrier” image than on the left one

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* The SW (LabVIEW) and HW (myRIO) components required for this project were provided by National Instruments
