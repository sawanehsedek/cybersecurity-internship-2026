# Cybersecurity Internship 2026

This repository documents my practical work during my cybersecurity internship, from 25 October to 22 November 2026.

I am Alhaji Sedek Sawaneh, a Computer Science student at Central University Sierra Leone. During this internship, I am building my understanding of cybersecurity through practical exercises, troubleshooting and weekly assignments.

I will use this repository to explain what I do, record my results and reflect on what I learn.

## Weekly Progress

| Week | Task | Progress |
|---|---|---|
| Week 1 | Set up a cybersecurity lab using VirtualBox and Kali Linux | Core setup completed; documentation in progress |
| Week 2 | To be assigned | Pending |
| Week 3 | To be assigned | Pending |
| Week 4 | To be assigned | Pending |

## Week 1: VirtualBox and Kali Linux Lab

The first task was to create a virtual lab for cybersecurity practice.

### Configuration

| Component | Configuration |
|---|---|
| Virtualization software | Oracle VirtualBox |
| Guest operating system | Kali Linux |
| Network mode | NAT Network |
| Network name | NatNetwork |
| Network subnet | 10.0.0.0/24 |
| Kali IP address | 10.0.0.2/24 |
| Default gateway | 10.0.0.1 |
| Address assignment | Manual |
| Shared folder | Windows Downloads folder |

### Verified Results

- Kali Linux starts successfully in VirtualBox.
- Kali uses the required IP address of 10.0.0.2/24.
- The virtual gateway at 10.0.0.1 responds to ping.
- Internet connectivity to 8.8.8.8 works.
- The domain kali.org resolves and responds to ping.
- All three ping tests completed with 0% packet loss.
- The shared Windows Downloads folder is accessible inside Kali.
- A snapshot was created as a recovery point.

### Troubleshooting

Initially, Kali could not reach the virtual gateway and returned “Destination Host Unreachable.”

After checking the VirtualBox network attachment and reconnecting Kali’s wired connection, I repeated the tests. The gateway, internet connectivity and domain name resolution tests then passed.

### What I Learned

- The difference between a virtual machine and the host computer.
- How to configure a NAT Network and a static IPv4 address.
- The roles of an IP address, subnet mask, gateway and DNS server.
- How to use `ip -4 addr`, `ip route` and `ping` to check connectivity.
- How shared folders connect the host and guest systems.
- How snapshots provide a recovery point before further practical work.

## Responsible Practice

My cybersecurity exercises are limited to my own lab and systems where I have explicit permission to test.

## Author

**Alhaji Sedek Sawaneh**
