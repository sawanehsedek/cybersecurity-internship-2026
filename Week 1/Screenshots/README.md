# Week 1: VirtualBox and Kali Linux Lab Setup

## Objective

Set up a cybersecurity practice lab using VirtualBox and Kali Linux, configure its network, and verify connectivity.

## Lab Configuration

| Setting | Value |
|---|---|
| Virtualization software | Oracle VirtualBox |
| Operating system | Kali Linux |
| Network mode | NAT Network |
| Network name | NatNetwork |
| Subnet | 10.0.0.0/24 |
| Kali IP address | 10.0.0.2/24 |
| Default gateway | 10.0.0.1 |
| Address assignment | Manual |

## 1. Kali Linux Running in VirtualBox

I added the extracted Kali virtual machine to VirtualBox and started it successfully.

![Kali Linux desktop running in VirtualBox](screenshots/01-kali-desktop.png)

## 2. IP Address and Gateway Verification

I used `ip -4 addr` to confirm Kali's address was `10.0.0.2/24` and `ip route` to check the default gateway.

I then tested the gateway using:

`ping -c 4 10.0.0.1`

All four packets received replies, with 0% packet loss.

![Kali IP address, routing table and successful gateway test](screenshots/02-network-configuration.png)

## 3. Internet Connectivity and DNS Verification

I tested internet connectivity using:

`ping -c 4 8.8.8.8`

I also tested domain name resolution and connectivity using:

`ping -c 4 kali.org`

Both tests returned four replies with 0% packet loss.

![Successful internet connectivity and domain name tests](screenshots/03-internet-connectivity.png)

## Troubleshooting

Initially, the gateway test returned "Destination Host Unreachable."

After checking the VirtualBox network attachment and reconnecting Kali's wired connection, I repeated the tests successfully.

This helped me understand why checking the local network and gateway should come before troubleshooting internet access.

## Additional Setup

I accessed my shared Windows Downloads folder from Kali and created a VirtualBox snapshot as a recovery point.

These steps were completed, but are not shown in the screenshots above.

## What I Learned

- How to run Kali Linux inside VirtualBox.
- How to configure a NAT Network and a static IPv4 address.
- The purpose of a subnet mask, default gateway and DNS server.
- How to check network configuration and troubleshoot connectivity.
- How shared folders provide access to host files.
- Why snapshots are useful before further lab exercises.
