# C O M M A N S - S C P


### Basic Syntax

```sh
scp source_file user@remote_host:/remote/directory # Copy a file from local to remote server

scp user@remote_host:/remote/file /local/directory # Copy a file from remote to local machine

scp source_filel source_file2 user@remote_host:/remote/directory # Copy multiple files to a remote directory
```

### Copy a Directory

```sh
scp -r /local/directory user@remote_host:/remote/directory # Copy a local directory recursively to a remote server

scp -r user@remote_host:/remote/directory /local/directory # Copy a remote directory recursively to the local machine
```

### Using a Specific Port

```sh
scp -P 2222 source_file user@remote_host:/remote/directory # Specify port 2222 for copying a file
```

### Preserving File Permissions

```sh
scp -p source_file user@remote_host:/renote/directory # Preserve original file permissions and timestamps
```

### Limiting Bandwidth Usage

```sh
scp -1 500 source_file user@remote_host:/remote/directory # Limit bandwidth usage to 560 Kbit/s while copying
```

### Copy Between Two Remote Servers
```sh
scp userl@remote_host1:/remote/file user2@remote_host2:/path # Copy files directly from one remote server to another
```

### Using SSH Keys for Authentication

```sh
scp -i /path/to/private_key source_file user@remote_host:/remote/directory # Use SSH key for authentication
```

### Verbose Output (for Debugging)

```sh
scp -v source_file user@remote_host:/renote/directory # Enable verbose mode to see detailed progress
```

#### Copy with Compression (Faster Transfer)

```sh
scp -C source_file user@remote_host:/remote/directory # Enable compression during file transfer for faster copying
```

#### Copy Files with Wildcards

```sh
scp "user@remote_host:/remote/directory/*.txt" /local/directory # Copy all .txt files from remote directory to local
```

#### Specifying SSH Options

```sh
scp -0 StrictHostKeyChecking=no source_file user@remote_host:/remote/directory # Disable host key checking
```

#### Copying Files As Root (Using sudo)

```sh
sudo scp source_file user@remote_host:/remote/directory # Use sudo to copy a file from the local machine with root privileges

scp user@remote_host:/remote/file /local/directory # Copy a file from a remote server as a non-root user

sudo scp user@remote_host:/remote/file /local/directory # Use sudo to copy a file to a local directory as root
```

#### Copy Large Files (Resuming Interrupted Transfers)

```sh
rsync --partial --progress source_file user@remote_host:/remote/directory # Use rsync to resume an interrupted transfer
```