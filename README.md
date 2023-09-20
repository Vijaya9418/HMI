# HMI  AND  AOSP ARCHITECTURE

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


**AOSP main folder:-**
1. ART :- Android runtime, this folder contains the modules realated to android runtime like dalvik virtual machine, dex compilers, JVM etc.
2. bionic:- It is a android custom C library which contains, math library,Clibrary, dynamic linker etc.
3. bootable:- it contains boot related code. bootloader,OTA(Over the Air update),recovery mechanism.
4. build:- it contains the build system. some shell files such as envsetup.sh, common shell scripts, make and soong folders here.
5. compatiblity:- CDD(Compatibility definition document) it is a documentation folder.
6. cts:- android compatibity test suit standards.
7. Frameworks:- Android framework is very important which are written in java and C++. where we can find all the system service and core implementation of android.
   framework/base/core/java/android/content/

**AIDEGen:-**

It helps to automates the project setup for developers to work with C/C++ and java project in popular IDE. developers no longer needs to manually configure an intellij setup.

**why dalvik is converting into APT or what is the difference between Dalvik and ART?**

Both is runtime library, but ART(Android run time) have more advantages than dalvik, becoz in dalvik byte codes converts the code into machine language which will slow down the running efficiency of the code.

But with the help of ART the code of all the appliaction will be pre compiled into machine code, when it is first installed in the device.


**What is SELinux?**

It stands for Security Enhance linux. which is a set of rules which will imporve the security of your system.<br>
It is a labelling system, every process has a label.we lable the process in order to enhance the security of a process.

MAC(Mandatory Access Control).<br>
DAC(Discretionary Access Control).<br>
these both are most important access control, the diff between them is that how they provide the access to the system.

MAC determines that which subjects(android process) can access specific data objects(files,sokets).<br>
DAC the owner of the object determines which subject can access the object.

**.te** file we write the rules for SELinux policies.

**Boot Loader path?**

![boot loader](https://github.com/Vijaya9418/HMI/assets/56352158/5aabc485-eeb3-4fe5-b316-1f332c19a4cd)

1. In this first step is the power on and the system starts which is hardcoded in the ROM and this will load the boot loader into the RAM.
2. Boot loader is a small program that runs before the operating system starts whose main function is to start the system OS.
3. Once the lunux kernel starts it loads all the system like cache, audio, video drivers.
4. When the kernel finishes to load these systems, iy looks for the init.rc file and then it starts the root process.

So, this init process does 4 things:-
1. It will create some folders and mount the devices.
2. It will setup SELinux policies.
3. Initialize and starts the property service.
4. parse the init.rc file and starts the zygote process.

init process:- In this we have main file which include 3 main properties which are:-

1. FirstStageMain :- it is responsible for creating the directory and mounting the devices.
2. SELinux:- It loads all the set of selinux policies and sets the enforcement of SELinux polocies.
3. SecondStageMain:- this is implemented in init.cpp in whcih main method is propertyInit() which will initialize the property within the system.


5. Zygote process:- In android system, the android runtime, dalvik virtual machine,app process, system service are all done by zygote process. It uses the fork mechanism for system service and app process.

fork mechanism:- it will create the new process by duplicating the exisisting process from which it is called. It contains init.zygote64.rc file in which the code is written in android.

inside init.rc file there is one command written which is **class_start main** which will start the zygote main process.

6. zygote starts the system server which is done through fork system server.inside which we have different services responsible for starting the services like audio, camera, etc.



Soong build system:-

So we have varioud build system like soong, make, ninja etc. So we can see that we hav two type of build files, file.bp(blueprint) and file.mk(make), why we have two type of files. 
because before android 7 we used .mk file for building but it was error prone, pretty slow and unscallable and was difficult to test. then google decided to use the new build system called soong.It is similar to the json format. which basically converts the *.bp files to *.ninja files

.bp --> soong build logic --> .ninja --> ninja build system --> .so,.apk,.jar


![soong](https://github.com/Vijaya9418/HMI/assets/56352158/5bc73f40-828b-4b13-9e06-5baf059c4f51)




first step for the build is to execute the envsetup.sh file for this we use the command source build envsetup.sh<br>
hmm is a command which we can run to see all the available command presnt<br>
then the lunch command which shows you the lunch menu(build variants avaibale to AOSP.


What is an overlay?

In simple words, runtime resource overlay is a package that changes the resource value of a target package. "An apk with only one resource file in it".

It can technically overlayed all the resource files like layouts, strings,colors,drawables and other resource file. with the help of which we can changes the look and feel of an application.

We cannot overlayed any source code files present in java and kotlin file.

![rro](https://github.com/Vijaya9418/HMI/assets/56352158/c2e2c237-32ad-4898-959f-18bedea227c9)


**What is ADB?**

It is a android debug bridge which is a command line rule that lets us to communcate with an android device. It is the most imp tool that will we use working with android studio. <br>
It is widely used for debugging, installing, logging the app and also to access the unit shell of a device.

steps,<br>

1. adb command to invoke the client.
2. adb daemon which runs the commands on a device which runs as a background process through each device.
3. adb server which manages the communication between the client and the daemon.

   1. if you want to start the adb from the root - adb root

   
  2. adb start-server<br>
   adb stop-server<br>
   adb kill-server<br>

3. exit - to exit the shell.

4. If you need to connect to the device then adb -d shell.
5. If you need to connect to the emulator then adb -e shell.


**What is boot animation?**

It is the animation screen or the splash screen when we start the emulator. in this we write 6-7 steps which are in numberic form and add the animation file in the same folder and compress it, then we run some commands for boot animation.




**what is system services?**

system services acts as a bridge between the harware abstraction layer and applications.
for example:- when we take pictures through the camera we communicate through the system services to the camera hardware drivers.

There are manily tow types of system servers:-

1.Media server.(it involves media player, camera, audio player etc.)
2. System server.(it involves search, window, notifications etc.)


**what is KML?**<br>
KML(keyHole markup language) is a file format used to display geographic data in an Earth browser such as Google Earth.



**What is Binder?**

It is a interprocess Communication (IPC) in android.It helps you to communicate and share the services with earch other.<br>

Example:-  processes in android have different spaces, so one process cannot be access the other process which is called process isolation.However, if a process wants to offer some useful files or services to another process then for this we need some communication , so for this we use IPC.

If we want to communicate between the system apps and android apps, then we need a binder to communicate with each other.


**what is shared library addon?**

The purpose of shared library addon is to share some of the library with your embeded device may be to a vendor or your external partner. lets suppose we are working with OEM like samsumg so there might be so many vendors, so if we want to provide the HAL to your partner , so what we can do is , we can create a shared library addon which we can embed to the Sdk . and store it in the web, and your partner can you it from there.


to build the add-on:-

make -j8 PRODUCT- yourLibrary- sdk_addon


![image](https://github.com/Vijaya9418/HMI/assets/56352158/09e04c48-a0bb-43da-b807-09ed6f27c6c8)






   














 







