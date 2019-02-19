NOTE: This is currently a work in progress.

# Arch System Setup

This is documentation around my preferred setup of Arch Linux. This is some documentation I decided to start early in my exploration into Arch Linux. My background consists mainly of Redhat/Fedora so I tend to lean toward some of the tools that are in use with those distributions.


### Table of Contents

1. Basic Setup
    1. Network Conncetivity
    2. Partitioning and Mounting
    3. Initializing Arch
    4. Localization and Setup
    5. Bootloader Configuraiton (GRUB)
    
2. First Boot Setup
    1. Network Setup

## 1. Basic Setup

### 1i. Network Connectivity

#### Using DHCP

One of the easiest ways to start with the setup process is to connect the system to a network that provides DHCP and run:

```bash
dhcpcd
```

The system will grab an IP Address and will print out the address that it obtained. Once the system obtains an IP, you can check internet connectivity using:

```bash
ping www.google.com
```

If you run into trouble above, the following command can help you troubleshoot:

```bash
# Check to ensure that the interface that you are working with is up
ip link
# Check to ensure that you have a valid IP address on the expected network
ip addr
# Check to ensure that you have a valid route to the internet
ip route show
# Check to see if you can reach the internet via your default gateway
ping 8.8.8.8
# Check to see if DNS resolution is functional
drill www.google.com
```

We'll start with the basic repeatable setup. Slight variation in Partition structure depending on usage.


## 2. First Boot Setup

### 2.1. Network Setup

NOTE: If you followed the installation instructions above, all required packages to complete these settings as I prefer should be installed and the system should not require internet access. If you did not, please ensure that the `ifplugd` package is installed as this is what I use to start the static interfaces.

1. Locate your interface

```bash
ip link
```

2. 



### A Note about VM's

I tend to run VM's a bit on the large side and do thin provisioning on whatever platform I'm working with. I like to start at 40GB and work up or down depending on need. That being said, once an application is specialized and into "production" _(Aka. When my wife will complain if it's down)_ I tend to take a maintenance window (read: "Internet is down honey!") and move the application over to a more streamlined VM. That is, until I get it all into containers.

## Sources

I took lots of content and guidance from the [Arch Wiki](https://wiki.archlinux.org/). I would recommend bookmarking this if you haven't already as it is an invaluable reference for the Linux adventures (Not just Arch!).
