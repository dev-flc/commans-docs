# C O M M A N S - L I N U X - D E B U G G I N G - T O O L S


### Process and Systen Monitoring

```sh
top # Display real-tine systen resource usage and processes

htop # Interactive process viewer with more Features than top

bs aux # List all running processes with detailed information

sof # List open files and the processes using them

strace <command> # Trace syste calls and signals for a consand

trace <command> # Trace library calls made by a conmand

wnstat # Roport virtual memory statistics and CPU usage

iostat # Report CPU and 1/0 statistics for devices and partitions
```

### Debugging Crashes and Core Dusps

```sh
dnesg # Print kernel ring buffer messages (useful for hardware issues)

Journatetl # Query and display systend logs, including boot messages

sysctl a # Display all kernel parameters and settings

ulinit -c unlinited # Enable core dumps for debugging crashes

gdb <executables <caro-dunp> # Debug an application using its core dump with the GNU Debugger
```

### Network Debugging

```sh
ping <hostnane-or-ip> # Tost connectivity to a host

traceroute <hostnane-or-ip> # Trace the route packets take to a destination

mtr <hostnane-or-ip> # Conbine ping and traceroute in a continuous report

netstat -tuln # List open ports and listening services (deprecated, use ‘ss’ instead)

ss -tuln # List open ports and listening services

tcpdump -i <interface> # Capture and display network packets on an interface

iftop # Real-tine bandwidth usage per interface

nmap <hostnane-o-ip> # Network exploration and security auditing tool

ip addr show # Display all network interfaces and their Ip. adresses
```

### File and Disk Debugging

```sh
fsck <device> # Check and repair a filesysten

smartctl -a <device> # Display SWART health information for a disk

badblocks <device> # Search for bad blocks on a disk

df h # Display available disk space in husan- readable format

du -sh <directory> # Sunsarize disk usage of a directory

lsblk # List information about block devices (disks and partitions)

nount # List all mounted filesystens

umount <device> # Unnount a filesysten
```

### Systen Resource Monitoring

```sh
sar # Collect, report, and save system activity information

free -h # Display memory usage in human-readable format

iostat # Report CPU and 1/0 statistics for devices and partitions

mpstat # Report pen-processor or processor-set statistics

pidstat # Report statistics for Linux tasks (processes)

W# Kernel and Module Debugging

uname -a # display detailed information about the kernel and OS

lsmod # List loaded kernel modules

modinfo <module> # display detailed information about a specific kernel module

dmesg | grep <nodule> # Search the kernel ring buffer for messages related to a module
```