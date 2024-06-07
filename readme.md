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