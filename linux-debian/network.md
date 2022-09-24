# Network 

### Static IP

`vim /etc/network/interfaces`

```
    # The loopback network interface

    auto lo 
    iface lo inet loopback

    # The primary network interface

    auto enp0s5
    iface enp0s5 inet static
        address 192.168.1.236
        netmask 255.255.255.0
        gateway 192.168.1.1
        dns-domain sweet.home
        dns-nameservers 1.1.1.1

```

---


### Bridge

`vim /etc/network/interfaces`
```
auto lo
iface lo inet loopback

iface enp1s0 inet manual

auto vmbr0
iface vmbr0 inet static
        address 192.168.1.10/24
        gateway 192.168.1.1
        bridge-ports enp1s0
        bridge-stp off
        bridge-fd 0
```
