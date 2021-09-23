####---UNDER CONSTRUCTION---#### mqtt-sn in raspberry pi 
project: website
# mqtt-sn in raspberry pi 
project: website
I will cut all the definition and how data were handle over MQTT and go direct to the main setup
Encountering problem
As blogs or other sources have mentioned, the MQTT and MQTT-SN basic difference in initial implementation is in MQTT-SN, you have to setup a GATEWAY to BROKER, and BROKER if you're using RSMB instead of only configuring the BROKER (Paho, AWS) like MQTT. 

I then found out this blog (https://jpinjpblog.wordpress.com/2018/02/08/trying-mqtt-sn-on-raspberry-pi/). JJPP has also guided it thoroughly and more importantly, the GATEWAY is working.
 


Image from this PDF

As aforementioned and from image, we need 3 things to have it functional:
	1. MQTT-SN GATEWAY, in here I am using Eclipse Paho MQTT-SN from Steve
	2. MQTT-SN Broker that supports MQTT-SN, in here I am using RSMB
	3. MQTT-SN Clients, in here I am using Steve's file for testing
	
1. Setting up the GATEWAY
	• How to build the GATEWAY
	$ git clone https://github.com/eclipse/paho.mqtt-sn.embedded-c   
	$ cd paho.mqtt-sn.embedded-c/MQTTSNGateway       
	$ make   
	$ make install   
	$ make clean 
	
	• How to execute the GATEWAY
	Before executing, we need to configure the config file 
	<>
	Executing
	<>
	
	2. Setting MQTT-SN Broker

