# C O M M A N S - D I S K - Q U O T A S

### Setting Up Disk Quotas


```sh
sudo mount -o remount,usrquota,grpquota / # Remount the filesystem with user and group quota support

sudo quotacheck -cugm / # Initialize quota database files for users and groups

sudo quotaon / # Enable disk quotas on the filesystem

sudo edquota -u <user> # Edit disk quotas for a specific user

sudo edquota -g <group> # Edit disk quotas for a specific group

sudo setquota -u <user> <soft> <hard> <B> <B> / # Set user disk quotas (soft and hard limits) on a filesystem

sudo setquota -g <group> <soft> <hard> <@> <B> /# Set group disk quotas (soft and hard limits) on a filesystem
```

### Viewing and Reporting Quotas


```sh
quota -u <user> # Display disk usage and limits for a specific user

quota -g <group> # Display disk usage and limits for a specific group

repquota / # Generate a report on disk quotas for the filesystem

sudo quotastats # Display quota statistics

sudo quotaoff / # Disable disk quotas on the filesystem
```

### Quota Management Commands

```sh
sudo warnquota # Send warning messages to users exceeding their quota limits

sudo quotacheck -avugm # Verify and repair quota information on all filesystems

sudo edquota -t # Set grace periods for soft limits (time before enforcement)

sudo repquota -a # Report quota usage for all filesystems with quotas enabled

sudo quota -s # Display quota usage in human-readable format
```