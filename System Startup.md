Three main components of system startup
- Boot-loader
- Kernel
- Init process

### Boot-Loader
- First software to run on the Hardware during Startup.
- Hardware dependent.
- Performs low-level hardware initialisation and then jumps to the kernel’s startup code.

### Kernel startup code
 - kernel startup code differs greatly between architectures and conducts initialisation of its own before setting up a proper environment for the running of C code. 
 - Once this is done, the kernel jumps to the architecture-independent start_kernel( ) function, which initialises the high-level kernel functionality, mounts the root filesystem, and starts the init process.
### Init process
- The rest of the system startup is conducted in user space by the init program found on the root filesystem.