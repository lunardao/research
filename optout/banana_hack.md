# Nokia 8110 "Banana" - Jailbreak

**Warning:** *Changing IMEI number is illegal in multiple jurisdictions. This report is not to promote any activity which can cause users any legal problems! Please research the laws concerning this issue in your region. Treat this report as educational source.*

This report speaks about GSM network data monitoring. Do NOT confuse it with internet identifiers (MAC, IP address etc). 


### Problem: IMEI Number Identification

There are multiple security risks when using a mobile provider (phone or router + sim card) as a hotspot. One security risk is the unique sim card number. However sim cards can be purchased without KYC and changed, the internet or hotspot device - phone or portable router - has a unique IMEI number (International Mobile Equipment Identity). this number remains the same (despite changing MAC or IP address). This makes a device easy to track as IMEI number is communicated to the mobile provider.


### Solution: Unlocking IMEI Modification

Nokia 8110 or "Banana phone" (as it's known) is a great hotspot device, separated from the users main internet device (smart phone, tablet or laptop). With a few hacks, the Banana phone allows users to change the IMEI number any time. This setup has several advantages:

1. Keeps the sim away from the actual user's devices. Prevents leakage of the main the main internet device IMEI
2. Hacked Nokia 8110 can appear on GSM network as any other phone since IMEI numbers are unique per device and model.
3. If IMEI and sim card are changed together - the user is very hard to be linked (mind the place of connection and other active devices!)

**Tip:** An IMEI number on Nokia 8110 can be seen in `Menu` -> `Settings` -> `Device` -> `Device Information` -> `More Information` or by dialing `*#06#`. Validate the setup functionality by running a test check before and after the IMEI change.


## Pre-Requisities

* Nokia 8110 4G "Banana"
* USB <-> Micro-USB cable with a capacity to handle data
* Internet
* Android SDK Tools 
* WebIDE - Palemoon works well

**SDK Tools**

To communicate with the phone via computer an adb command & shell are needed. Adb is a part of Android SDK Tools. Install as below.

Linux (Debian based)  
```sh
sudo apt update && sudo apt install android-sdk
```

Windows - Follow steps in this [manual](https://www.androidcentral.com/installing-android-sdk-windows-mac-and-linux-tutorial).

**WebIDE - Palemoon**

WebIDE is used to *sideload* (install without the bootloader hacking) the needed apps via GUI. An older version of Palemoon works well. Open terminal in a directory where Palemoon will be downloaded and enter the following commands.

```sh
wget http://archive.palemoon.org/palemoon/28.x/28.6.1/palemoon-28.6.1.linux-x86_64.tar.bz2

tar -xf palemoon-28.6.1.linux-x86_64.tar.bz2
```

Move to Palemoon drectory and remove auto-update scripts to keep stay on this version.

```sh
cd palemoon
rm -rf update*
```

Run Palemoon

```sh
./palemoon
```

In case Palemoon still prompts to update, deny!


## Installation & Setup

Regardless of the chosen setup, the Banana phone must have updated firmware and activated debugging mode.

**Keep the device and desktop connected throughout the entire installation process.**


### Update Nokia Firmware

The device must be updated to the latest firmware.

**Check Firmware Version**

`Settings` -> `Device` -> `Device Information` -> `Software`

**Update Firmware Version**

`Settings` -> `Device` -> `Device Information` -> `Software Update` -> `Select` -> `Select`


### Debugging

*Debugging* is a mode in which developer changes can be implemented. Dial the code `*#*#33284#*#*` (`*#*#debug#*#*`) with your keypad. A bug icon should appear in the system taskbar above (as already said, on some devices it is necessary to open a menu using the additional code `*#*#0574#*#*` and from there enable the USB debugging).


### Different Setups

This manual has three options, divided according to the three levels of customization and difficulty of the setup. All three of them include unlocking IMEI customization option.

**Three Options**

1. **Minimal** - The necessary steps to allow IMEI & TTL modification \*
2. **Advanced** - Minimal + FOSS alternative enabled, remove Google apps enabled \*
3. **Expert** (not described in this manual yet)- Reinstalling the complete OS to Gerda - IMEI & TTL changing app is included with auto-randomizing script. 

Chose option and follow the proceeding described under that option directly (ie if 2. is the choice, don't do 1. before).

**Note:** The points with \* use Walace Toolbox to change IMEI. User needs to enter the new IMEI manually. LunarDAO listed a database of IMEI numbers at [wiki.lunardao.net/imei_tables/imei_table.html](https://wiki.lunardao.net/imei_tables/imei_table.html).


### 1. Minimal Setup - Wallace Toolbox Sideload

This setup is the fastest and the least difficult one. The only customization is a sideload of the Wallace Toolbox enabling user to change IMEI, TTL and do few other temporary root actions.

**Get Wallace Toolbox**

Open terminal in target directory to download and run:

```sh
wget https://gitlab.com/suborg/wallace-toolbox/-/archive/master/wallace-toolbox-master.zip
unzip wallace-toolbox-master.zip
```

**Install**

1. Open Palemmon WebIDE: Open Palemoon browser (the steps above) and press `Shift` + `F8` or navigate to `Tools` -> `Web Developer` -> `WebIDE`
2. Setup adb to tcp socket 6000. In terminal run:
```sh
adb forward tcp:6000 localfilesystem:/data/local/debugger-socket
```
3. Connect Palemoon WebIDE app to the phone: click on *Remote Runtime* on the right and make sure it's set to `localhost:6000`.
4. In Palemoon WebIDE app click on *Open Packaged Ap...* On the left
5. Navigate to the *wallace-toolbox-master* directory and click *Open*.
6. Click on the play button on top to sideload it.
7. Done. Unmount the device.

**Usage**

Open the Wallace Toolbox app in the phone menu. Use index numbers to navigate. To edit IMEI1 or IMEI2, the new number must be correct, use  [wiki.lunardao.net/imei_tables/imei_table.html](https://wiki.lunardao.net/imei_tables/imei_table.html) to get one based on device and model of your choice. Reboot and control the IMEI in the phone settings.

**Important:** Test it few times without a sim card. After each reboot dial `*#06#` to confirm the IMEI number was edited. To maintain privacy, remove the phone back cover before the IMEI edit. When the phone turns off to reboot take off the battery and exchange sim cards. Assemble and power on.


### 2. Advanced Setup - Replacing Google Services with FOSS

**WARNING!** This process includes factory reset. All data and application will be wiped out!

This setup is probably the best compromise of spent time, needed skills, risk and outcome. The result is a rooted KaiOS (the original OS) enabling user to be in control of all applications and processes. This allows for access to developer menu, removing unwanted apps (Google services), sideloading any new apps and (like in setup #1) editing IMEI & TTL number. 

This hack disables *navigator.mozApps.mgmt.import* method package signature checks, installs [OmniSD](https://sites.google.com/view/bananahackers/install-omnisd) and allows for app config modification.

Before this process, make sure Palemoon is installed (read Pre-Requsities), the firmware is up to date and the device debug mode is enabled.

**Donwload OmniSD**

Download OmniSD.zip and extract. Open terminal in the target directory and run the following commands:
```
mkdir omisd
cd ominsd
wget https://cloud.disroot.org/s/QTC5oM4tZ9rWpAZ/download/OmniSD.zip
unzip OminSD.zip2
```

**Install OmniSD & Run Priviledged Factory Reset**

1. Open Palemmon WebIDE: Open Palemoon browser (the steps above) and press `Shift` + `F8` or navigate to `Tools` -> `Web Developer` -> `WebIDE`
2. Setup adb to tcp socket 6000. In terminal run:
```sh
adb forward tcp:6000 localfilesystem:/data/local/debugger-socket
```
3. Connect Palemoon WebIDE app to the phone: click on *Remote Runtime* on the right and make sure it's set to `localhost:6000`.
4. In Palemoon WebIDE app click on *Open Packaged Ap...* On the left
5. Navigate to the *omnisd* directory and click *Open*.
6. Click on the play button on top to sideload it.
7. In OmniSD menu on your device press `#` and accept privileged reset.
8. Let the device reboot and run the initial setup.
9. Allow debug mode again. Either dial `*#*#33284#*#*` or `Settings` -> `Device` -> `Developer Menu` -> Enable debugger in the "ADB and DevTools" mode. 
10. Repeat the steps 1 to 6.
11. When the installation is finished, all the applications shall be listed in the left-side bar of the WebIDE.

Keep the phone plugged, WebIDE connected and move through the following points.

**Get Wallace Toolbox**

Open terminal in target directory to download and run:

```sh
wget https://gitlab.com/suborg/wallace-toolbox/-/archive/master/wallace-toolbox-master.zip
unzip wallace-toolbox-master.zip
```

**Install Wallace Toolbox**

1. In Palemoon WebIDE app click on *Open Packaged App...* On the left
2. Navigate to the *wallace-toolbox-master* directory and click *Open*.
3. Click on the play button on top to sideload it.

**Uninstall Pre-Installed Apps**

Pre-installed apps don't show the option *Uninstall* in the Menu. This quick hack makes them removable.

1. Open Wallace Toolbox App and select 1:ADB root
2. Pull *webapps* dictionary from the phone, in terminal enter:
```sh
adb pull /data/local/webapps/webapps.json
```
3. Make a backup in case something goes wrong:
```sh
cp webapps.json webapps.json.bak
```
4. Open ~/webapps.json in a text editor
5. Search every app to be set as removable and edit the dictionary line in the sub-dictionary from `"removable": false,` to `"removable": true,`.  Save & exit.
6. Push the modified file back to the phone:
```sh
adb push webapps.json /data/local/webapps/

```
7. Reboot: `adb rebbot`
8. Uninstall Apps in the device menu: move selector to the chosen app -> `Options` -> `Uninstall`

**Edit IMEI in Wallace Toolbox App**

Open the Wallace Toolbox app in the phone menu. Use index numbers to navigate. To edit IMEI1 or IMEI2, the new number must be correct, use  [wiki.lunardao.net/imei_tables/imei_table.html](https://wiki.lunardao.net/imei_tables/imei_table.html) to get one based on device and model of your choice. Reboot and control the IMEI in the phone settings.

**Important:** Test it few times without a sim card. After each reboot dial `*#06#` to confirm the IMEI number was edited. To maintain privacy, remove the phone back cover before the IMEI edit. When the phone turns off to reboot take off the battery and exchange sim cards. Assemble and power on.

### 3. Expert Setup - Replacing OS

*To be tested and docummented soon.*

## Additional Security Steps

For maximal security do not use this phone for web browsing or other online applications. Run it as a hotspot and connect to it from another device using MAC spoofing and VPN or Tor!

* Always change both IMEI and sim card at the same time when changing a setup (from hotspot to burner etc)
* Disable Web Tracking: `Menu` -> `Settings` -> `Privacy & Security` -> `Do Not Track` -> Tick [x] on *Tell websites and apps that I do not want to be tracked*
* Clear Browsing History, Cookies & Stored Data: `Menu` -> `Settings` -> `Privacy & Security` -> `Browsing Privacy`
* App Permissions: `Menu` -> `Settings` -> `Privacy & Security` -> `App Permissions` -> Make sure no app has any permissions without asking.
* Search: `Menu` -> `Settings` -> `Personalization` -> `Search` -> *Change Engine* from  *Google* to *DuckDuckGo* and turn *Search Suggestions* to *No*.
