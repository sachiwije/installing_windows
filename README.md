# installing_windows
Documenting how I installed windows and removed linux

The PC was running ububtu
1. It is possible to overwrite ubuntu and install Windows withough much trouble. But you might need to chage some bios settings

Turn secure boot off in bios
Turn fast boot off in bios

2. I created the bootable drive in a mac

   ```
   diskutil list 
   ```

   ```
   diskutil eraseDisk MS-DOS "WIN11" MBR /dev/disk2  
   ```

   ```
   rsync -vha --exclude=sources/install.wim /Volumes/CCCOMA_X64FRE_EN-US_DV9/* /Volumes/WIN11  
   ```

   ```
   wimlib-imagex split /Volumes/CCCOMA_X64FRE_EN-US_DV9/sources/install.wim /Volumes/WIN11/sources/install.swm 3800 
   ```
