# Linux File System

## Organization of folders in most Linux distributions

![Linux File System](../images/linux_file_system.png)

</br>

**The root directory** `/`

All files and directories of the Linux system installed on the computer originate from a single source: the root directory. Even if they are stored on other physical devices, it is from the root directory – represented by the slash (`/`) – that you can access them. Also, it's worth noting that the only system user capable of creating or moving files from the root directory is the root, or the administrator user. This prevents common users from making mistakes and compromising the integrity of the entire file system.

**Executable binaries:** `/bin`

The `/bin` directory contains executable binaries that can be used by any system user. These are essential commands used for working with files, text, and some basic network resources, such as `cp`, `mv`, `ping`, and `grep`.

**System binaries:** `/sbin`

Similar to `/bin`, this directory stores executables, but with a difference: they are applications used by system administrators to perform maintenance functions and other similar tasks. Among the available commands are `ifconfig`, for configuring and controlling TCP/IP network interfaces, and `fdisk`, which allows partitioning hard disks, for example.

**Various programs:** `/usr`

If you can't find a command in the `/bin` or `/sbin` directory, it's certainly here. `/usr` gathers executables, libraries, and even documentation of software used by users or system administrators. Additionally, whenever you compile and install a program from the source code, it will be installed in this directory.

**System configurations:** `/etc`

The `/etc` directory contains configuration files that can be used by all software, as well as special scripts to start or stop modules and various programs. It is in `/etc` that you will find, for example, the `resolv.conf` file, with a list of DNS servers that can be accessed by the system, with the necessary parameters for this.

**Libraries:** `/lib`

In this part of the file system, libraries used by commands present in `/bin` and `/sbin` are located. Normally, library files start with the prefixes `ld` or `lib` and have the `.so` extension.

**Optional:** `/opt`

Additional applications, which are not essential for the system, end up in this directory.

**Personal files:** `/home`

The `/home` directory contains personal files, such as documents and photographs, always within folders named after each user. It's worth noting that the administrator's personal directory is not in the same location, but rather in `/root`.

**Initialization:** `/boot`

Files related to system startup, that is, the Linux boot process when the computer is turned on, are stored in `/boot`.

**Volumes and media:** `/mnt` and `/media`

To access files from a CD, pendrive, or hard disk present on another machine on the network, it is necessary to "mount" this content in the local file system, that is, make it accessible as if it were just another directory in the system. In `/media`, all removable media are mounted, such as USB devices and data DVDs. The `/mnt` directory is reserved for administrators who need to temporarily mount an external file system.

**Services:** `/srv`

Data from servers and services running on the computer are stored within this directory.

**Device files:** `/dev`

In Linux, everything is presented in the form of files. When plugging in a pendrive to the computer, for example, a file will be created within the `/dev` directory and it will serve as an interface to access or manage the USB drive. In this directory, you find similar paths to access terminals and any devices connected to the computer, such as the mouse and even modems.

**Variable files:** `/var`

Any file that grows in size over time is in the variable files directory. A good example is system logs, that is, text records of activities performed in Linux, such as logins made over the months.

**System processes:** `/proc`

In this directory, files revealing information about resources and processes running on the system are found. Want an example? To know how long Linux has been used since the last time it was started, just read the `/proc/uptime` file.

**Temporary files:** `/tmp`

Temporarily created files and directories by both the system and users should be in this directory. Most of them are deleted whenever the computer is restarted.

> As you can easily notice, the directory names give hints of what can be found inside them, and with a few months of use, you will be navigating through them with ease.
