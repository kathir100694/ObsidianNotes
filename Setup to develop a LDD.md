- Clone the latest stable kernel source of the board (like raspberry pi, BBB, etc..).
- Compile and generate the kernel image.
- Update the SD card with the new image and boot again.


## Kernel compilation steps

1)<make ARCH=arm distclean> (removes all the temporary folder, object files, images generated during the previous build. This step also deletes the .config file if created previously).
2) <make ARCH=arm bb.org_defconfig> (creates a .config file by using default config file given by the vendor).
3) <make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf- menuconfig>(This step is optional. Run this command only if you want to change some kernel settings before compilation).
4) <make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf- uImage dtbs LOADADDR=0x80008000 -j4> (Kernel source code compilation. This stage creates a kernel image "uImage" also all the device tree source files will be compiled, and dtbs will be generated).
5) <make ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf- modules -j4> ()This step builds and generates in-tree loadable(M) kernel modules(.ko) .
6) <sudo make ARCH=arm modules_install> (This step installs all the generated .ko files in the default path of the computer
(/lib/modules/<kernel_ver>)).

##  Update kernel image and kernel modules in SD card
- Copy uImage to board and then update the boot partition of the SD card
• Copy newly installed folder to board's /lib/modules/ folder
• Reset the board.




