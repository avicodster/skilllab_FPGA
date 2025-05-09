# RVCE FPGA Workshop Repo (Summary)
Welcome to the repository for the RVCE-Workshop on FPGA,UART AND RISC-V. This repo contains all the source codes and the details of the workshop conducted by [Kunal Ghosh](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/).
### Team Members: Aviral, Bhini

### Objectives:

1. FPGA VDI Installation
   This covers setting up the VDI environment on an FPGA board, preparing it for development and testing of hardware projects.We installed ORACLE virtualbox for creating a virtual machine which helped us further execute the experiments.

2. Communicate via UART using `picocom`.

3. LED Blinking and UART Loopback
   A hands-on introduction to digital I/O with FPGA: blinking an LED helps verify GPIO control, while UART and UART loopback demonstrate serial communication and data verification.
***
### Requirements:
Installing, cloning and running the projects.
### Cloning the Github Repository:
```
https://github.com/avicodster/skilllab_FPGA.git
cd skilllab_FPGA
```

### Usage of Each project:
####  1.LED Blinking
```
cd led_blinking
make flash
```
####  UART Loopback
```
cd uart_loopback
make flash
sudo make terminal
```
***
### Issues faced
```
sudo: picocom: command not found
make: *** [Makefile:27: terminal] Error 1
```
### Issue fixed by:
We need to install 'picocom' using the below commands:
```
sudo apt update
sudo apt install picocom
```

