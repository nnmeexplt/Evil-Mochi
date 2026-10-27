<div align="center">

<img width="795" height="247" alt="bannernice" src="https://github.com/user-attachments/assets/4f0e6567-c721-4cde-9e40-fc6ed92c7c7a" />


  <br/>
  <br/>

  <p align="center">
    <a href="https://github.com/nnmeexplt/evil-mochi"><img src="https://img.shields.io/static/v1?label=nnmeexplt&message=Evil-Mochi&color=880808&logo=github"/></a>
    <a href="https://github.com/nnmeexplt"><img src="https://img.shields.io/badge/Profile-333333?logo=refinedgithub&logoColor=black"/></a>
    <img src="https://img.shields.io/badge/ESP32C3-Offensive%20%2B%20Defensive-880808?logo=espressif"/>
    <img src="https://img.shields.io/badge/License-333333"/>
  </p>

  <p align="center">
    <a href="https://tiktok.com/@nnme.dev"><img src="https://img.shields.io/badge/TikTok-000000?style=flat&logo=tiktok&logoColor=white"/></a>
    <a href="https://nnmestore.pages.dev"><img src="https://img.shields.io/badge/Website-880808?logo=googlechrome&logoColor=black"/></a>
    <a href="https://github.com/nnmeexplt/blood-radar"><img src="https://img.shields.io/badge/Blood Radar-333333?logo=openstreetmap&logoColor=black"/></a>
  </p>

</div>

&nbsp;
<!-- About this Project -->
# ABOUT THIS PROJECT
Evil Mochi is a custom ESP32-C3 firmware made for wireless tools, pentesting, and general utilities. It supports Wi-Fi, Bluetooth, and IR functionality, with a 128×64 I²C OLED for the interface and a custom animated mochi that changes moods while on idle.

Designed to bring wireless experimentation, security testing, and practical hardware utilities together in a compact, feature-rich platform. Combining offensive and defensive capabilities, it provides an accessible interface for exploring wireless technologies, testing security configurations, and interacting with compatible hardware in controlled environments.

Built for enthusiasts, developers, and security researchers, Evil Mochi offers a versatile platform for exploring hardware capabilities, experimenting with wireless technologies, and understanding both offensive techniques and defensive security practices.

Beyond its technical functionality, Evil Mochi incorporates a distinctive visual identity through its custom animated Mochi companion. When the device is idle, Mochi displays expressive animations and changing moods, adding personality to the firmware while giving the interface a menu full of features.

> [!NOTE]
> **Developed and tested on the ESP32-C3 SuperMini**, but works on any ESP32-C3 dev board with the same GPIO wiring.

#### **Evil Mochi is intended for authorized testing, educational experimentation, and legitimate security research.** Users are responsible for ensuring that their activities comply with applicable laws and that they have permission to test the devices and networks involved.

<div>&nbsp;</div>


<div>&nbsp;</div>

<table align="center">
  <tr>
    <td align="center" width="50%">
      <img src="images/1.jpg" alt="" width="100%">
    </td>
    <td align="center" width="50%">
      <img src="images/2.jpg" alt="" width="100%">
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <img src="images/3.jpg" alt="" width="100%">
    </td>
    <td align="center" width="50%">
      <img src="images/4.jpg" alt="" width="100%">
    </td>
  </tr>
</table>

<div>&nbsp;</div>

<p align="center">
    <img src="https://img.shields.io/badge/Wi Fi-880808?style=flat&logo=antenna&logoColor=white"/>
    <img src="https://img.shields.io/badge/Bluetooth-1F242C?style=flat&logo=antenna&logoColor=white"/>
    <img src="https://img.shields.io/badge/Infrared-880808?style=flat&logo=antenna&logoColor=white"/>
    <img src="https://img.shields.io/badge/Settings-1F242C?style=flat&logo=antenna&logoColor=white"/>
</p>

<!-- Features -->
## 📌 FW Features
<details>
<summary><strong>📡 WIFI</strong></summary>
  
