# <img src="https://github.com/user-attachments/assets/22ff37ba-a8ea-4b65-b7b2-e7fcb09d858b" height="32" width="32"></img> Virtual Display Driver Compatibility Fork

This project creates a _virtual monitor_ in Windows that functions just like a physical display. It is particularly useful for applications such as **streaming, virtual reality, screen recording,** and **headless servers—systems** that operate without a physical display attached. 

Unlike traditional monitors, this virtual display supports custom resolutions and refresh rates beyond hardware limitations—offering greater flexibility for advanced setups. You can also use custom EDIDs to simulate or emulate existing hardware displays.


> ⚠️ **VirusTotal Warning – False Positives (Explained)**

I'm providing this **older version** of the Virtual Display Driver (VDD) because some users (especially on **Tensordock VMs**) have reported issues with the newer one – in some cases, it's not properly recognized after installation.

This version works reliably in those setups.

---

### 🧪 VirusTotal Scan Results

![VirusTotal Screenshot](./vdd-virustotal.png)

I ran the file through [VirusTotal](https://virustotal.com), and here's the result:

- ✅ **67 out of 71 antivirus engines** marked it as **clean**
- ⚠️ **4 vendors** flagged it:
  - `W32.AIDetectMalware` – Bkav Pro  
  - `Malicious` – SecureAge  
  - `Win/grayware_confidence_60%` – CrowdStrike Falcon  
  - `BehavesLike.Win32.Generic.vc` – Skyhigh (SWG)

These detections are **false positives** due to:
- The driver calling WMI / behaving like debugging software
- Overlay-related functions or long sleep cycles
- No digital signature (which is common for niche tools like this)

---

### 🔐 What You Should Know

- 🧠 This file is **unmodified**, originally from [ItsMikeTheTech](https://itsmikethetech.com/)
- 💡 You’re welcome to **analyze or scan** it yourself if you have concerns
- 🛡️ Windows Defender and most major AVs report it as safe

---

> I’m only sharing this older version for compatibility reasons.  





| 👤 Developer          | 🏷️ Role                            | 💖 Support Us                                                                                                         |
| --------------------- | ----------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **[MikeTheTech](https://github.com/itsmikethetech)** | Project Manager, Lead Programmer | [Patreon](https://www.patreon.com/mikethetech) :gem: / [GitHub Sponsors](https://github.com/sponsors/itsmikethetech/) 💖  |
| **[Jocke](https://github.com/zjoasan)**       | Programmer, Concept Design  | [GitHub Sponsors ](https://github.com/sponsors/zjoasan) 💖                                                             |

:bulb: *We appreciate your support—every contribution helps us keep building amazing experiences!*

## ⬇️ Download Latest Version

- [Driver Installer (Windows 10/11)](https://github.com/VirtualDisplay/Virtual-Display-Driver/releases) - Check the [Releases](https://github.com/VirtualDisplay/Virtual-Display-Driver/releases) page for the latest version and release notes.

> [!IMPORTANT]
> Before using the Virtual Display Driver, ensure the following dependencies are installed:
> - **Microsoft Visual C++ Redistributable**  
>   If you encounter the error `vcruntime140.dll not found`, download and install the latest version from the [Microsoft Visual C++ Redistributable page](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170).


## 🛠️ Installation

- Step 1: Download the Installer
   - You can download the installer directly from the [Releases]([https://github.com/VirtualDisplay/Virtual-Display-Driver/releases](https://github.com/ULTRA-VAGUE/Virtual-Display-Driver-Compatibility-Fork)) page.

- Step 2: Run the Installer
   - Launch the installer.
   - Follow the on-screen instructions to complete the installation.

- Step 3: Verify the Installation (Optional)
   - Check if the Virtual Display Driver is correctly installed by running the following:
   - **Device Manager:** Check "Device Manager" under "Display Adapters."
   - **Settings:** Check display settings under system settings and see if the virtual displays show.

Manual installation can be found in the wiki

## 🤔 Comparison with other IDDs

The table below shows a comparison with other popular Indirect Display Driver
projects.

![Untitled-6](https://github.com/user-attachments/assets/98ccb915-5a94-42f9-818b-213ceef4c3ac)

¹ ARM64 Support in Windows 11 24H2 or later may require test signing be enabled.

HDR Support Now Available for Windows 11 23H2+ 

## ▶️ Videos and Tutorials

### Installation Video

[![maxresdefault](https://github.com/user-attachments/assets/fa9bec7f-c6f4-4362-be11-8e5d43c326f1)](https://youtu.be/ChvucKHbwMo)

![Powerpoint](https://github.com/user-attachments/assets/9ac05776-36e1-4ba1-ac52-3f189dbd7730)

## 🤝 Sponsors

<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/ca93d971-67dc-41dd-b945-ab4f372ea72a" /></td>
    <td>Free code signing on Windows provided by <a href="https://signpath.io">SignPath.io</a>, certificate by <a href="https://signpath.org">SignPath Foundation</a></td>
  </tr>
</table>

## Acknowledgements

- Shoutout to **[MikeTheTech](https://github.com/itsmikethetech)** Project Manager, Owner, and Programmer
- Shoutout to **[zjoasan](https://github.com/zjoasan)** Programmer. For scripts, EDID integration, and parts of installer.
- Shoutout to **[Bud](https://github.com/bud3699)** Former Lead Programmer, has since left the project.
- Shoutout to **[Roshkins](https://github.com/roshkins/IddSampleDriver)** for the original repo.
- Shoutout to **[Baloukj](https://github.com/baloukj/IddSampleDriver)** for the 8-bit / 10-bit support. (Also, first to push the new Microsoft Driver public!)
- Shoutout to **[Anakngtokwa](https://github.com/Anakngtokwa)** for assisting with finding driver sources.
- **[Microsoft](https://github.com/microsoft/Windows-driver-samples/tree/master/video/IndirectDisplay)** Indirect Display Driver/Sample (Driver code)
- Thanks to **[AKATrevorJay](https://github.com/akatrevorjay/edid-generator)** for the hi-res EDID.
- Shoutout to **[LexTrack](https://github.com/lextrack/)** for the MiniScreenRecorder script. 

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=VirtualDrivers/Virtual-Display-Driver&type=Date)](https://www.star-history.com/#VirtualDrivers/Virtual-Display-Driver&Date)

## Disclaimer:

This software is provided "AS IS" with NO IMPLICIT OR EXPLICIT warranty. It's worth noting that while this software functioned without issues on our systems, there is no guarantee that it will not impact your computer. It operates in User Mode(Session0), which reduces the likelihood of causing system instability, such as the Blue Screen of Death. However, exercise caution when using this software.
