# My First Virtual Networking Lab | Networkwalks Internship

This is one of the first practical things I worked on during my cybersecurity internship with **Networkwalks IT Solutions & Training**, with our instructor **Waqas Karim**.

For this task, I used **Oracle VirtualBox** to set up a small virtual network between **Kali Linux** and **Windows**. I wanted to understand how two computers can communicate even when both of them are running on the same laptop.

## What I used

- Oracle VirtualBox
- Kali Linux
- Windows virtual machine
- NAT Network

## 1. Setting up the NAT Network

First, I created a NAT Network in VirtualBox and named it `NatNetwork`. I used the network `10.0.0.0/24` and enabled DHCP in the network settings.

This gave my virtual machines a network they could both connect to. I configured the machine IP addresses manually for the lab.

![VirtualBox NAT Network settings](images/01-nat-network.png)

## 2. Giving Kali Linux an IP address

Next, I opened Kali Linux's wired network settings and set the IPv4 method to **Manual**.

I used these settings:

- IP address: `10.0.0.2`
- Network prefix: `24`
- Gateway: `10.0.0.1`

This is the address of my Kali Linux machine inside our virtual network.

![Kali Linux IPv4 settings](images/02-kali-linux-ip.png)

## 3. Giving Windows an IP address

After that, I configured the Windows virtual machine with a different IP address so both computers would have their own addresses on the same network.

- IP address: `10.0.0.11`
- Subnet mask: `255.255.255.0`
- Default gateway: `10.0.0.1`
- Preferred DNS: `8.8.8.8`

![Windows IPv4 settings](images/03-windows-ip.png)

## Result

After setting up the network and fixing some connection issues, **I successfully pinged both virtual machines from each other**. It was good to finally see them communicating using the IP addresses I assigned.

## What I learned

This task helped me understand how to create a virtual network, assign IP addresses, use a subnet mask and gateway, and connect two different operating systems on the same laptop. I also learned that sometimes a network doesn't work the first time, and troubleshooting is part of learning.

Thanks to **Networkwalks IT Solutions & Training** and our instructor **Waqas Karim** for the guidance.

*This is my own practice lab documentation. The three pictures above are from my setup.*
