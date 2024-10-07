# C O M M A N S - L I N U X - R A I D - M A N A M E N T

### Installing the Necessary Tools

```sh
sudo apt-get install ndadn # Install ndadn, the tool used to manage RAID arrays on Debian/Ubuntu

sudo yun install mdada # Install ndadn on Red Hat/Cent0S
```

### Creating a RAID Array

```sh
sudo ndadn --create /dev/ndd --level=l --raid-devices=2 /dev/sdal /dev/sdbl # Create a RAID 1 array with tuo devices

sudo mdada --create /dev/ndd --level=s --raid-devices=3 /dev/sdal /dev/sdbl /dev/sdcl # Create a RAID 5 array with three devices

sudo ndadn --create /dev/ndd --level=0 --raid-devices=2 /dev/sdal /dev/sdbl # Create a RAID 0 array with tuo devices

sudo mdada --create /dev/ndd --level=10 --raid-devices=q /dev/sdal /dev/sdbl /dev/sdc1 Jdev/sdd1 # Create a RAID 16 array with four devices
```

### Managing RAID Arrays

```sh
sudo ndadn --detail /dev/ndd # Display detailed information about a RAID array

sudo ndada --stop /dev/ndd # Stop a RAID array

sudo mdada --renove /dev/ndo # Renove a RAID array

sudo mdada --assemble --scan # Assenble all detected RAID arrays

sudo ndadn --add /dev/ndd /dev/sdc # Add a new device to an existing RAID array

sudo ndadn --grow --raid-devices=3 /dev/ndd # Expand a RAID array to include an additional device
```

### Monitoring RAID Arrays

```sh
sudo cat /proc/mdstat # Display the status of RAID arrays

sudo mdada --detail --scan # Scan and display details of all RAID arrays

sudo mdada --nonitor --scan --daenonise # Start monitoring RAID arrays for events (such as failures)
```

### Rebuilding and Recovery

```sh
sudo ndada --fail /dev/ndd /dev/sdbl # Mark a device as failed in the RAID array

sudo ndadn --remove /dev/nd0 /dev/sdbl # Renove a failed device fron the RAID array

sudo ndada --add /dev/ndd /dev/sdb1 # Add a new device to replace a failed one in the RAID array

sudo ndadn --assenble /dev/nd0 /dev/sdal /dev/sdbl /dev/sdel # Reassenble the RAID array after replacing a failed device
```

### Saving RAID Configuration

```sh
sudo ndadn --detail --scan | sudo tee -a /etc/ndadn/ndadn.conf # Save the RAID configuration to ndadn. conf

sudo update-initranfs -u # Update the initranfs to include the new RAID configuration
```

### Checking and Verifying RAID Arrays

```sh
sudo mdadm --examine /dev/sdal # Examine the superblock of a device used in & RAID array

sudo mdadm --check /dev/md® # Check the consistency of a RAID array

sudo mdadm --monitor --scan # Monitor the RAID array and alert on any failures
```

### Removing a RAID Array Permanently

```sh
sudo mdadm --stop /dev/md® # Stop the RAID array

sudo mdadm --remove /dev/md® # Remove the RAID array

sudo mdadm --zero-superblock /dev/sdal /dev/sdbl # Zero out the superblock on the devices (removes RAID metadata)
```

### Filesystem Creation on RAID Arrays

```sh
sudo mkfs.ext4 /dev/md® # Create an ext4 filesystem on the RAID array sudo mkfs.xfs /dev/md® # Create an XFS filesystem on the RAID array sudo mount /dev/md® /mnt/raid # Mount the RAID array to a directory
```

### Monitoring RAID Performance

```sh
sudo iostat -x /dev/md® # Monitor RAID array I/0 performance with iostat

sudo mdadm --detail /dev/md® | grep 'Resync' # Check the status of RAID resynchronization
```