# Iot JumpWay WebSockets MQTT Samples
======================================

PLEASE NOTE: Due to a conflict with the security fix for the recent Padding Oracle in OpenSSL CBC Ciphersuites, this feature is currently unavalable.

TechBubble Tecnologies Internet of Things (IoT) JumpWay is a web platform that allows anyone to connect IoT devices such as Raspberry Pi, Intel Galileo, Arduino, ESP8266 and even phones,PCs, Macs and laptops to the Internet of Things. The various IoT JumpWay libraries and samples allow you to connect devices and sensors to the IoT JumpWay and control/monitor sensors/actuators and data to and from the devices.

The WebSockets MQTT examples allow developers to communicate from web and desktop applications by sending commands to devices via the TechBubble IoT JumpWay MQTT Broker.

# Before You Begin

Make sure that you have a device already connected to the TechBubble IoT JumpWay. If you are using the LED sample you will need to install the following library and set up a device with your LED.

  https://github.com/AdamMiltonBarker/TechBubble-Iot-JumpWay-Python-MQTT
  
# Installation

These samples are very easy to setup, you can either run the locally on your PC/Mac/Laptop etc or you can upload them to a webserver.

##LED Sample Connection Credentials
------------

First of all you need to add your application connection credentials. You will be provided these credentials when you set up an application in the IoT JumpWay GUI.

```
var mqttOptions = {
	locationID: "YOURLOCATIONID",
	applicationID: "YOURAPPLICATIONID",
	applicationName: "YOURAPPLICATIONNAME",
	userName: "YOURAPPLICATIONMQTTUSERNAME",
	passwd: "YOURAPPLICATIONMQTTPASSWORD"
};
```

##LED Sample Device Details
------------

The final step is to add the device details that you will be controlling.

```
$('body').on('click','#subscribe',function(){			
	websocketclient.subscribeToDeviceCommands( {
		locationID: "YOURLOCATIONID",
		zoneID: "YOURZONEID",
		deviceID: "YOURDEVICEID"
	});			
}); 
```

Once the above are set up, you are done, either double click the index.html file on your PC/Mac/Laptop or upload the structure to your webserver and visit the page.


