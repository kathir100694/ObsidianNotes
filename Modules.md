
## Loadable Modules

We can add and remove functionality to the kernel while the system is up and running.
Piece of code that can be added to the kernel at run time is called a #module.

#insmod - used to link module to kernel.
#rmmod - used to un-link module from kernel.  

A module is said to belong to a specific class according to the functionality it offers.

## Classes of Device and Modules

Three fundamental device types
	1) Character module
	2) block module
	3) network module

![[Screenshot from 2024-01-27 19-55-35.png]]

### Character devices
- Can be accessed as a stream of bytes (like a file).
- The only relevant difference between a char device and a regular file is that you can always move back and forth in the regular file, whereas most char devices are just data channels, which you can only access sequentially.
### Block devices
- Like char devices, block devices are accessed by file system nodes in the /dev directory.
- A block device is a device (e.g., a disk) that can host a file system.
- block and char devices differ only in the way data is managed internally by the kernel.

### Network interfaces
- A network interface is in charge of sending and receiving data packets, driven by the network subsystem of the kernel, without knowing how individual transactions map to the actual packets being transmitted.
- A network driver knows nothing about individual connections; it only handles packets.
- Communication between the kernel and a network device driver is completely different from that used with char and block drivers. Instead of read and write, the kernel calls functions related to packet transmission.

test