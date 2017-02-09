# IoT JumpWay Intel® Arduino/Genuino 101 Dev Kit LED Example

![IoT JumpWay Intel® Arduino/Genuino 101 Dev Kit LED Example Docs](../../images/main/IoT-Jumpway.jpg)  

## Introduction

Here you will find sample device scripts for connecting Intel® Arduino/Genuino 101 and IoT Dev Kit to the TechBubble Technologies IoT JumpWay using the Python MQTT Serial Library. The codes allow you to set up a basic device that allows control of an LED, and an application to communicate with the device / IoT JumpWay, and make the LED flash on and off. Once you understand how it works you are free to add as many actuators and sensors to your device and modify your code accordingly.

## Python Versions

- 2.7

## Software requirements

1. iot_jumpway_mqtt_serial
2. Arduino/Genuino IDE
2. ArduinoJson

## Hardware Requirements

![IoT JumpWay Intel® Arduino/Genuino 101 Dev Kit LED Example Docs](../../images/Dev-Kit-LED/Arduino-101-Hardware.jpg)

1. Intel® Arduino/Genuino 101.
2. Grove starter kit for Intel® Arduino/Genuino/Genuino 101.
3. 1 x LED.

## Before You Begin

If this is the first time you have used the TechBubble IoT JumpWay in your IoT projects, you will require a developer account and some basics to be set up before you can start creating your IoT devices. Visit the following link and check out the guides that take you through registration and setting up your Location Space, Zones, Devices and Applications.

[TechBubble Technologies IoT JumpWay Developer Program (BETA) Docs](https://github.com/TechBubbleTechnologies/IoT-JumpWay-Docs/ "TechBubble Technologies IoT JumpWay Developer Program (BETA) Docs")

## Cloning The Repo

You will need to clone this repository to a location on your Raspberry Pi 3. Navigate to the directory you would like to download it to and issue the following commands.

    $ git clone https://github.com/TechBubbleTechnologies/IoT-JumpWay-Intel-Examples.git

## Install Requirements On Your PC & Arduino/Genuino 101

1. Install the iot_jumpway_mqtt_serial library:

    $ pip install iot_jumpway_mqtt_serial

2. Install the iot_jumpway_mqtt_serial library:

    $ pip install iot_jumpway_mqtt_serial

## Setting Up Your Intel® Arduino/Genuino 101

![IoT JumpWay Intel® Arduino/Genuino 101 Dev Kit LED Example Docs](../../images/Dev-Kit-LED/Arduino-101-Setup.jpg)

First of all you need to connect up an LED to your Intel® Arduino/Genuino 101. To connect the LED you will need a Grove starter kit for Intel® Arduino/Genuino/Genuino 101. 

1. Connect the Grove Starter Kit to your Intel® Arduino/Genuino 101.
2. Connect the LED to pin D5 of your Grove Starter Kit.

## Device Connection Credentials & Actuator Settings

- Follow the [TechBubble Technologies IoT JumpWay Developer Program (BETA) Location Device Doc](https://github.com/TechBubbleTechnologies/IoT-JumpWay-Docs/blob/master/4-Location-Devices.md "TechBubble Technologies IoT JumpWay Developer Program (BETA) Location Device Doc") to set up your device. 

![IoT JumpWay  Intel® Arduino/Genuino 101 Dev Kit LED Example Docs](../../images/Dev-Kit-LED/Device-Creation.png)  

- Download the [TechBubble IoT JumpWay Python MQTT Serial Library Application](https://github.com/TechBubbleTechnologies/IoT-JumpWay-Python-MQTT-Serial-Client/blob/master/application.py "TechBubble IoT JumpWay Python MQTT Serial Library Application") and the [TechBubble IoT JumpWay Python MQTT Serial Library Config File](https://github.com/TechBubbleTechnologies/IoT-JumpWay-Python-MQTT-Serial-Client/blob/master/config.json "TechBubble IoT JumpWay Python MQTT Serial Library Config File"), retrieve your connection credentials by following the link above, and update the config.json file with your new connection  credentials and actuator (LED) setting.

```
	"IoTJumpWaySettings": {
        "SystemLocation": 0,
        "SystemZone": 0,
        "SystemDeviceID": 0,
        "SystemDeviceName" : "Your Device Name",
        "SystemDeviceCom" : "Your Device Com Port"
    },
	"IoTJumpWayMQTTSettings": {
        "MQTTUsername": "Your Device MQTT Username",
        "MQTTPassword": "Your Device MQTT PASSWORD"
    }
```

- Open up the [Arduino/Genuino 101 Dev Kit LED Example](https://github.com/TechBubbleTechnologies/IoT-JumpWay-Intel-Examples/blob/master/Intel-Arduino/Genuino-101/Dev-Kit-LED/Dev-Kit-LED.ino "Arduino/Genuino 101 Dev Kit LED Example") and update the following line with your LED actuator ID retrieved from the steps above, then upload the sketch to your device:

    ```
        const int actuator1JumpWayID = 0;
    ```

## Execute The Python Program

As you have already uploaded your sketch, the program will now be running on your Arduino/Genuino 101. All that is left is to start the Python program with the following line:

    $ python NameOfYourSerialApplication.py 

## Viewing Your Data  

Each time your device detects a person or an intruder, it will send data to the [TechBubble IoT JumpWay](https://iot.techbubbletechnologies.com/ "TechBubble IoT JumpWay"). You will be able to access the data in the [TechBubble IoT JumpWay Developers Area](https://iot.techbubbletechnologies.com/developers/dashboard/ "TechBubble IoT JumpWay Developers Area"). Once you have logged into the Developers Area, visit the [TechBubble IoT JumpWay Location Devices Page](https://iot.techbubbletechnologies.com/developers/location-devices "Location Devices page"), find your device and then visit the Sensor/Actuator page and the Warnings page to view the data sent from your device.

![IoT JumpWay  Intel® Arduino/Genuino 101 Dev Kit LED Example Docs](../../images/Dev-Kit-LED/SensorData.png)

![IoT JumpWay  Intel® Arduino/Genuino 101 Dev Kit LED Example Docs](../../images/Dev-Kit-LED/WarningData.png)

## IoT JumpWay Intel® Arduino/Genuino 101 Examples Bugs/Issues

Please feel free to create issues for bugs and general issues you come across whilst using the IoT JumpWay Intel® Arduino/Genuino 101 Examples. You may also use the issues area to ask for general help whilst using the IoT JumpWay Intel® Arduino/Genuino 101 Examples in your IoT projects.

## IoT JumpWay Intel® Arduino/Genuino 101 Examples Contributors

- [Adam Milton-Barker, TechBubble Technologies Founder](https://github.com/AdamMiltonBarker "Adam Milton-Barker, TechBubble Technologies Founder")

![Adam Milton-Barker,  Intel Software Innovator](../../images/main/Intel-Software-Innovator.jpg)  