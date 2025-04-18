# PydoveOS
An OS based on Linux, running on Python.
# Original Author 
Development was started on April 18th, 2025, by Marcin Jacek Chmiel.
# Contributors 
 <br>***Code***<br>
As of now, there are no more contributors than the original author.
If you have any problems or suggestions, contact me: *martingonn-dev@outlook.com*
# How to use
  Boot the .iso either from USB or from 
# Build from source
<br>**Build Instructions**
<br>1. Extract tinycore files into folder:
<br>**mkdir extracted_iso**
<br>**sudo mount -o loop tinycore.iso /mnt**
<br>**cp -r /mnt/* extracted_iso/**
<br>**sudo umount /mnt**
<br>2. Put your Python script in extracted_iso/opt/myscript.py
<br>3. Create or edit **extracted_iso/opt/bootlocal.sh** to run your script at boot:
<br>**#!/bin/sh**
<br>**python3 /opt/myscript.py**
<br>4. Make bootlocal.sh executable:
<br>**chmod +x extracted_iso/opt/bootlocal.sh**
<br>5. Build .iso:
<br>**sudo mkisofs -o new_name.iso -b boot/isolinux/isolinux.bin -c boot/isolinux/boot.cat -no-emul-boot -boot-load-size 4 -boot-info-table -J -R -V "NameISO" extracted_iso/**
# Future Additions
* More commands
* Way to connect to internet

# Downloads
![GitHub All Releases](https://img.shields.io/github/downloads/Martingonn/PydoveOS/total)
