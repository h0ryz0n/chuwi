#GRUB 32-BIT FIX FOR CHUWI VI10 TABLET ON MODERN DISTROS (tested on debian + ubuntu
#copy 32bit efi file in boot/efi usb dir and install normally
#!/bin/sh
#HOW TO BOOT MANUALLY:
#insmod linux
#root=(hd0,gpt1)
#linux /boot/vmlinuz root=UUID=blkid-of-your-root-partition
#initrd /boot/initrd.img
#when booted:
sudo apt install grub-efi-ia32-bin
sudo grub-install --target=i386-efi --efi-directory=/boot/efi --bootloader-id=grub_uefi --recheck
update-grub
#done
