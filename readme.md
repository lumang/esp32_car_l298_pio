# TODO 
- [√] Joystick control toys car 
- [] camera toys car
- [] asr control toys car
# get receive mac 

get receiver mac address

# receive
main.receive-->main.cpp
build 
upload

# sender
main.sender-->main.cpp
build 
upload
# hardware 
- esp32-wroom * 2
- l298 module * 1
- toys car kits   * 1
- some  Connecting cables
- battery 1.5 *4
- joystick     * 1

# error
```shell
Succes: Initialized ESP-NOW
E (133) ESPNOW: Peer interface is invalid
Failed to add peer
```
main.sender
```cpp
esp_now_peer_info_t peerInfo;// global variable
```

# learn esp-now 
[reference](https://randomnerdtutorials.com/esp-now-esp32-arduino-ide/)


 Here’s what we should include in the sender sketch:

>Initialize ESP-NOW;
Register a callback function upon sending data – the OnDataSent function will be executed when a message is sent. This can tell us if the message was successfully delivered or not;
Add a peer device (the receiver). For this, you need to know the receiver MAC address;
Send a message to the peer device.

On the receiver side, the sketch should include:

>Initialize ESP-NOW;
Register for a receive callback function (OnDataRecv). This is a function that will be executed when a message is received.
Inside that callback function, save the message into a variable to execute any task with that information.
ESP-NOW works with callback functions that are called when a device receives a message or when a message is sent (you get if the message was successfully delivered or if it failed).