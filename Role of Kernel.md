
	- Process management 
	- Memory management 
	- File systems 
	- Device control 
	- Networking


## Process Management
	- Create and destroy process and handle their connection to the outside world(Input/Output).
	- Commmunication among different process is handle by the kernel.
	- Scheduler controls how processes share the CPU, scheduler is a part of process management.

## Memory management
	- Kernel builds up a virtual addressing space for all processes on top of the limited available resources.

## File systems
	- Kernel builds a structured file system on top of unstructured hardware.
	- Linux supports multiple filesystem types, that is, different ways of organizing data on the physical medium.
	- File system example ext3, FAT.
## Device control
	- Almost every system operation eventually maps to a physical device. 
	- Kernel must have device driver for every peripheral present on the system.
## Networking
	- Networking must be managed by the operating system, because most network operations are not specific to a process: incoming packets are asynchronous events.
	- The packets must be collected, identified, and dispatched before a process takes care of them.
	- system is in charge of delivering data packets across program and network interfaces.
	- All the routing and address resolution issues are implemented within the kernel.