<div align="center">

<img width="795" height="247" alt="bannerCOMPsmaller" src="https://github.com/user-attachments/assets/96aef791-8533-4de7-a165-b820b6b6aa80" />


  <br/>
  <br/>

  <p align="center">
    <a href="https://github.com/nnmeexplt/evil-mochi"><img src="https://img.shields.io/static/v1?label=nnmeexplt&message=Evil-Mochi&color=880808&logo=github"/></a>
    <a href="https://github.com/nnmeexplt"><img src="https://img.shields.io/badge/Profile-333333?logo=refinedgithub&logoColor=black"/></a>
    <img src="https://img.shields.io/badge/ESP32C3-Offensive%20%2B%20Defensive-880808?logo=espressif"/>
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
    <img src="https://img.shields.io/badge/Bluetooth-880808?style=flat&logo=antenna&logoColor=white"/>
    <img src="https://img.shields.io/badge/Infrared-880808?style=flat&logo=antenna&logoColor=white"/>
</p>

## 📌 Features & Functionality
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


> **BLE Radar Distance**
> - **Nearby** → 0–3 m
> - **Moderate** → 3–8 m
> - **Very Far** → 10–30 m
> - **Extreme** → unkonwn 

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
> **After 45-seconds its enters automatically to mochi standby**
> 
> ***More features, styles and animations will come soon***

</details>

<details>
<summary><strong>🕹️ GAMES</strong></summary>
  
| Games | Description |
|------|-------------|
| Snake | (G)old school nokia game |
| Flappy Bird | that stupid ass flying bird |
| Dino | classic chrome dino game (I tried my best) |
| Lane Racer | endless lane dodging game, gets faster the longer you drive |

</details>


<details>
<summary><strong>⚙️ CONFIG</strong></summary>
  
| Tool | Description |
|------|-------------|
| LED Brightness | Configure how bright you want your led indicator from 0 to 100% |
| Invert Colors | Inverts the colors displayed on the screen, turning each color into its opposite |
| Restart | Restart the device if you can't reach the physical RST button |
> Brightness & Color Inversion its saved to NVS so its not lost after first restart.

</details>

##### Some features may violate local laws. Use at your own risk.

## 🛠️ Hardware Required
- **ESP32-C3** – Main microcontroller with Wi-Fi and Bluetooth (Either C3 dev board or supermini will work)
- **DISPLAY** – 0.96" I2C OLED display 128x64 (SSD1306)
- **IR LED Trasmitter** – Either a generic IR trasmitter module or separate IR LEDs wired according to the schematic schematic below
- **STATUS LED + 1x150Ω resistor** – Any red,green,blue led will work properly
- **Resistors 3x10Ω/1x150Ω** – (Optional, needed only if you are following my IR schematic)
- **transistors 1x NPN BJT** – (Optional, needed only if you are following my IR schematic)
- - **3x BUTTONS** – Any push button will do the job
>
> Battery Components (Not neccessarily unless you are following my IR diagram or you simply want it)
> 
- **Li Po 3.7V Battery** – Over 1k mAh if you dont want to change the resistor from the tp4056
- **SWITCH** – Any on/off switch will work
- **TP4056** – Make sure you get the charging module with battery protection which has 6 pads
- **MT3608** – DC-DC Step-Up (Boost) Converter
- #### Alternatively, use a single module that integrates both as shown in my schematic below.
> [!WARNING]
> If you are gonna charge a battery under 1kmAh please make sure to change the resistor with the appropiate value.

<br/>

## 🔗 Connections Pinout          
### • DISPLAY
| Component | Pin |
| :--- | :--- |
| **VCC** | 3.3V | 
| **GND** | GND |  
| **SDA** | GPIO 8 |  
| **SCL** | GPIO 9 | 

### • Others 
| Component | Pin |
| :--- | :--- | 
| **IR LED** | GPIO 4 | 
| **Status LED** | GPIO 3 Through a 150Ω resistor |
| **Button UP** | GPIO 2 |     
| **Button OK** | GPIO 1 |  
| **Button DOWN** | GPIO 0 |  

### • Battery (Aditional) 
**Set the boost converter output to 5V before connecting the ESP32.**

| Component | Connects to | 
| :--- | :--- | 
| **Battery (+)** | Switch / Leg 1 | 
| **Switch / Leg 2** | TP4056 BAT+ |
| **Battery (−)** | TP4056 BAT− |
| **TP4056 OUT+** | Booster IN+ |  
| **TP4056 OUT−** | Booster IN− |
| **Booster OUT+ (5V)** | ESP32 5V / VIN |
| **Booster OUT− (GND)** | ESP32 GND |

**Neccessary only if you are gonna use custom IR setup like my schematic and not a generic IR trasmitter module.**


<img width="1002" height="716" alt="Schematic" src="https://github.com/user-attachments/assets/1b12f727-6605-4ecd-b517-6535a533ed52" />

> In my build schematic i used exactly these components:  **ESP32C3Supermini, OLED 0.96" Display 128x64, 3x Tactile Push Buttons, 3x TSAL6200 (IR LEDs),  5x Resistors (150ohms/10ohms), 1x 2n2222 Transistor, 1x on/off switch and a Li Po Battery 3.7v plus TP4056+Booster module.**

## 🚀 Installation & Flashing

### What You Need
Before you begin, make sure you have:
*   An ESP32-C3 development board (tested on the SuperMini).
*   A USB data cable (not just a charge-only cable).
*   The Evil Mochi firmware `.bin` file.
*   A compatible ESP32 flashing tool, such as [ESP Flasher.](https://esptool.spacehuhn.com/) or [Adafruit Flasher](https://adafruit.github.io/Adafruit_WebSerial_ESPTool/)
*   USB drivers for your board if required (CH340 or CP2102)

### Step 1: Download the Firmware
1. Download the latest Evil Mochi release from the repository's **Releases** section or install the zip file directly.
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
5. `Ready to go and play`

## 💎 Credit
- Fully developed and maintained by **me**.
- Check out my other projects on my [github](https://github.com/nnmeexplt?tab=repositories)

**Special thanks to the open-source pentesting community for protocol research and payload inspiration.**

## 📩 Contact
- Portfolio: [nnmestore](https://nnmestore.pages.dev) 
- Tiktok:  [@nnme.dev](https://tiktok.com/@nnme.dev) 
- Github:    [nnmeexplt](https://github.com/nnmeexplt)
- Email:     nonametester@proton.me
##### If you have any questions regarding the project, feel free to share them on [here](https://tiktok.com/@nnme.dev) 
##### Check out my videos of the builds and projects i've made over the time on [here](https://tiktok.com/@nnme.dev) 

## 🌟 Support 

- 💬 Found a bug or have a feature request? Open an [Issue](https://github.com/nnmeexplt/evil-mochi/issues)
- ⭐ Like the project? a star on the repo will make a big difference.
- 🤝 Want to see more projects like this? Drop a follow, it means a lot and keeps me motivated.

> ⚠️ This project is intended for **educational and research purposes only.** Users are fully responsible for any misuse of this firmware.
