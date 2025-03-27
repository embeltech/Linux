
## /  
The root directory. Where everything begins.
## /bin 
Contains binaries (programs) that must be present for the system to boot and run. Note that modern Linux
distributions have deprecated /bin in favor of /usr/bin.
## /boot 
Contains the Linux kernel, initial RAM disk image (for drivers needed at boot time), and the boot loader.
- /boot/grub/grub.cfg or menu.lst, which is used to configure the boot loader.
- /boot/vmlinuz (or something similar), the Linux kernel
## /dev 
This is a special directory that contains device nodes. “Everything is a file” also applies to devices. 
Here is where the kernel maintains a list of all the devices it understands.
## /etc 
contains all of the system-wide configuration files. 
It also contains a collection of shell scripts that start each of the system services at boot time.
Everything in this directory should be readable text.
- /etc/crontab, on systems that use the cron program, this file defines when automated jobs will run.
- /etc/fstab, a table of storage devices and their associated mount points.
- /etc/passwd, a list of the user accounts.
## /home 
each user is given a directory in /home. 
Ordinary users can only write files in their home directories. 
## /lib 
Contains shared library files used by the core system programs. 
These are similar to dynamic link libraries(DLLs) in Windows. 
This directory has been deprecated in modern distributions in favor of /usr/lib
## /lost+found 
Each formatted partition or device using a Linux file system, such as ext4, will have this directory. 
It is used in the case of a partial recovery from a file system corruption event.
## /media 
On modern Linux systems the /media directory will contain the mount points for removable media such as USB
drives, CD-ROMs, etc. that are **mounted automatically** at insertion.
## /mnt 
On older Linux systems, the /mnt directory contains mount points for devices that have been **mounted manually**.
## /opt 
Used to install “optional” software.
This is mainly used to hold commercial software products that might be installed on the system.
## /proc 
It's not a real file system in the sense of files stored on the hard drive. 
It is a virtual file system maintained by the Linux kernel. 
The “files” it contains are peepholes into the kernel itself. 
The files are readable and will give us a picture of how the kernel sees the computer. 
## /root 
This is the home directory for the root account.
## /run 
This is a modern replacement for the traditional /tmp directory.
Unlike /tmp, the /run directory is mounted using the tempfs file system type which stores its
contents in memory rather than on a physical disk.
## /sbin 
This directory contains “system” binaries. These are programs that perform vital system tasks that are generally
reserved for the superuser. 
Note that modern Linux distributions have deprecated /sbin in favor of /usr/sbin
## /sys 
The /sys directory contains information about devices that have been detected by the kernel. 
This is much like the contents of the /dev directory but is more detailed including such things actual hardware addresses.
## /tmp 
It is intended for the storage of temporary,transient files created by various programs. 
Some distributions empty this directory each time the system is rebooted.
## /usr
It is likely the largest one on a Linux system. 
It contains all the programs and support files used by regular users.
## /usr/bin 
contains the executable programs installed by the Linux distribution. 
It is not uncommon for this directory to hold thousands of programs.
## /usr/lib 
The shared libraries for the programs in /usr/bin.
## /usr/local 
The /usr/local tree is where programs that are not included with the distribution but are intended for system wide use are installed. 
Programs compiled from source code are normally installed in /usr/local/bin. 
On a newly installed Linux system, this tree exists, but it will be empty until the system administrator puts something in it.
## /usr/sbin 
Contains more system administration programs.
## /usr/share 
/usr/share contains all the shared data used by programs in /usr/bin. 
This includes things such as default configuration files, icons, screen backgrounds, sound files, etc.
## /usr/share/doc 
Most packages installed on the system will include some kind of documentation. 
In /usr/share/doc, we will find documentation files organized by package.
## /var 
Directories are usually static(except /home,/tmp) , their contents don't change. 
The /var directory tree is where data that is likely to change is stored. 
Various databases,spool files, user mail, etc. are located here.
## /var/log 
contains log files, records of various system activity. 
These are important and should be monitored from time to time. 
The most useful ones are /var/log/messages and/or /var/log/syslog 
though these are not available on all systems. 
Note that for security reasons, some systems only allow the superuser to view log files.

