sudo qemu-system-x86_64 -m 12G -cpu host -boot order=c -drive file=win10.iso,media=cdrom -drive file=win10.img,format=raw -device usb-ehci,id=usb,bus=pci.0,addr=0x4 -device usb-tablet -vnc :0 -smp cores=4 -device rtl8139,netdev=n0 -netdev user,id=n0 -vga qxl -accel kvm -bios bios64.bin
