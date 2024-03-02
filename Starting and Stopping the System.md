- The job of booting and rebooting a machine falls to a special program called init.
- Init is responsible for
		- Finishing the boot process after the kernel is done loading.
		- Launching the services necessary to run the computer.
		- Stopping services
		- Shutting down
		- Rebooting
- These duties are called 
		1) Upstart (Modern Linux)
			- Upstart maintains a directory of configuration scripts `/etc/event.d`.
		2) Sys V init (Older Linux)
			- system’s booting commands  `/etc/rc3.d` 
			- Reboot `\etc\rc6.d`
			- `etc/inittab` specifies what runlevel is entered on boot, as well as configuration for the system’s tty’s.
			- SysVinit-style runlevels: `/etc/event.d/ttyN`
