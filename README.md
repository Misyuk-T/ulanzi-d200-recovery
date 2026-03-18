# Ulanzi D200 / D200H — Recovery and repair (RK Solution)

Instructions and materials for recovering RK (Rockchip) based devices, including D200 and D200H models that fail to power on.

---

## Materials on Google Drive

All materials (**_MACOSX**, **Driver** — DriverAssistant v5.1.1, **RKDevTool** v3.19 for Windows) in one folder:

![ulanzi folder on Google Drive](assets/drive-ulanzi-folder.png)

**[Open ulanzi folder](https://drive.google.com/drive/folders/1ayBERi3SmIFKS7yYgxk8DdpD99kiSG8D?usp=sharing)**

---

## Troubleshooting Steps for RK Solution-based D200 and D200H Models That Fail to Power On

**Applicable only to the fault where the device cannot enter the normal interface after "Ulanzi Starting up" appears at the bottom right corner during startup.**

![Ulanzi Starting up — symptom](assets/image1.png)

---

### Repair Tools and Steps

#### 1. Install the Windows version of the flashing driver: DriverAssitant_v5.1.1

![DriverAssistant](assets/image2.png)

#### 2. Open the RKDevTool_v3.19_for_window flashing tool. Select "Upgrade Firmware", then choose the firmware file and import the "update" firmware into the tool.

![RKDevTool — Upgrade Firmware](assets/image3.png)

![RKDevTool — firmware selection](assets/image4.png)

![RKDevTool — import update](assets/image5.png)

#### 3. Remove the device's back cover and use tweezers to short-circuit pins 1 and 3 as shown in the images.

![Pins 1 and 3 — rear view](assets/image6.png)

![Short-circuit pins 1 and 3](assets/image7.png)

![Pin position](assets/image8.png)

#### 4. Keep the short-circuit connected (don't let go of the tweezers) and plug in the USB cable to connect the PC and the device.

![USB connection](assets/image9.png)

#### 5. If the PC tool shows "A LOADER device found", it means the device is successfully connected to the PC. You can then release the tweezers. If the connection fails, the tweezers may not be short-circuited properly. Please try repeatedly—make sure to keep the short-circuit first, then plug in the USB cable.

![A LOADER device found](assets/image10.png)

#### 6. Click "Upgrade" to start the firmware update. Wait until the download reaches 100% and the tool shows "Success". Then you can unplug the USB cable, plug it back in, and the fault will be resolved.

![Upgrade — start](assets/image11.png)

![Success — complete](assets/image12.png)

---

## Notes

- Install drivers via **DriverInstall.exe** from the DriverAssistant folder.
- RKDevTool documentation: the RKDevTool folder contains the PDF «开发工具使用文档_v1.0.pdf».
- Get the **update** firmware file from Google Drive (ulanzi folder) or from the official source.
- **Install path:** When installing or running the flashing tools and firmware, use a **simple, short path with no spaces or special characters** (e.g. `C:\ulanzi` or `D:\tools\RK`). Avoid paths like `C:\Users\Name\My Documents\...` or folders with spaces/symbols, or the tool may fail.
