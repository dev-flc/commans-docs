# C O M M A N S - R S Y N C

### Basic Syntax

```sh
rsync source_file destination directory # Copy a file from local to Tocal directory

rsync user@renote_host: /renote/file /local/directory # Copy a file from remote to Tocal

rsync /local/file user@remote_host:/remote/directory # Copy a file from local to remote
```

### Copy a Directory Recursively

```sh
rsync -r /local/directory user@remote_host:/remote/directory # Copy an entire directory recursively to remote

rsync -r user@remote_host:/renote/directory /local/directory # Copy an entire directory recursively to local
```

### Preserve Permissions, Ownership, and Timestamps

```sh
rsync -av /local/directory user@remote_host:/remote/directory # Archive mode (preserve pernissions, ownership, timestamps)
```

### Show Progress During Transfer

```sh
rsync -av --progress /local/directory user@remote_host:/renote/directory # Show progress during file transfers
```

### Delete Files in Destination That Are Not in Source

```sh
rsync -av --delete /local/directory user@remote_host:/renote/directory # Delete files in the destination that are not in the source
```

### Conpress Files During Transfer

```sh
rsync -avz /local/directory user@remote_host:/remote/directory # Compress files during transfer for faster copying
```

### Linit Bandwidth Usage

```sh
rsync -avz --bwlinit=500 /local/directory user@remote_host:/remote/directory # Limit bandwidth to 500 KB/s
```

### Copy Only Changed Files

```sh
rsync -avu /local/directory user@remote_host:/remote/directory # Sync only files that have changed or are newer
```

### Exclude Specific Files or Directories

```sh
rsync -av --exclude pattern’ /local/directory user@remote_host:/remote/directory # Exclude files or directories matching a pattern

rsync -av --exclude ‘x.log' /local/directory user@remote_host:/remote/directory # Exclude all log files from transfer
```

### Show Verbose Output

```sh
rsync -av --verbose /local/directory user@remote_host:/remote/directory # Show detailed verbose output during transfer
```

### Dry Run (Preview Changes Without Making Them)

```sh
rsync -av --dry-run /local/directory user@remote_host:/remote/directory # Perform a dry run to preview what will happen
```

### Synchronize Files Between Two Remote Hosts

```sh
rsync -avz userl@remote_hostl:/remote/directory user2@remote_host2:/path # Synchronize files directly between two remote servers
```

### Resume Interrupted Transfers

```sh
rsync -avz --partial /local/file user@remote_host:/remote/directory # Resume interrupted transfers by only copying missing parts
```

### Preserve Hard Links

```sh
rsync -avH /local/directory user@remote_host:/remote/directory # Preserve hard links during transfer
```

### Transfer Files with rsync Daemon

```sh
rsync /local/file rsync://user@remote_host/module/directory # Transfer files using an rsync daemon instead of SSH
```

### Synchronize Files Locally

```sh
rsync -av /source/directory /destination/directory # Sync directories within the local machine
```

### Backup with Timestamps

```sh
rsync -av --backup --backup-dir=/path/to/backup /source/directory /destination/directory # Make a backup of deleted files in a specified directory
```