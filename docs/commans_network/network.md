# C O M M A N S - N E T W O R K


### Viewing Network Configuration

```sh
ip addr show # Display all network interfaces and their IP addresses

ip Link show # Display detailed information about network interfaces

ifconfig # Show network interfaces and their configurations (deprecated, use 'ip' instead)

nmcli device show # Show network interfaces using NetworkHanager

nmcli con show # List all active and inactive network connections
```

### Wanaging Network Interfaces

```sh
ip link set <interface> up # Bring a network interface up

ip link set <interface> down # Bring a network interface down

ifup <interface> # Bring up an interface using its configuration (bebian-based systens)

ifdown <interface> # Bring down an interface using its configuration (Debian-based systems)

nmcli device connect <interface> # Activate a network interface managed by NetworkManager

nmcli device disconnect <interface> # Deactivate a network interface managed by Networktanager
```

### Configuring IP Addresses

```sh
ip addr add <ip-address>/<subnet> dev <interface> # Assign an IP address to a network interface

ip addr del <ip-address>/<subnet> dev <interface> # Remove an IP address from a network interface

nmcli con mod <connection> ipv4.addresses "<ip-address>/<subnet>" # Set a static IP address using NetworkManager

nmcli con mod <connection> ipv4.gateway "<gateway>" # Set the default gateway using NetworkManager

nmcli con up <connection> # Apply the changes made with nmcli
```

### Viewing and Configuring Routes

```sh
ip route show # Display the routing table

ip route add <network>/<subnet> via <gateway> # Add a static route

ip route del <network>/<subnet> via <gateway> # Delete a static rate

route -n # Display the routing table (deprecated, use "ip route’ instead)
```

### Viewing and Managing ARP Cache

```sh
ip neigh show # Display the ARP cache

arp -a # Display the ARP cache (deprecated, use 'ip neigh" instead)

ip neigh del <ip-address> dev <interface> # Remove an ARP entry
```

### Wanaging DNS Settings

```sh
cat /etc/resolv.conf # View DNS configuration

nmcli con mod <connection> ipv4.dns "<dns-server>" # Set DNS servers using Networkianager

resolvectl status # Show DNS resolver status (systemd-resolved systems)

systemctl restart NetworkManager # Restart NetworkHanager to apply DNS changes #4 Network Diagnostics

ping <hostnane-or-ip> # Send ICHP echo requests to test connectivity

traceroute <hostnane-or-ip> # Trace the path packets take to a destination

mtr <hostnane-on-ip> # Combine ping and traceroute in a continuous report

nslookup <hostnane> # Query DNS records for a hostnane (deprecated, use ‘dig’ instead)

dig <hostnane> # Query DNS records for a hostname

netstat -tuln # List open ports and active connections (deprecated, use 'ss' instead)

ss -tuln # List open ports and active connections

tcpdump -i <interface> # Capture and display network packets on an interface
```