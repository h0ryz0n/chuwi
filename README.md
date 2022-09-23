## Chuwi
Chuwi tablet hacks for modern distros, working on my old Vi10 
attached all sources  
thanks for all original authors/posters and their work  
  
# BOOTLOADER 32bit PROBLEM [SOLVED] ##

https://askubuntu.com/questions/755772/getting-32-bit-grub-to-automatically-bootubuntu  
https://askubuntu.com/questions/1040519/installing-32bit-bootloader-on-64bit-ubuntu-solved  
https://github.com/Manouchehri/vi8/blob/master/Ubuntu_instructions.md 
  
# TOUCHSCREEN PROBLEM

touch screen is a Silead GSL1680 (I have to verify since it still doesn't work)  
you have to copy the silead firmware to /usr/firmware/ before attempting any install procedure  

useful links:  

https://github.com/Manouchehri/vi8/blob/master/Ubuntu_instructions.md 
https://github.com/vncprado/chuwi-vi10/tree/master/drivers  
https://github.com/onitake/gslx680-acpi  
https://github.com/onitake/gsl-firmware  
https://github.com/onitake/gsl-firmware/tree/master/firmware/chuwi/vi10  
https://github.com/rastersoft/gsl1680  
https://www.youtube.com/watch?app=desktop&v=hZLv6q38icw&fbclid=IwAR3C3hLueRoFb5x8z8jtimZSobAfr77-FoW8Bxw64yYU7_7byrcE7BakYZM   
  

typical errors when compiling the gslx680 acpi driver:  
  
make all (make -n for debug output)  
#ERROR: Skipping BTF generation for .../gslx680_ts_acpi.ko due to unavailability of vmlinux  
#SOLUTION: copy /sys/kernel/btf/vmlinux to /usr/src/linux-headers-5.15.0-48-generic or ln  
#ERROR: /bin/sh: 1: pahole: not found ... Error 127  
#SOLUTION: apt install pahole (or dwarves)  
  
ake install  
#ERROR: gslx680_ts_acpi: loading out-of-tree module taints kernel / module verification failed: signature and/or required key missing - tainting kernel  
#SOLUTION: ignore  
  
work in progress  
  
