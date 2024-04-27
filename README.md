# esp-idf-websocket-camera
Take a picture and Publish it via WebSocket.   
This project use [ESP32 Camera Driver](https://components.espressif.com/components/espressif/esp32-camera).   

ESP32 works as a WebSocket server.   
Use your browser as a WebSocket client.   
```
+----------+               +----------+               +----------+
|          |               |          |<-----Get------|          |
|  Camera  |<---Capture--->|  ESP32   |               |  Browser |
|          |               |          |----Picture--->|          |
+----------+               +----------+               +----------+
```

# Hardware requirements
ESP32 development board with OV2640 camera.     

# Software requirements
esp-idf v4.4/v5.X.   

```
# Install project step by step
git clone https://github.com/thienphu0904/esp_cam_websocket.git
git checkout master
cd esp-idf-websocket-camera
idf.py set-target {esp32/esp32s3}
idf.py menuconfig

idf.py flash monitor
```

# Take pictures using Browser
ESP32 acts as a WebSocket server.   
Open index.html included in this project.   
Push connect server button.
Result: 
![5f9a3662-0495-4d76-986d-cbf305bc0272](https://github.com/thienphu0904/esp_cam_websocket/assets/167863085/363fe215-0172-430e-94db-d2340074e316)
