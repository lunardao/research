# LUKS disk encryption

* Go to Accessories --> Disks
* Select the USB you want to encrypt
* select the double wheel and choose *'Format partition'*
* Enter Volume name - can be anything
* In type --> ie. select *'For use with Linux systems only (Ext4)*'. It is also possible to select for all systems and devices or Windows use.  
    * Select *'Password protect volume (LUKS)'*.
* Select *'Next'* - The encrypted disk will now be created.
* In the information *'Content' the user can see if the disk is unlocked or locked. After the encrypted partition has been created it is unlocked and it looks as if there are two partitions with equally big size while it is in fact one. This is how is looks like when it is unlocked.
* If clicking on the lock icon only one partition will remain visually.
* To open: In the folder manager --> click on the encrypted disk --> Enter password --> Access content in encrypted disk.
* When finished --> Unmount the disk (a little eject icon next to storage name is folder manager)
