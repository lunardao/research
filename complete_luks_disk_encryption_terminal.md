# LUKS disk encryption via terminal

```bash
sudo apt install cryptsetup 
```

**To see a list of available disks. In terminal, run:**

```bash
lsblk
```

- The usual name for external disk are sda, sdb etcetera. The list will also show the size of the disk, which will facilitate identifying which one. The whole path should be:  
/dev/sda unless more than one USB is being plugged in.

**To encrypt the disk, run:**

```bash
sudo cryptsetup -y -v luksFormat /dev/sda
```

- This will warn the user that all content on the disk will be deleted if proceeding.  
- If accepted --> Enter password.  
- Completed.

**To open the encrypted disk:**

- Check the name of the device again:

```bash
lsblk
```

```bash
sudo cryptsetup luksOpen /dev/sda
```
- Note that when unlocking the name of the disk will change.  
- The user is notified (example below, can be a different name): 

>Unlocked /dev/sda as /dev/dm-4.

**Mounting:**


# Complete disk encryption

To see all disks:

```bash
lsblk
```
Create a partition:

```bash
fdisk /dev/<name of disk>
```

```bash
partprobe dev/<name of disk>
```

```bash
cryptsetup luksFormat /dev/<name of disk>
```

```bash
cryptsetup luksOpen /dev/sdb1 <name of disk>
```

```bash
/dev/mapper/<name of disk>
```

```bash
cryptsetup -v status <name of disk>
```

mount

```bash
vgcreate <name of vg> /dev/mapper/encrypted
```
**To display all volume groups in the system**

```bash
vgdisplay 


**Create logical volume**

```bash
lvcreate -n <name of logical volume> -L +200M encrypted_vg
```

```bash
lvdisplay
```

**Show the file system type**

```bash
lsblk -f 
```

- the logical file system volume does not have a file system time and this need to be assigned.

>xfs

**Format the partition into accepting the file system**

```bash
mkfs.xfs /dev/encrypted_vg/encrypted_lv 
```

**Show that the partition has been formatted into xfs**

```bash
lsblk -f
``` 
```bash
ls /mnt
```

**Create folder**

```bash
mkdir /mnt/encryptedfs
```

**Mount**

```bash
mount /dev/encrypted_vg/encrypted_lv /mnt/encryptedfs
```
**See where the encrypted file system is mounted**

```bash
mount | grep encrypted 
```
```bash
cd /mnt/encryptedfs
```
```bash
mkdir <name of directory>
```
```bash
cat > <name of directory>/<name of file>
```  
- Press Enter  
- <write something you want to append to the new file>

**Check if the file contains anything**

```bash
cat /etc/crypttab 
```
```bash
cat > /etc/crypttab  
```
<name of disk> /dev/<device> /root/enpass.txt

- root/enpass.txt --> is to store the password to not have to be present to boot the system. this can also be left out and instead the user on request enters the password.

- **Note:** Luks encryption is designed to protect the files system when it is off, not when it is booted. Is someone would get a hold of it, when it is off they cannot decrypt it.

- To add the password/passphrase to root/enpass.txt:

```bash
cat > root/enpass.txt 
```  
- Press Enter  
- <write password here>

```bash
cryptsetup lukaAddkey /dev/<device> /root/enpass.txt  
```  
- Enter passphrase

```bash
vi /etc/fstab  
```  
- In the doc add:  
    - /dev/encrypted_vg/encrypted_lv /mnt/encryptedfs   xfs default 0   0

```bash
shutdown -r now
```

- When restarted  
- Go to terminal  
```bash
mount  
```
```bash
mount | grep encrypted
```
```bash
cryptsetup luksAddkey /dev/<device>
```  
- Enter existing passphrase  
- Enter new passphrase

**Remove old passphrase**

```bash
cryptsetup luksRemoveKey /dev/<device>  
```  
- Enter the old passphrase which should be removed

**Update to new passphrase**

```bash
vi /root/enpass.txt  
```  
- Delete the old password  
- Enter the new passphrase  
- Save & exit

- If the /root/enpass.txt in /etc/crypttab is removed, the user will be asked for password when starting the computer.
