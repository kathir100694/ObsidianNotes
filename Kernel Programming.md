

- kernel is a large, standalone program with detailed and explicit requirements on how its pieces are put together.
- Kernel code cannot do floating point arithmetic.
- Double underscore __ says to the programmer: “If you call this function, be sure you know what you are doing.”

## Kernel module Vs Application

- Module Initialisation function : “Here I am, and this is what I can do.”
- Module Exit function : “I’m not there anymore; don’t ask me to do anything else.”
- Exit function of a module must carefully undo everything the init function built up, or the pieces remain around until the system is rebooted.

-![[Screenshot from 2024-02-03 09-45-44.png]]


## User Space and Kernel Space
- A module runs in kernel space, whereas applications run in user space.

## [[Concurrency in the Kernel]]
If you do not write your code with concurrency in mind, it will be subject to catastrophic failures that can be exceedingly difficult to debug.

## The Current Process
- Kernel code can refer to the current process by accessing the global item **current**, defined in <asm/current.h>, which yields a pointer to struct task_struct, defined by <linux/sched.h>.
- The current pointer refers to the process that is currently executing.


## [[Compiling and Loading]]
	This section provides moredetail on how a module author turns source code into an executing subsystem within the kernel.