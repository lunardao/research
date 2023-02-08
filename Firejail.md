## What is Firejail  
[https://firejail.wordpress.com/](https://firejail.wordpress.com/)

Firejail allows a process and all its descendants to have their own private view of the globally shared kernel resources. There are no dependencies for firejail and can run on any linux computer running kernel 3.8 or higher. Firejail creates a security sandbox around any type of process. This sandbox restricts the process' running environment to a linux namespace. There are very little configurations to edit.

## Benefits of Firejail

If a process is running in a sandbox, there is control over the environment in which the process is being run.

Firejail uses the linux kernel security features. It's used to restrict access to files and system capabilities from programs running on a computer.

Firejail is a program that restricts untrusted applications, and gives a process its own private access of the globally shared kernel and kernel resources including network, process table and mount table. The Firejail sandbox protects any type of process and any descendant of that firejail'd process.

## Downloading Firejail

Arch Linux:
```sh
pacman -S firejail
```
Debian:
```sh
sudo apt install firejail
```
Fedora:
```sh
dnf install firejail
```
openSUSE:
```sh
zypper install firejail
```
To create separate profiles for all applications, run the fire config command with sudo privileges and it will generate profiles for all applications on the device.

```sh
sudo firecfg
```
- This creates symlinks to usr/local/bin/ and allows the programs to run by default sandboxed,
- creates new desktop files removing hardcoded paths, to ensure the desktop files will run in a sandbox
- and adds the running user to the allowed users list.


## Librewolf and Firejail

Download librewolf from [here](https://librewolf.net/).

To view the benefits of librewolf visit our [privacy tools](https://wiki.lunardao.net/list_privacy_tools.html) page. 

Once both librewolf and firejail are installed, build a librewolf profile for firejail to use.
```sh
firejail --build=librewolf.profile librewolf
```

After building a librewolf profile, run this command with no further configurations.
```sh
firejail librewolf
```

Librewolf is now running in a security sandbox.


An application can run entirely in memory with this command (specify the path to the process).
```sh
firejail --private /usr/bin/librewolf
```

