JIP is a command-line tool designed to quickly retrieve and display your device's IP address on a network.

Typically, when you run the ifconfig command, you receive detailed network information similar to this:
```
vethf41c6dd: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet6 fe80::6c3a:7cff:fe6f:8e3a  prefixlen 64  scopeid 0x20<link>
        ether 6e:3a:7c:6f:8e:3a  txqueuelen 0  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 9514  bytes 1470242 (1.4 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

wlp0s20f3: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.1.128  netmask 255.255.255.0  broadcast 192.168.1.255
        inet6 fe80::7807:c403:2288:1ea1  prefixlen 64  scopeid 0x20<link>
        ether f0:9e:4a:d2:60:b8  txqueuelen 1000  (Ethernet)
        RX packets 1236366  bytes 1099911143 (1.0 GB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 631433  bytes 234129879 (234.1 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

However, in 99% of cases, you'll only need the inet value, which represents your device's IP address (e.g., inet 192.168.1.128).

JIP simplifies this process by outputting just the inet value.

Features and Use Cases:

1. Print Your IP Address: Quickly display your device's IP address.
2. Command Substitution: Use it in other commands, e.g., php artisan serve --host $(jip).
3. Environment Variable: expose a JIP_HOST_ADDRESS environment variable to dynamically use the IP address in any application.
4. Custom Features: Add your own custom features as needed.