| Tool | Description |
|------|-------------|
| Wi-Fi Scan | Full AP scan with SSID, BSSID, RSSI, and Channel |
| Deauth Attacks | Deauth Flood (targets all scanned APs) and Deauth Select (pick one target) |
| Captive Portal | Default "Free WiFi" portal and Evil Twin that logs captured credentials to the screen |
| Station Sniffer | Captures probe requests and data frames to see nearby phones/clients |
| Beacon Spam | floods the surrounding area with fake SSIDs |
| Packet Analyzer | Real-time live graph across all 16 channels |
| Guardian | Monitors for Wi-Fi attacks (Deauth floods, Beacon floods, Probe floods) and alerts you in real time |

</details>

<details>
<summary><strong>🔵 BLUETOOTH</strong></summary>
  
| Tool | Description |
|------|-------------|
| BLE Scan | Lists nearby BLE devices, names, and RSSI. |
| Beacon Spam | Floods the surrounding area with fake Bluetooth SSIDs (probably the most optimized for esp32c3 around) |
| Android Spam | Broadcasts FastPair payloads with random MACs |
| Bad BLE | HID emulation for injecting keystrokes over Bluetooth Low Energy |
| BLE Radar | Tracks nearby BLE devices and shows device name, MAC address, RSSI, visual proximity meter, and total times seen |

</details>

<details>
<summary><strong>📺 INFRARED</strong></summary>
  
| Tool | Description |
|------|-------------|
| TVBGONE | Turn off any TV, Features 140 EU and 137 NA codes with a custom power icon fill animation |
> More coming soon                                                        

</details>

<details>
<summary><strong>👾 IDLE MOCHI</strong></summary>
  
| Tool | Description |
|------|-------------|
| Idle Mochi | Gets you back to mochi standby |
> After 45-seconds its enters automatically to mochi standby 

</details>

<details>
<summary><strong>⚙️ CONFIG</strong></summary>
  
| Tool | Description |
|------|-------------|
| LED Brightness | Configure how bright you want your led indicator from 0 to 100% |
| Invert Colors | Inverts the colors displayed on the screen, turning each color into its opposite |
| Restart | Restart the device if you can't reach the physical RST button |
> Brightness & Color Inversion its saved to NVS so its not lost after first restart or shut off

</details>

> **Some features may violate local laws.** Use at your own risk.

<br/>

## 🛠️ Hardware Required
- **ESP32-C3** – Main microcontroller with Wi-Fi and Bluetooth (Either dev board or supermini will work)
- **I2C OLED DISPLAY** – 0.96" I2C OLED display 128x64 (SSD1306) 
- **IR LED + 1x150Ω resistor** – Either a generic IR module or separate IR LEDs wired according to the schematic diagram below
- **STATUS LED** – Any red,green,blue led will work properly
- **3x BUTTONS** – Any push button its good
- **Resistors 3x10Ω/1x150Ω** – (Optional, needed only if you are following my IR diagram)
- **transistors 1x NPN BJT** – (Optional, needed only if you are following my IR diagram)
>
> Battery components (not neccessarily unless you are following my IR diagram or want a battery).
> 
- **Li Po 3.7V Battery** – Over 1k mAh if you dont want to change the resistor from the tp4056
- **TP4056** – Make sure you get the charging module with battery protection which has 6 pads
- **MT3608** – DC-DC Step-Up (Boost) Converter
#### Or else get a single module featuring both. Like in my diagram below for reference.
> [!WARNING]
> If you are gonna charge a battery under 1kmAh please make sure to change the resistor with the appropiate value.

<br/>

## 🔗 Connections Pinout          
### • I2C OLED Display  
| OLED | ESP32C3 |
| :--- | :--- |
| **VCC** | 3.3V | 
| **GND** | GND |  
| **SDA** | GPIO 8 |  
| **SCL** | GPIO 9 | 

