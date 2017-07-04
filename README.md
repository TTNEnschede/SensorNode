# Nexus-LoRaWAN-Mote
With this code the Nexus will send messages that will be accepted by the LoRaWAN network. Also the Nexus board will listen in receiveslot to if the gateway is sending back a message.

Transmit
- Channel 0: 868.100 MHz
- Datarate 5 = Spreading factor 7, 125 kHz BW
- Full power

Receive
- Channel: 869.525 MHz
- Datarate 3: Spreading factor 9, 125 kHz BW

The timing for the receive slot is handeld in LoRaMAC_V10.cpp

This code will not:
- Change channels
- Change datarates
- Send MAC commands

# Hardware
The Nexus board is fitted with an ATMEGA328P and a RFM95 module.To adapt this code to other hardware change the LoRaWAN_V30.h. From the DIO's only 0,1 and 5 are used

## Bill of materials
-	Arduino Pro Mini (3.3V / 8MHz)
- Hope RFM95
- PCB (ask [Corbo](https://github.com/corbo) or alternatively order it [here](https://oshpark.com/shared_projects/wVpp4ro0))
-	FTDI232 – jumper op 3.3V
- Male headers (30 pins)
- Femal headers (44 pins)
- Male jumper wire as an antenna
- (optional) BMP280 temperature sensor

Impression of finished product:
![Basic LoRa node](https://github.com/TTNEnschede/SensorNode/blob/master/Basic-LoRa-node.jpg)
