View this project on [CADLAB.io](https://cadlab.io/project/24088). 

# Celling lamp
![Version](https://img.shields.io/badge/version-v3-orange.svg)

An AC output controlled by an ESP8266 and powered by AC main


### Firmwares

#### Test

This firmware allows you to test the hardware if needed. It will change the relay status each 400 millisenconds when the button is pressed and it will send the push button status via serial communication.

#### AdafruitIO

This firmware is based in the Adafruit example for comumnicate with its MQTT broker called AdafruitIO. You can see more in <a href="https://io.adafruit.com">io.adafruit.com</a>

In order to use it you should set:

- Your WiFi setting
- You Adafruit user name
- API Key from Adafruit IO
- The MQTT feed which will be used in Adafruit IO

#### MQTT

This firmware allows you to communicate with a MQTT broker. For example, you can install your own MQTT broker in a Raspberry Pi.

This is the actual firmware that I am using at home with this circuit, and it is prepared for being working 24/7. It does:

- Recovery after a power failure.
- Wake up message
- Reconnect message
- Serial debug
- WiFi reconnect if the signal is lost
- MQTT Broker reconnect if the signal is lost

### For future revisions

- `Diode Footprint`: It is wrong in the PCB design
- `ESP8266`: ESP8266 as SoC instead of the ESP8266-12E module
- `UPS`: Uninterrupted Power System. Cesar Fernández idea
- `Capacitive button`: A capacitive external button that acts as the push button

***

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Licencia Creative Commons" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Ceiling lamp</span> by <span xmlns:cc="http://creativecommons.org/ns#" property="cc:attributionName">Enrique Gómez</span> licensed by <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.<br /><br />
