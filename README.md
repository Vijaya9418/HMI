# HMI

![main HMI](https://github.com/Vijaya9418/HMI/assets/56352158/a10ef1ba-4e11-44c9-9d98-23d75e232732)


**What is HMI?**

The full form of HMI is Human Machine Interface which is a component and features for car hardware and software applications that allows driver and passangers to engage with the vehile as well as the outside world.

Or in simple words we can say that an HMI is a screen that allows operator to interact with control system which is controlling the process

It has operating pannel and a monitoring screen.


It is used as an operator control panel to PLCs, RTUs, and in some cases directly to IEDs.

It replaces manually activation of switches, dials.

Some examples of common Human Machine Interface devices that we encounter in our daily lives include touchscreens and keyboards. 

A computer program that manages or organize the several other program at the same time. 

![HMI overview](https://github.com/Vijaya9418/HMI/assets/56352158/8b953ce5-7111-477e-b5fa-eeaeb678e23e)


What is PLC?

The full form of PLC is Programming Logic Controller  which process the given information(Input), execute the given command or instruction given from the program and deliver the result output.


**Is a HMI a PLC?**

One of the key differences between a PLC and an HMI is their primary function. While a PLC is responsible for executing control logic and managing inputs and outputs, an HMI focuses on providing a user-friendly interface for operators to interact with the system.

![HMI](https://github.com/Vijaya9418/HMI/assets/56352158/0bc94b9c-a234-4ffc-839a-43a3cc4cd156)


**How HMI is connected to PLC?**

HMI & PLC : they are generally connected throw a **Profibus** cable for real time communication.


Human Machine Interface (HMI) and Programmable Logic Controller (PLC) interface with each other by using a communication protocol. This allows the HMI to display real-time information and receive input from the operator, while the PLC can control the operation of the machine or process. Common communication protocols include Modbus, Profinet, and Ethernet/IP. The HMI and PLC can also interface through other industrial protocols such as OPC UA, MQTT, and HTTP. It is important to ensure that the HMI and PLC are compatible and have the same communication protocol in order to establish a successful interface.


![HMI and PLC connection](https://github.com/Vijaya9418/HMI/assets/56352158/dea1cf19-e007-48d1-a239-7f45bd6eb315)

The person programming the HMI has to program each indicator and button to specific input and output address of PLC.So the PLC and HMI should be compatiple.


**what is a SCADA?**

The full form of SCADA is Supervisory Control and Data Acquisition which is responsible for monitoring and controlling the field devices that we use in remote places.

HMI is simply a part of SCADA

![scada](https://github.com/Vijaya9418/HMI/assets/56352158/ac6a9a4d-9486-4ef2-ba7d-14f5cbdbc075)


 There are two basic types of HMI software: supervisory level and machine level.
 

** what is AOSP architechture?**

AOSP stands for android Open System Platform, which maintains the complete software stack. It is a publically available and modifiable source code whcih anyone can download and modify the AOSP for their devices. It includes middleware, operating system and key applications, combination of libraries, API that let the developer to build their android application.

The AOSP framework is written in Java and is designed to be flexible and extensible, allowing developers to build and run a wide range of applications on Android devices.

AOSP can't provide support for apps that require backend services, such as a cloud messaging or advanced location services app. 

The software stack for AOSP contains the following layers:



<img src="https://github.com/Vijaya9418/HMI/assets/56352158/3100f82f-c086-487a-bbfa-daefd7d2f732" width="300">,<img src="https://github.com/Vijaya9418/HMI/assets/56352158/12451d56-ac89-4458-b42b-6d4b2cd659a6" width="300">


There are 4 main components of AOSP architecture:

Linux Kernel

Libraries

Application Framework

System Applications.


Linux kernel:- It is the bottom most layer and is a core of android architecture.It provides various features, such as Security, Memory Management, Multitasking, Device Management, and Process Management. It also provides the basic functionality of the kernel.

Libraries:-This layer in Android AOSP provides the necessary infrastructure for applications to run. It consists of a set of libraries and Android runtime.

Application framework:- The application framework provides the APIs that allow developers to create Android apps, as well as a set of standard app components (such as activities, services, and content providers) that developers can use to build their apps.

System Application:- It is the top-most layer of Android AOSP architecture which is the user interface. This layer has native Android applications and third-party installed applications, and it also works around managing user input. 

Repo:- It is a source code manager just like git, it is build over Git in order to manage the code more efficiently.


**common aosp commands**


gettop - get the top aosp directory. example :- cd $(gettop)/framework/base <br>

croot - change the current directory to the root AOSP.<br>

mm - Build the package.<br>

cgrep - only matches the source files in C/C++ language.<br>

jgrep - only matches the source files in java language.<br>

resgrep - only matches the XML file present in XML folder.<br>

godir - goto a directory having the provided file.<br>


AIDEGen:-

It helps to automates the project setup for developers to work with C/C++ and java project in popular IDE. developers no longer needs to manually configure an intellij setup.

**why dalvik is converting into APT or what is the difference between Dalvik and ART?**

Both is runtime library, but ART(Android run time) have more advantages than dalvik, becoz in dalvik byte codes converts the code into machine language which will slow down the running efficiency of the code.

But with the help of ART the code of all the appliaction will be pre compiled into machine code, when it is first installed in the device









 







