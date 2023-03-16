# TAILS INSTALLATION AND USAGE

[Tails](https://tails.boum.org/) is a free and open source portable Debian based operating system that works through a USB stick. It provides a safer environment to work on your own computer or somebody else's as it never accesses the computer's OS. Everything done in Tails disappears when it's shut down, leaving no trace on the computer: Tails always starts from a clean, fresh state and doesn't write anything to the hard drive.
It's possible to save files and configurations in the Persistent storage, otherwise everything done in Amnesia will be wiped.
Tails can't be used alongside the regular OS because it needs to be booted from BIOS/UEFI on the computer.

## Installation

### Through USB stick

If there's another trusted Tails user, it's advised to clone Tails from their stick. These are the steps, starting with the other user's Tails:

**Installation via cloning:** 
1. The trusted user starts their Tails. 
2. Plug the fresh USB that is to be used to recieve the cloned image. 
3. Go to Applications --> Tails --> Tails installer. 
4. Select the USB stick and install. This usually takes ~1/2 hour.
5. When finished you can eject the newly cloned USB and power down the original Tails instance.

**Configuation:**  
See steps listed below.

**Usage:**

1. Boot Tails from the computer. Most devices don't automatically show the Boot Menu, which needs to be accessed through a key (depending on the manufacturer, its usually one of these keys: Esc, F2, F7, F9, F10, F11, F12).
2. Start Tails from the Welcome Screen

### Download and verify

1. [Download Tails](https://tails.boum.org/install/download/index.en.html).
2. Verify the download through the same link or with OpenPGP signature.
3. It is important to verify the software you're downloading to ensure the integrity of the software.

### Burning Tails on a DVD

Links for detailed [instructions](https://tails.boum.org/install/dvd/index.en.html) for Windows, Ubuntu and macOS.

### Running Tails on a virtual machine

See the example of [Virtualbox](https://wiki.lunardao.net/virtualbox_whonix.html). 
**Security concerns:** Running Tails in parallel to the regular OS can be useful and more comfortable but may bring some security concerns:.
* both the host OS and the virtualization sotware are able to monitor what is being done in Tails, hence use trustworthy ones - always at least open-source. Be mindful that if the host OS has been tampered with, it can break Tails' security guarantees.
* traces of the session may be left on the hard disk.
* Tails' default MAC address anonymization doesn't affect the settings of the host OS. The MAC address anonymization only affects the Tails instance.
Here's more content and [virtualization solutions](https://tails.boum.org/doc/advanced_topics/virtualization/index.en.html)

## Configuration

1. Boot into Tails from the Boot Menu.
2. From Welcome Screen configure Language, Keyboard Layout, Formats.
3. If needed, configure [Persistent Storage](https://tails.boum.org/doc/persistent_storage/index.en.html). This allows to save Documents, Wi-Fi passwords, browser bookmarks and other configurations. Enter a secure Passphrase (check this recommended link on [how to create a secure passphrase](https://theintercept.com/2015/03/26/passphrases-can-memorize-attackers-cant-guess/)) and keep it in a safe place: if forgotten, there's no way to access the Persistent Storage again.
4. Additional Settings:  
	- **a. Administrator Password:** Used to access internal hard drive or to perform administrative tasks.  
	- **b. MAC Address Anonymization:** Every device has a Media Access Control (MAC), serial number used to identify the communications on local network. On Tails its anonymized by default - but this setting can be turned off - by changing the serial number to random values. The MAC anonymizer feature is useful to prevent tracking geographical location and to hide the Tor connection, but sometimes it can be suspicious.  
	- **c. Offline Mode**
	- **d. Unsafe Browser:** By default Tails connects to internet through Tor Network, which hides content, destination and location; there's the possibility to use the Unsafe Browser if needed to connect to a captive portal (a captive portal is a web or splash page displayed before end-users can authenticate onto WiFi or wired networks to get access to the internet).
	
## Persistent Storage

Every time Tails is booted, there's the possibility to access the Persistent Storage by entering the Passphrase.
When Tails is started, select Applications --> Tails --> Persistent Storage. The Pesrsistent Storage has the following possible features:

1. **Persistent Documents**
* Persistent folder: Allows to save documents. To open it, choose Places --> Persistent.
2. **System Settings**
* Welcome Screen: Used to save settings of the Persistent Storage.
* **Printers** Printers' configuration saved.
3. **Network**
* Network connections: Wi-Fi passwords and configuration of wired networks saved.
* **Tor Bridge:** The last Tor bridge used to connect is saved.
4. **Applications**
* [Tor Browser](https://www.torproject.org/) Bookmarks
* [Electrum Bitcoin Wallet](https://electrum.org/#home)
* [Thunderbird Email Client](https://www.thunderbird.net/en-US/)
* [GnuPG](https://gnupg.org/): OpenPGP keys created or imported in GnuPG and Kleopatra are saved.
* [Pidgin Internet Messenger](https://pidgin.im/): account, contact and chat configurations, OTR encryption keys and keyrings.
* SSH Client: SSH keys created or imported, public keys of hosts previously connected to, SSH configuartion file (~/.ssh/config)
5. **Advanced Settings**
* Additional Software: A list of additional software chosen is automatically installed every time Tails starts.
* Dotfiles: dotfiles are configuration files to manage some programs' functionalities; they're named dotfiles because their name starts with a "." (for example ~/.gitconfig). Be careful when writing dotfiles not to harm your security: Tails and Tor guarantee anonymity by making it impossible to distinguish one user from the other and modifying dotfiles can harm this. 

## Usage

### Security

Tails is pre-configured with safe defaults: Tor Browser with uBlock, Thunderbird, KeepPassXC, LibreOffice, OnionShare, Metadata Cleaner; every app connects only through Tor and everything in Persistent Storage is automatically encrypted.
Even though there are still some risks associated with using Tails, listed below, it's a fairly easy way to secure anonymity and it's accessible enough to a user who has less experience. It's widely known and used in the activist, militant and journalism fields, here are some examples:
* [Abortion activists in Brazil](https://tails.boum.org/news/story_protecting_abortion_activists/index.en.html)
* [BOAK, Russian Partisan Organization](https://tails.boum.org/contribute/how/user_experience/interviews/boak/)
* [Other interviews with journalists and activists that use Tails](https://tails.boum.org/contribute/how/user_experience/interviews/)

LunarDAO fully supports the use of Tails in these fields to avoid state repression and ensure freedom; nonetheless, lunarpunk movement believes that privacy is and should be a right for everyone, hence encourage the usage of Tails for everybody that strives for more privacy.
 
### Warnings

Tails is designed to be a safer OS than regular ones but there are still some behaviours that can put an anonymous setup at risk:
- Sharing files without wiping metadata
- Using a website in the same session to access more than one account: They can be connected because of the usage of the same Tor circuit. Consider having different Tails sticks.
- Tails uses the Tor Network by default to connect to internet, which is definitely safer than connecting on the clearnet but still has some vulnerabilities, mainly regarding hiding that Tor is being used and protecting communications from skilled attackers. If trying to hide the Tor fingerprint, use a Tor bridge.
- Tor vulnerabilities include: Decrypting through exit node, deanonymization through control of 3 relays of the circuit, eavesdropping on unencrypted communications if not using HTTPS mode only.
- Using Tails on untrusted computers: Don't use Tails USB stick as a normal stick, do not plug it in when another OS is running. If possible clone Tails directly from a trusted person. If the hardware is compromised, not even Tails is safe.

### System requirements and Troubleshooting:

* [System requirements](https://tails.boum.org/doc/about/requirements/index.en.html)
* [Known issues](https://tails.boum.org/support/known_issues/index.en.html)
* [Known issues with graphic cards](https://tails.boum.org/support/known_issues/index.en.html)

## [Tails Social Contract](https://tails.boum.org/doc/about/social_contract/index.en.html)
