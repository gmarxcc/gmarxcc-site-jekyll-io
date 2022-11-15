---
title: Mobile Devices
author: Gerardo Marx
layout: lectures
---

# Mobile Devices for Master Degree
This is the web for Mobile Devices Course at **Master Degree August 2022**, the course is mainly focused into the Signal Processing Lane. The course requires basic programming and Linear Algebra knowledge.

![SBC](https://www.gadgetronicx.com/wp-content/uploads/2016/12/single-board-computers.jpg)

## Introduction
The mobile devices (md) course needs a system or an embedded system to implement and understand how a md can be programmed and used as a main stream to gather information. Thus, it is highly recommended to have a device similar to the BeagleBone or RaspBerry boards.

The main idea is to learn how a Linux based operative system can be used to develop hardware-access applications from terminal or windows systems.

The lectures of this course will be mainly provided by Git repositories to allow the student reproduce the complete task developed by the instructor. Thus, it is highly recommended to learn the basics of the Git system. 



# 1. Introduction to the beagle boards
We are going to work with **Single Board Computers** or **Portbale Embedded Systems**, both systems are really close to Mobile Devices that works (in most of the cases) with Embedded Linux.

There are several options to select: Raspberry Pi, DragonBoard, ASUS Tinker Board, cRio, LattePanda, Intel Nuc, Libre Computer, ESP32, NanoPi, BeagleBone, Onion, Intel Galileo, and
more.

Of course the selected option depends on the final application or applications. **For this course,
the best options are the: 1) The BeagleBone Black, 2)BeagleBone Nano, and 3) Raspberry Pi; in this priority order.**

**I recommend the BeagleBone Boards because its support by groups and forums, available tools, and the huge possibilities to work with.**
 
*If you want to know prices and more details please visit
[Best single computers](https://www.slant.co/topics/1629/~best-single-board-computers)*

## 1.1 Basics of Linux
*GNU Linux* is the technical name that receives the Unix based operative systems(OS). The OS are the combination of several open-source projects, the most relevant are the GNU environment (Richard Stallman) and the OS kernel known as *Linux* (Linus Torvalds). 

Nowadays, the word Linux is used to refer to the complete OS instead of the kernel, however, the correct name is GNU/Linux. Thus, the GNU/Linux OS are commonly distributed as compendium of packages or programs, these is known as a distro or distribution. Each distribution has a minimum of packages previously installed to work with. 

GNU-Linux is a wide used operative systems in several engineering applications, data science server/computers, real time application, embedded systems, and more. According with [^1], GNU/Linux distributions are used in the 78% of the most important servers in the world.

Therefore, I recommend to be in full contact with the work-flow of GNU-Linux. As you may know, there are several Linux distributions to work with, and this distribution must be selected by considering the final application. 

Then, if you are a first user of GNU-Linux, I recommend to use Ubuntu. If you have already used a GNU-Linux distribution, I recommend to work with Debian, or if you can handle it a little bit more, use Arch.

Thus, you will need a way to work with many Linux distributions to develop applications. To manage this, you can install a physical instance of each distro in your computer (the best option, but take with care), otherwise you can install **the Docker system** to have many distros without problems as sand-boxes, or as a last option work with virtual machine instances; not the best option but the easiest.

The full contents of the Lecture and examples is in the repository [Basics of Linux](http://gmarxcc.com:8088/Mobile-Devices-ITM/basics-of-linux.git)

## 1.2 Git and Vim introduction
Along this lecture two important tools are introduced: GIT version control system and Vim source text editor. Details about the lectures are in the next repositories:

- [Git and Vim in terminal](http://gmarxcc.com:8088/mcie-rs101/git-intro.git)
- [Git using a GUI application](http://gmarxcc.com:8088/mcie-rs101/git-introduction-gui.git)

## 1.2 Board connections and basic comunnication 

We have already used the ssh protocol to connect our computers to the Beagle/Rasp board. Nevertheless, it is important to understand and use the ssh-keygen tools and how to improve a little bit our boards installing VIM and Oh-my-Bash:

- [Basic connection](http://gmarxcc.com:8088/Mobile-Devices-ITM/basic-connection/src/branch/master/README.md)
- [Oh-my-Bash and Vim](http://gmarxcc.com:8088/Mobile-Devices-ITM/ohmybash-vim/src/branch/master/README.md)


# 2 Basics of programming  

## 2.1 Bash programming concepts
In the next repositories you can find a basic guide to access and test the onboard LEDs (BeagleBone only), and also a basic script to test the bash programming concepts:

- [LED Bash Guide](http://gmarxcc.com:8088/Mobile-Devices-ITM/beagle-bash)
- [LED Bash Script](http://gmarxcc.com:8088/Mobile-Devices-ITM/Bash-LED)

## 2.2 C programming concepts

A long this lecture, let us test a basic *Hello World* scripts on C by turning ON or OFF the USR3 LED. The idea is to remember the compilation chain process to obtain an executable application. 

- [Basic guide to test on board LEDs using C](https://github.com/ITM-MCIE/led-c)

# 3 SBC's Services	
## 3.1 A Web and CGI server

The lecture presents the basic procedure to install and configure an Apache Web server. Then, a basic CGI script is running on the server. Finally, we discuss the basics of arduino IDE to work with the ESP32 iot device :

- [Web and cgi server](http://gmarxcc.com:8088/Mobile-Devices-ITM/web-server)
- [ESP32-blinking](http://gmarxcc.com:8088/Mobile-Devices-ITM/esp32-blinking-serial) 



<!---
In order be ready for basic programming directly on the BBBs, we must check that some tools are already installed on our boards: Python, g++ compiler and make tools. 

First check that python is installed by

```
debian@beaglebone-black:~$ python --version 
Python 2.7.16
``` 

any version later than 2.6 is ok.

Next, check the g++ compiler version installed in your board:

```
debian@beaglebone-black:~$ g++ --version 
g++ (Debian 8.3.0-6) 8.3.0
Copyright (C) 2018 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```
at least version 8.3.0 is recommended. 

Finally, check the version of the `make` tool: 
```
debian@beaglebone-black:~$ make --version 
GNU Make 4.2.1
Built for arm-unknown-linux-gnueabihf
Copyright (C) 1988-2016 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
```
version 4.2.1 is preferred. If you do not have these tools installed use:
```
$ sudo apt-get install g++
$ sudo apt-get install make
$ sudo apt-get install python
```
only the missing packages. If you have installed the packages, but versions are lower update the packages by using:

```
$ sudo apt-get upgrade g++
$ sudo apt-get upgrade make
$ sudo apt-get upgrade python
```
to upgrade the requiere package.


## 2.1 Version Control System Git

## 2.2 


# 3 IoT
# 4 Cross-Compilation 
# 5 Projects

### Basic USB connection

[^1]: IDC http://www.tercerainformacion.es/spip.php?article15580
ing a GUI](http://gmarxcc.com:8088/mcie-rs101/git-introduction-gui.git)


## 1.3 Board connections and basic comunnication

## 1.4 An introduction to services

# 2 Basics of programming  
## 2.1 Version Control System
# 3 IoT
# 4 Cross-Compilation 
# 5 Projects

### Basic USB connection

[^1]: IDC http://www.tercerainformacion.es/spip.php?article15580

-->

