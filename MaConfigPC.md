
## 🔧 **Résumé de ma configuration**

| Élément             | Détail                                                           |
| ------------------- | ---------------------------------------------------------------- |
| **Processeur**      | Intel Core i5-6300HQ (4 cœurs / 4 threads, Skylake, 2.3–3.2 GHz) |
| **Carte graphique** | NVIDIA GTX 1060 6 Go (Mobile, Pascal, 2016)                      |
| **RAM**             | 16 Go DDR4                                                       |
| **Disque**          | SSD Crucial MX500 2 To (SATA, pas NVMe)                          |
| **Écran**           | 1920x1080 + 2560x1080                                            |
| **Système**         | Manjaro Linux avec KDE Plasma 6.3.4                              |
| **Date BIOS**       | Avril 2019 (donc laptop d’environ 2016–2017)                     |


---

### 🧠 **Processeur (CPU)**

* **Modèle** : Intel Core i5-6300HQ
* **Architecture** : Skylake (4 cœurs physiques)
* **Fréquence** : 2.7 GHz (jusqu’à 3.2 GHz)

---

### 🎮 **Carte graphique (GPU)**

* **NVIDIA GeForce GTX 1060 Mobile (6 Go)** — *très correcte pour du jeu ou du rendu léger*
* Pilote : `nvidia` propriétaire (version 570.144)

---

### 🧩 **Mémoire vive (RAM)**

* **16 Go** de RAM
* Utilisée actuellement : \~6.4 Go

---

### 💽 **Stockage**

* **Crucial CT2000MX500SSD1** — SSD SATA 2 To
* **Espace utilisé** : 1.55 To sur 1.82 To (85 % plein)
* **Partition principale** : `/dev/sda5` en **ext4**
* **Partition EFI** : `/dev/sda1`
* **Partition swap** : 31.25 Go utilisée à 3 %

---

### 🔊 **Audio**

* Carte intégrée Intel HD Audio
* Sortie HDMI audio via NVIDIA
* Interface audio USB externe : **BEHRINGER UMC404HD 192k** — *bon matos pour la musique 🎧 !*

---

### 📶 **Réseau**

* **Wi-Fi** : Intel Wireless 8260
* **Ethernet** : Realtek RTL8111/8168 (1 Gbit/s)
* **Bluetooth** : intégré (Intel), service actif mais désactivé logiciellement (`rfkill` soft-block)

---

### 🔋 **Batterie**

* Capacité actuelle : 43.5 Wh
* Capacité d’origine : 64.4 Wh → **67.5 % de santé**
* État : branché, pas en charge (peut indiquer une charge complète ou une dégradation batterie)

---

### 🖥️ **Écrans**

* Écran principal : 1920×1080 @ 60 Hz
* Second écran branché : 2560×1080 @ 60 Hz
* Serveur X11 + Xwayland (pas encore sur Wayland natif)

---

### 🌡️ **Températures et ventilateurs**

* **CPU** : 70°C
* **GPU** : 64°C
* **Ventilateur CPU** : 3600 RPM — *fonctionne correctement mais ça peut chauffer un peu si sollicité*

---

### 💡 **Système**

* **Manjaro Linux KDE Plasma 6.3.4**
* **Kernel** : 6.14.4-1
* **Uptime** : 23 heures
* **Shell** : Zsh
* **Paquets installés** : 1994

---

