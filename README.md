# Easy LoRa Node - Tracker
A wearable LoRa node with battery with deepsleep less than 15uA.

# 1. Specifications
## 1.1 Overview
![Easy LoRa Tracker - Overview](https://user-images.githubusercontent.com/29994971/104403543-516f5d00-558b-11eb-9928-45658bd5ce4e.jpg)

## 1.2 Components
![Easy LoRa Tracker - Component](https://user-images.githubusercontent.com/29994971/104406783-a9f62880-5592-11eb-8292-f9eb78175576.jpg)


# 2. Usage guides
## 2.1 Pin mapping
LED
* LED                   22 // LOW is off, HIGH is on.

Button
* BTN                   39 // Pressed is HIGH. Keep LOW.

LoRa
* LORA_POWER            21 // LOW to off, HIGH to power on LoRa module
* LORA_SS               25 // Have pull up resistor
* LORA_SCK              18
* LORA_MOSI             23
* LORA_MISO             19
* LORA_DIO0             26
* LORA_DIO1             35
* LORA_DIO2             34
* LORA_RESET            27

Battery
* BAT_METER             36 // To measure battery voltage

Other GPIOs
* Connect directly to ESP32-Pico-D4: https://www.espressif.com/sites/default/files/documentation/esp32-pico-d4_datasheet_en.pdf

## 2.2 Upload sketch
* To install UART driver for CP2012: https://github.com/IoTThinks/EasyLoRaGateway_v2.1/wiki/Install-USB-UART-driver
* To install Arduino IDE:
* To install ESP32 for Arduino IDE: https://github.com/IoTThinks/EasyLoRaGateway_v2.1/wiki/Setup-Arduino-IDE-and-ESP32
* To install LoRa library: https://github.com/sandeepmistry/arduino-LoRa

![Easy LoRa tracker - Compilation](https://user-images.githubusercontent.com/29994971/104406345-af06a800-5591-11eb-9424-496a6c1f9ca7.png)

## 2.3 Sample codes
* Test code for receiver: https://github.com/IoTThinks/EasyLoRaNode_Tracker/tree/main/ESP32SimpleReceiver_920Mhz
* Test code for sender: https://github.com/IoTThinks/EasyLoRaNode_Tracker/tree/main/EasyLoRaMiniNodeTest-Batch1

## 2.4 LoRa Power
To turn on/off LoRa power
* Be sure LoRa power is on before sending LoRa messages
* To turn off LoRa power if not in use or in deep sleep to save power.
![LoRa Power](https://user-images.githubusercontent.com/29994971/104407327-ed9d6200-5593-11eb-9511-557aa6ae8a1b.png)


## 2.5 Battery
### 2.5.1 No battery
The node can be powered via usb port 5v or Vin (3.6v-5v)
* The charge LED will be blinked.

### 2.5.2 Connect battery
Recommended battery:
* Lipo battery 4.2v with under-voltage protection is recommended. 
* 18650 battery is NOT recommended as it does not have under-voltage protection.

### 2.5.3 Charge battery
To connect the battery and plug the USB jack into 5v USB
* You can still use the node during the charging
* It takes around 2 hours to fully charge

### 2.5.4 Battery protection

### 2.5.5 Measure battery voltage

### 2.5.6 Measure battery current during deepsleep


## 2.6 Assemble everything