### • Others 
| Component | Pin |
| :--- | :--- | 
| **IR Led** | GPIO 4 | 
| **Status LED** | GPIO 3 Through a 150Ω resistor |
| **Button UP** | GPIO 2 |     
| **Button OK** | GPIO 1 |  
| **Button DOWN** | GPIO 0 |  

> [!TIP]
> **If you are using a generic IR module connect data to gpio 4 directly.**
> 
> **If not and you are using a custom IR setup follow my diagram below for best results.**

### • Battery (Aditional) 
| Component | Connects to | 
| :--- | :--- | 
| **Battery (+)** | Switch / Leg 1 | 
| **Switch / Leg 2** | TP4056 BAT+ |
| **Battery (−)** | TP4056 BAT− |
| **TP4056 OUT+** | Booster IN+ |  
| **TP4056 OUT−** | Booster IN− |
| **Booster OUT+ (5V)** | ESP32 5V / VIN |
| **Booster OUT− (GND)** | ESP32 GND |
> [!TIP]
> Neccessary only if you are gonna use custom IR setup like my diagram and not a generic IR trasmitter module.
>
> Set the boost converter output to 5V before connecting the ESP32.
>
> If you are gonna charge a battery under 1kmAh please make sure to change the resistor with the appropiate value.

<img width="1002" height="716" alt="Schematic" src="https://github.com/user-attachments/assets/1b12f727-6605-4ecd-b517-6535a533ed52" />

<br/>

## 🚀 Installation & Flashing

### What You Need
Before you begin, make sure you have:
*   An ESP32-C3 development board (tested on the SuperMini).
*   A USB data cable (not just a charge-only cable).
*   The Evil Mochi firmware `.bin` file.
*   A compatible ESP32 flashing tool, such as [ESP FLASHER.](https://esptool.spacehuhn.com/) or [ADAFRUIT FLASHER](https://adafruit.github.io/Adafruit_WebSerial_ESPTool/)
*   USB drivers for your board if required (CH340 or CP2102)

### Step 1: Download the Firmware
1. Download the latest Evil Mochi release from the repository's **Releases** section.
2. Extract the downloaded archive if necessary.
3. Locate the firmware `.bin` file.

### Step 2: Connect Your ESP32-C3
1. Connect your ESP32-C3 to your computer using a USB data cable.
2. Make sure again the required USB-to-serial drivers are installed.
3. Identify the serial (COM) port assigned to your board.
4. **If the board does not enter download mode automatically:** Hold the **BOOT** button while connecting or resetting it.

### Step 3: Open the ESP32 Flasher
1. Launch your preferred ESP32 flashing tool.
2. Select the correct serial port.
3. Load the firmware `.bin` file at 0x0 offset.
4. Once flashing reaches 100%, the tool will display a success message.

<br/>

## 💎 Credit
- Fully developed by **nnmexplt**.
- One person. One vision. No limits.
- Personal project made by me.
- Check out my other projects on [github](https://github.com/nnmeexplt?tab=repositories) and my builds on my [tiktok](https://tiktok.com/@nnme.dev) .

> *Special thanks to the open-source pentesting community for protocol research and payload inspiration.*

## 📸 Contact
- Portfolio: [nnmestore](https://nnmestore.pages.dev) 
- Tiktok:  [@nnme.dev](https://tiktok.com/@nnme.dev) 
- Github:    [nnmeexplt](https://github.com/nnmeexplt)
- Email:     nonametester@proton.me
##### if you have a question related to the project dont hesitate to do it [here](https://tiktok.com/@nnme.dev) for the quickest reply.
##### Check out my other builds/projects i've made on [here](https://tiktok.com/@nnme.dev)

## Support & Contributions

- 💬 Found a bug or have a feature request? Open an [Issue](https://github.com/nnmeexplt/evil-mochi/issues)
- ⭐ Like the project? a star on the repo will make a big difference.
- 🛠 Want to contribute? Fork it and submit a pull request.
- 🤝 Want to see more projects like this? Drop a follow, it means a lot and keeps me motivated.

‎

> [!CAUTION]
> This project is intended for **educational and research purposes only**. Unauthorized use may violate local laws.