inxi -Fxz
```shell
System:  
 Kernel: 6.14.4-1-MANJARO arch: x86_64 bits: 64 compiler: gcc v: 14.2.1  
 Desktop: KDE Plasma v: 6.3.4 Distro: Manjaro base: Arch Linux  
Machine:  
 Type: Laptop System: ASUSTeK product: GL502VML v: 1.0  
   serial: <superuser required>  
 Mobo: ASUSTeK model: GL502VML v: 1.0 serial: <superuser required>  
   UEFI: American Megatrends v: GL502VML.306 date: 04/29/2019  
Battery:  
 ID-1: BAT0 charge: 43.5 Wh (100.0%) condition: 43.5/64.4 Wh (67.5%)  
   volts: 15.2 min: 15.2 model: ASUSTeK ASUS Battery status: not charging  
CPU:  
 Info: quad core model: Intel Core i5-6300HQ bits: 64 type: MCP  
   arch: Skylake-S rev: 3 cache: L1: 256 KiB L2: 1024 KiB L3: 6 MiB  
 Speed (MHz): avg: 2700 min/max: 800/3200 cores: 1: 2700 2: 2700 3: 2700  
   4: 2700 bogomips: 18399  
 Flags: avx avx2 ht lm nx pae sse sse2 sse3 sse4_1 sse4_2 ssse3 vmx  
Graphics:  
 Device-1: NVIDIA GP106M [GeForce GTX 1060 Mobile] vendor: ASUSTeK  
   driver: nvidia v: 570.144 arch: Pascal bus-ID: 01:00.0  
 Device-2: IMC Networks USB2.0 HD UVC WebCam driver: uvcvideo type: USB  
   bus-ID: 1-4:3  
 Display: x11 server: X.Org v: 21.1.16 with: Xwayland v: 24.1.6 driver: X:  
   loaded: nvidia gpu: nvidia,nvidia-nvswitch resolution: 1: 1920x1080~60Hz  
   2: 2560x1080~60Hz  
 API: EGL v: 1.5 drivers: nouveau,nvidia,swrast platforms:  
   active: gbm,x11,surfaceless,device inactive: wayland  
 API: OpenGL v: 4.6.0 compat-v: 4.5 vendor: nvidia mesa v: 570.144  
   glx-v: 1.4 direct-render: yes renderer: NVIDIA GeForce GTX 1060/PCIe/SSE2  
 API: Vulkan v: 1.4.309 drivers: nvidia surfaces: xcb,xlib devices: 1  
 Info: Tools: api: clinfo, eglinfo, glxinfo, vulkaninfo  
   de: kscreen-console,kscreen-doctor gpu: nvidia-settings,nvidia-smi  
   wl: wayland-info x11: xdpyinfo, xprop, xrandr  
Audio:  
 Device-1: Intel 100 Series/C230 Series Family HD Audio vendor: ASUSTeK  
   driver: snd_hda_intel v: kernel bus-ID: 00:1f.3  
 Device-2: NVIDIA GP106 High Definition Audio vendor: ASUSTeK  
   driver: snd_hda_intel v: kernel bus-ID: 01:00.1  
 Device-3: BEHRINGER GmbH UMC404HD 192k driver: snd-usb-audio type: USB  
   bus-ID: 1-1:2  
 API: ALSA v: k6.14.4-1-MANJARO status: kernel-api  
 Server-1: sndiod v: N/A status: off  
 Server-2: PipeWire v: 1.4.2 status: active  
Network:  
 Device-1: Intel Wireless 8260 driver: iwlwifi v: kernel bus-ID: 02:00.0  
 IF: wlp2s0 state: up mac: <filter>  
 Device-2: Realtek RTL8111/8168/8211/8411 PCI Express Gigabit Ethernet  
   vendor: ASUSTeK driver: r8169 v: kernel port: d000 bus-ID: 03:00.0  
 IF: enp3s0 state: up speed: 1000 Mbps duplex: full mac: <filter>  
Bluetooth:  
 Device-1: Intel Bluetooth wireless interface driver: btusb v: 0.8 type: USB  
   bus-ID: 1-9:7  
 Report: rfkill ID: hci0 rfk-id: 0 state: down bt-service: enabled,running  
   rfk-block: hardware: no software: yes address: see --recommends  
Drives:  
 Local Storage: total: 1.82 TiB used: 1.55 TiB (85.3%)  
 ID-1: /dev/sda vendor: Crucial model: CT2000MX500SSD1 size: 1.82 TiB  
Partition:  
 ID-1: / size: 1.76 TiB used: 1.55 TiB (88.1%) fs: ext4 dev: /dev/sda5  
 ID-2: /boot/efi size: 259.5 MiB used: 36.3 MiB (14.0%) fs: vfat  
   dev: /dev/sda1  
Swap:  
 ID-1: swap-1 type: partition size: 31.25 GiB used: 1.05 GiB (3.4%)  
   dev: /dev/sda6  
Sensors:  
 System Temperatures: cpu: 70.0 C pch: 63.5 C mobo: N/A gpu: nvidia  
   temp: 64 C  
 Fan Speeds (rpm): cpu: 3600  
Info:  
 Memory: total: 16 GiB available: 15.55 GiB used: 6.44 GiB (41.4%)  
 Processes: 320 Uptime: 23h 11m Init: systemd  
 Packages: 1994 Compilers: clang: 19.1.7 gcc: 14.2.1 Shell: Zsh v: 5.9  
   inxi: 3.3.38
```
