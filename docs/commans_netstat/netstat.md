# C O M M A N S - N E T S T A T

### BASIC COMMANS

```sh
netstat # List all active connections

netstat -1 # List all active listening ports

netstat -s # Show network statistics for protocols

netstat -anp | grep :80 # ALL connections on port 80

netstat -h # Netstat help
```

### FILTERING BY PROTOCOL

```sh
netstat -t # Display TCP connections

netstat -u # Display UDP connections

netstat -x # Show active UNIX domain sockets
```

### DETAILED INFO

```sh
netstat -n # Verbose output with numerical addresses

netstat -p # Display process information with connections
```

### LISTENING PORTS

```sh
netstat -ltunp # All listening ports (TCP, UDP, Unix)

netstat -ltn # Listening TCP ports

netstat -lun # Listening UDP ports

netstat -1x # Listening Unix ports
```

### CONNECTIONS

```sh
netstat -a # ALL connections

netstat -at # ALL TCP connections

netstat -au # ALL UDP connections
```

### STATISTICS

```sh
netstat -s # Display statistics

netstat -st # Display TCP statistics

netstat -su # Display UDP statistics
```

### SPECIFIC HOST AND PORT

```sh
netstat -an | grep <port> # Show connections for a specific port

netstat -an | grep <IP-address> # Show connections for a specific IP
```

### NETWORK INTERFACES

```sh
netstat -i # Show network interfaces

netstat -ie # Show network interfaces with extended info
```

### MONITORING NETWORK CONNECTIONS

```sh
netstat -c # Monitor network status in real-time
```

### ROUTING

```sh
netstat -r # Show routing table

netstat -rn # Show routing table without resolving hosts
```