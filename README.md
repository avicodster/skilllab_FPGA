# RVCE FPGA Workshop Repo (Summary)
Welcome to the repository for the RVCE-Workshop on FPGA,UART AND RISC-V. This repo contains all the source codes and the details of the workshop conducted by [Kunal Ghosh](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/).
### Team Members: Aviral, Bhini

We used VSDSquadron FPGA Mini to achieve the above objectives.
## VSDSquadron FPGA Mini(About the Board)
The VSDSquadron FPGA Mini (often referred to as "FM Mini") is a compact, low-cost FPGA-based prototyping board designed primarily for semiconductor and VLSI education, as well as rapid prototyping in the open-source hardware community.

### **Key features:**
- 32-bit QingKe RISC-V2A processor core
- Supports 2 levels of interrupt nesting
- Up to 48MHz system clock frequency
- 16KB Flash memory
- 2KB SRAM
- Operates at 3.3V or 5V supply voltage
- Multiple low-power modes: Sleep, Standby


### Objectives:

1. FPGA VDI Installation
   This covers setting up the VDI environment on an FPGA board, preparing it for development and testing of hardware projects.We installed ORACLE virtualbox for creating a virtual machine which helped us further execute the experiments.

2. Communicate via UART using `picocom`.

3. LED Blinking and UART Loopback
   A hands-on introduction to digital I/O with FPGA: blinking an LED helps verify GPIO control, while UART and UART loopback demonstrate serial communication and data verification.
4. Real-time Sensor Data Acquisition or DPLL
   Involves capturing and processing sensor signals using FPGA in real-time or implementing a Digital Phase-Locked Loop (DPLL) for timing synchronization in digital systems.
***
### Requirements:
Installing, cloning and running the projects.
### Cloning the Github Repository:
```
https://github.com/avicodster/skilllab_FPGA.git
cd skilllab_FPGA
```
### **Clean Previous Builds**

Before starting a new build, clean old files using:

```sh
sudo make clean
```

This removes any previous bitstream files.
### **Build the FPGA Bitstream**

To **synthesize the design and generate the bitstream**, run:

    sudo make build
### **Flash the FPGA**

Once the bitstream is built, upload it to the FPGA using:

```sh
    sudo make flash
```
This step is to be repeated always so that the board is reporgrammed and the current program is only executed on the board.
***
### Usage of Each project:
####  1.LED Blinking
```
cd led_blinking
make flash
```

***
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
***

## Acknowledgment  

I would like to express my gratitude to:  

- **[Kunal Ghosh](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/)** for his valuable contributions to open-source VLSI education and FPGA learning resources.  
- **[K M Skanda](https://www.linkedin.com/in/k-m-skanda-541a02291/)** for helping me learn and execute the above projects and spreading information of using the VSDSquadron FPGA mini.

## Connect with me
**LinkedIn:** [Aviral Jain](https://www.linkedin.com/in/aviral-jain-492399255/)

**Email:** [aviraljain594@gmail.com]
