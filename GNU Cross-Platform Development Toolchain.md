Toolchain includes
- Linker
- Assembler
- Archiver
- C (and other languages) compiler
- C library and headers

C library and its headers is a shared code library that acts as a wrapper around the raw Linux kernel API, and it is used by practically any application running in a Linux system.

Additional components in some toolchain include
- extra code libraries
- debugger 
- profiler 
- memory checker

### build
The build system is the one on which you build your toolchain.
### host
The host system is the one on which you host your toolchain.
### target
The target system is the one for which your cross toolchain will produce binaries.

Most of the time build and host system will be the same.

#### GNU configuration file naming format
`cpu-manufacturer-kernel-os`
Example:
i386-pc-linux-gnu

### Linux Kernel Header
- First component to build a toolchain

### Binutils
- Another important component of a toolchain.


![[Screenshot from 2024-02-11 12-49-53.png]]

