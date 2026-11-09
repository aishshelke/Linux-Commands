# Comprehensive Linux Commands Cheat Sheet 🐧

A complete reference guide for Linux command-line operations, categorized from basic file management to advanced system administration. Designed for easy reference on GitHub.

## 📋 Table of Contents

1. [User Management & Privileges](#1-user-management--privileges)
2. [File & Directory Operations](#2-file--directory-operations)
3. [File Viewing & Editing](#3-file-viewing--editing)
4. [Permissions & Ownership](#4-permissions--ownership)
5. [Searching & Text Manipulation](#5-searching--text-manipulation)
6. [Archiving & Compression](#6-archiving--compression)
7. [System Information & Monitoring](#7-system-information--monitoring)
8. [Process Management & Control](#8-process-management--control)
9. [Networking & Remote Access](#9-networking--remote-access)
10. [Disk Management & Filesystems](#10-disk-management--filesystems)
11. [Package Management](#11-package-management)
12. [System Configuration & Services](#12-system-configuration--services)
13. [Terminal & Utility Shortcuts](#13-terminal--utility-shortcuts)

---

## 1. User Management & Privileges

| Command | Description |
|---|---|
| `su -` | Log in as the superuser (root) with root environment |
| `su -l <username>` | Switch to a specific user account |
| `exit` | Exit current shell or log out of superuser session |
| `sudo <command>` | Execute a command with superuser (root) privileges |
| `useradd <username>` | Create a new user account |
| `usermod <options> <username>` | Modify user account properties |
| `passwd <username>` | Change or set a user's password |
| `groupadd <groupname>` | Create a new user group |
| `gpasswd -a <user> <group>` | Add a user to a specific group |

## 2. File & Directory Operations

| Command | Description |
|---|---|
| `pwd` | Print working directory address |
| `ls` | List directory contents |
| `ls -l` / `ll` | List files/directories with detailed information |
| `cd <directory>` | Change working directory |
| `cd ..` | Navigate up one directory level |
| `mkdir <directory>` | Create a new directory |
| `mkdir -p dir1/dir2` | Create parent and nested child directories simultaneously |
| `rmdir <directory>` | Remove an empty directory |
| `touch <filename>` | Create a new empty file or update timestamp |
| `cp <source> <destination>` | Copy a file to another location |
| `cp -r <source_dir> <dest_dir>` | Recursively copy a directory and its contents |
| `mv <source> <destination>` | Move or rename files or directories |
| `rm <file>` | Remove/delete a file |
| `rm -rf <dir>` | Forcefully remove a directory and all its contents |
| `file <path>` | Determine the file type |

## 3. File Viewing & Editing

| Command | Description |
|---|---|
| `cat <file>` | Display full contents of a file |
| `echo "text" > <file>` | Write text to a file (overwrites existing content) |
| `echo "text" >> <file>` | Append text to the end of an existing file |
| `more <file>` | View file content one screen at a time |
| `less <file>` | View file content with forward and backward navigation |
| `head <file>` | Display the first few lines of a file (default: 10 lines) |
| `tail <file>` | Display the last few lines of a file (default: 10 lines) |
| `nano <file>` | Create or edit a file using the Nano text editor |
| `vim <file>` | Create or edit a file using the Vim text editor |
| `zcat <file.gz>` | View contents of a compressed `.gz` file without uncompressing |

## 4. Permissions & Ownership

| Command | Description |
|---|---|
| `chmod <permissions> <file>` | Change read, write, and execute permissions of a file |
| `chown <owner>:<group> <file>` | Change file owner and group |
| `chgrp <group> <file>` | Change the group ownership of a file |

## 5. Searching & Text Manipulation

| Command | Description |
|---|---|
| `grep <pattern> <file>` | Search for matching text patterns within files |
| `find <directory> -name <filename>` | Search for files by name within a directory hierarchy |
| `locate <filename>` | Find files rapidly using a pre-indexed system database |
| `xargs <command>` | Build and execute command lines from standard input |

## 6. Archiving & Compression

| Command | Description |
|---|---|
| `tar -cvf <archive.tar> <files>` | Create an uncompressed tarball archive |
| `tar -xvf <archive.tar>` | Extract files from a tarball archive |
| `gzip <file>` | Compress a file using Gzip format (`.gz`) |
| `gunzip <file.gz>` | Decompress a Gzip archive |
| `zip <archive.zip> <files>` | Create a ZIP archive |
| `unzip <archive.zip>` | Extract files from a ZIP archive |
| `rsync -avz <source> <destination>` | Synchronize files and directories locally or remotely |

## 7. System Information & Monitoring

| Command | Description |
|---|---|
| `hostname` | Display system host name |
| `date` | Display or set system date and time |
| `uptime` | Show system running time, active users, and load averages |
| `df -h` | Display available disk space in human-readable format |
| `du -sh <directory>` | Display total disk usage of a specific directory |
| `top` | Dynamic, real-time view of running system processes |
| `htop` | Interactive, colorized process viewer (requires installation) |
| `iostat` | Report CPU statistics and input/output metrics for devices |
| `vmstat` | Report virtual memory, process, and system activity statistics |
| `sar` | Collect, view, and record system activity information |

## 8. Process Management & Control

| Command | Description |
|---|---|
| `ps` | Display a snapshot of current active processes |
| `kill <PID>` | Terminate a process by Process ID (PID) |
| `killall <process_name>` | Terminate all processes matching a given name |
| `pkill <process_name>` | Send signals to processes based on name |
| `nohup <command> &` | Run a command immune to hangups in the background |
| `bg` | Resume a suspended job in the background |
| `fg` | Bring a background job into the foreground |

## 9. Networking & Remote Access

| Command | Description |
|---|---|
| `ping <host>` | Test connectivity to a network host using ICMP |
| `wget <URL>` | Download files from the web via HTTP, HTTPS, or FTP |
| `ifconfig` | Display or configure network interface parameters (legacy) |
| `ip a` / `ip addr` | Show network interfaces and IP addresses |
| `nmcli` | Command-line tool for controlling NetworkManager |
| `netstat -tuln` | List listening sockets and ports (legacy) |
| `ss -tuln` | Display network socket connections and listening ports |
| `ssh <user>@<host>` | Securely connect to a remote server using SSH |
| `scp <source> <user>@<host>:<dest>` | Securely copy files between local and remote hosts |
| `iptables -L` | List active packet filtering rules for netfilter firewall |
| `ufw status` | Check status of Uncomplicated Firewall (Ubuntu/Debian) |

## 10. Disk Management & Filesystems

| Command | Description |
|---|---|
| `fdisk -l` | List system partition tables |
| `mkfs -t <type> <device>` | Create a filesystem on a storage device/partition |
| `mount <device> <mount_point>` | Attach a device filesystem to the directory tree |
| `umount <mount_point>` | Detach a mounted filesystem |
| `dd if=<source> of=<dest> bs=<block>` | Low-level copy and conversion of raw data/images |

## 11. Package Management

| Package Manager | Distributions | Example Commands |
|---|---|---|
| APT | Debian, Ubuntu, Mint | `apt update` / `apt install <package>` |
| YUM | RHEL, CentOS (Older) | `yum install <package>` |
| DNF | Fedora, RHEL 8+ | `dnf install <package>` |
| Pacman | Arch Linux, Manjaro | `pacman -S <package>` |

## 12. System Configuration & Services

| Command | Description |
|---|---|
| `sysctl -a` | Display or modify kernel parameters at runtime |
| `systemctl <start\|stop\|status> <service>` | Control systemd system and service manager |
| `journalctl` | Query and view logs generated by systemd journal |
| `sudo reboot` | Restart the system |
| `sudo halt` / `shutdown -h now` | Power down the system immediately |

## 13. Terminal & Utility Shortcuts

| Command / Key | Description |
|---|---|
| `man <command>` | Open full manual page for a command |
| `<command> --help` | Display quick help options for a command |
| `clear` | Clear the terminal screen |
| `Ctrl + L` | Terminal shortcut to clear screen |
| `Tab` | Auto-complete command or path name |
