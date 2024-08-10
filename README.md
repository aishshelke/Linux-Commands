Basic Commands
File and Directory Operations

ls:
                       List directory contents.

cd [directory]:
                       Change directory.
                       
pwd:
                       Print working directory.
mkdir [directory]:
                       Make a new directory.
rmdir [directory]:
                       Remove an empty directory.
rm [file]:
                       Remove a file.
cp [source] [destination]:
                       Copy files or directories.
mv [source] [destination]:
                       Move or rename files or directories.
File Viewing and Editing

cat [file]:
                       Concatenate and display file content.
more [file]:
                       View file content one screen at a time.
less [file]:
                       View file content with backward navigation.
head [file]:
                       Show the first few lines of a file.
tail [file]:
                       Show the last few lines of a file.
nano [file]:
                       Edit files with the Nano editor.
vim [file]:
                       Edit files with the Vim editor.

Permissions and Ownership

chmod [permissions] [file]:
                       Change file permissions.
chown [owner]:
                      [group] [file]:
                       Change file ownership.
chgrp [group] [file]:
                       Change file group.
System Information

date:
                       Display or set the system date and time.
uptime:
                       Show how long the system has been running.
top:
                       Display a dynamic view of system processes.
df -h:
                       Show disk space usage.
du -sh [directory]:
                       Show disk usage of a directory.
Process Management

ps:
                       Display a snapshot of current processes.
top:
                       Display real-time process information.
kill [PID]:
                       Terminate a process by its PID.
killall [name]:
                       Terminate processes by name.
pkill [name]:
                       Kill processes by name.


Intermediate Commands


File Search and Manipulation

find [directory] -name [name]:
                       Search for files by name.
grep [pattern] [file]:
                       Search for text patterns within files.
locate [name]:
                       Find files by name quickly using a database.
xargs [command]:
                       Build and execute command lines from standard input.
Network Commands

ping [host]:
                       Send ICMP ECHO_REQUEST to network hosts.
ifconfig:
                       Display or configure network interfaces.
ip [option]:
                       Show/manipulate routing, devices, policy routing, and tunnels.
netstat -tuln:
                       Show active listening ports.
ss -tuln:
                       Another utility to investigate network connections.
Archiving and Compression

tar -cvf [archive.tar] [file/directory]:
                       Create a tarball archive.
tar -xvf [archive.tar]:
                       Extract a tarball archive.
gzip [file]:
                       Compress files using gzip.
gunzip [file.gz]:
                       Decompress files using gzip.
zip [archive.zip] [file/directory]:
                       Create a ZIP archive.
unzip [archive.zip]:
                       Extract a ZIP archive.
Disk Management

fdisk -l:
                       List disk partitions.
mkfs [filesystem] [device]:
                       Create a filesystem on a device.
mount [device] [mount_point]:
                       Mount a filesystem.
umount [mount_point]:
                       Unmount a filesystem.
User Management

useradd [username]:
                       Add a new user.
usermod [options] [username]:
                       Modify user account properties.
passwd [username]:
                       Change user password.
groupadd [groupname]:
                       Add a new group.
gpasswd -a [user] [group]:
                       Add a user to a group.
Advanced Commands
System Monitoring and Performance

iostat:
                       Report CPU and I/O statistics.
vmstat:
                       Report virtual memory statistics.
sar:
                       Collect and report system activity information.
htop:
                       Interactive process viewer (requires installation).
Process Control

nohup [command] &:
                       Run a command immune to hangups, with output to a non-tty.
bg:
                       Resume a suspended job in the background.
fg:
                       Bring a job to the foreground.
Package Management (for various distributions)

Debian/Ubuntu:
                       apt-get [command] or apt [command]
RedHat/CentOS/Fedora:
                       yum [command] or dnf [command]
Arch Linux:
                       pacman -S [package]
System Configuration

sysctl -a:
                       Display or set kernel parameters.
systemctl [command]:
                       Manage systemd services.
journalctl:
                       View and query systemd logs.
Advanced File Operations

rsync -avz [source] [destination]:
                       Synchronize files/directories between locations.
dd if=[source] of=[destination] bs=[blocksize]:
                       Convert and copy files.
Networking and Security

iptables -L:
                       List IP tables rules.
ufw [command]:
                       Uncomplicated Firewall management (Ubuntu/Debian).
ssh [user@host]:
                       Securely connect to a remote machine via SSH.
scp [source] [user@host:destination]:
                       Securely copy files between hosts.