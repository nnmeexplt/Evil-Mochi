<div align="center">

<img width="795" height="247" alt="bannernice" src="https://github.com/user-attachments/assets/4f0e6567-c721-4cde-9e40-fc6ed92c7c7a" />


  <br/>
  <br/>

  <p align="center">
    <a href="https://github.com/nnmeexplt/evil-mochi"><img src="https://img.shields.io/static/v1?label=nnmeexplt&message=Evil-Mochi&color=880808&logo=github"/></a>
    <a href="https://github.com/nnmeexplt"><img src="https://img.shields.io/badge/Profile-333333?logo=refinedgithub&logoColor=black"/></a>
    <img src="https://img.shields.io/badge/ESP32-Offensive%20%2B%20Defensive-880808?logo=espressif"/>
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
Evil Mochi is a custom ESP32-C3 firmware made for wireless tools, pentesting, and general utilities. It supports Wi-Fi, Bluetooth, and IR functionality, with a 128×64 I²C OLED for the interface and a custom animated mochi that changes mood while on idle.

**Developed and tested on the ESP32-C3 SuperMini**, but works on any ESP32-C3 dev board with the same GPIO wiring.

> **some features may violate local laws.** Use at your own discretion and risk.


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

<!-- Features -->
## 📌 Features
<details>
<summary><strong>📡 Wi-Fi</strong></summary>
  
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
<summary><strong>🔵 Bluetooth</strong></summary>
  
| Tool | Description |
|------|-------------|
| BLE Scan | Lists nearby BLE devices, names, and RSSI. |
| Beacon Spam | Floods the surrounding area with fake Bluetooth SSIDs (probably the most optimized for esp32c3 around) |
| Android Spam | Broadcasts FastPair payloads with random MACs |
| Bad BLE | HID emulation for injecting keystrokes over Bluetooth Low Energy |
| BLE Radar | Tracks nearby BLE devices and shows device name, MAC address, RSSI, visual proximity meter, and total times seen |

</details>

<details>
<summary><strong>📺 Infrared</strong></summary>
  
| Tool | Description |
|------|-------------|
| TVBGONE | Turn off any TV, Features 140 EU and 137 NA codes with a custom power icon fill animation |
> More coming soon                                                        

</details>

<details>
<summary><strong>👾 Idle Mochi</strong></summary>
  
| Tool | Description |
|------|-------------|
| Idle Mochi | Gets you back to mochi standby |
> After 45-seconds its enters automatically to mochi standby 

</details>

<details>
<summary><strong>⚙️ Config</strong></summary>
  
| Tool | Description |
|------|-------------|
| LED Brightness | Configure how bright you want your led indicator from 0 to 100% |
| Invert Colors | Inverts the colors displayed on the screen, turning each color into its opposite |
| Restart | Restart the device if you can't reach the physical RST button |
> Brightness & Color Inversion its saved to NVS so its not lost after first restart or shut off


</details>

> [!WARNING]
> This project is intended for **educational and research purposes only**. Unauthorized use may violate local laws.
