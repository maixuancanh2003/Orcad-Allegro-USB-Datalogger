# USB Mini Storage Datalogger with USB SSD - ESP32

## Introduction

The **USB Mini Storage Datalogger** project utilizes **ESP32** to interface with **USB SSD** for external data storage. The system is designed with the following features:
- **USB Communication**: Connect external SSD via USB standard.
- **Low Power**: Energy-saving mode, activated only when data transmission is needed.
- **USB Noise Immunity**: Complies with EMC standards to ensure stable data transfer.
- **Web Interface**: Developed with HTML to send files via HTTP.
- **PCB Design Software**: **OrCAD Allegro v17.4**.

## Hardware

### Microcontroller
- **ESP32**: WiFi + Bluetooth, supports USB Host.

### Storage
- **USB SSD**: High-speed storage via USB interface.

### Connectivity
- **USB 2.0/3.0**: Connect SSD to ESP32.

### Power Supply
- **5V/3.3V**: Powered via USB port or external source.

### Noise Immunity Design
- Uses **Ferrite Bead** and **Shielding** to minimize interference.
- **USB signal lines** are designed with differential pairs to meet USB standards.

## Software

### Firmware (ESP32)
- **USB Host**: Read/write data from USB SSD.
- **HTTP Server**: Enables file download via the web interface.
- **Low Power Mode**: Utilizes ESP32’s Deep Sleep function.

### Web Interface (HTML)
- Download data from SSD via HTTP.
- User-friendly interface displaying storage capacity and system status.

## Installation

### Requirements
- **ESP32 DevKit**
- **USB SSD**
- **OrCAD Allegro v17.4**

### Firmware Flashing Guide
```bash
esptool.py --chip esp32 --port /dev/ttyUSB0 write_flash -z 0x1000 firmware.bin
```

### Accessing the Web Interface
1. ESP32 will generate an IP address after connecting to WiFi.
2. Open a browser and navigate to: `http://<ESP32_IP>`.

## 📸 Project Images
| View        | Image                             |
|-------------|-----------------------------------|
| **Top View**    | ![Top View](Image/Top1_img.png)    |
| **Bottom View** | ![Bottom View](Image/Bottom1_img.png) |
| **Layout**    | ![FrontLeft View](Image/Layout1_img.png) |
| **Interface**    | ![Interface View](Image/web_local1_img.png)  | 
## Notes
- **Data Transfer Speed**: Optimized for USB 2.0.
- **Noise Immunity**: Tested in high-interference environments.
- **Power Consumption**: < 100mA in operation mode.



## 👨‍💻 Author & Contributions
Developed by **Mai Xuan Canh** 🚀  
📩 Contact: [canhmai.work@gmail.com](mailto:canhmai.work@gmail.com)  
📌 LinkedIn: [linkedin.com/in/maixuancanh2003](https://linkedin.com/in/maixuancanh2003)  
