NOTE: This is currently a work in progress.

# Arch System Setup

This is documentation around my preferred setup of Arch Linux. This is some documentation I decided to start early in my exploration into Arch Linux. My background consists mainly of Redhat/Fedora so I tend to lean toward some of the tools that are in use with those distributions.

## Basic Setup

We'll start with the basic repeatable setup. Slight variation in Partition structure depending on usage.

### Table of Contents
1. Partitioning and Mounting
2. Initializing Arch
3. Localization and Setup
4. Bootloader Configuraiton (GRUB)

### A Note about VM's

I tend to run VM's a bit on the large side and do thin provisioning on whatever platform I'm working with. I like to start at 40GB and work up or down depending on need. That being said, once an application is specialized and into "production" _(Aka. When my wife will complain if it's down)_ I tend to take a maintenance window (read: "Internet is down honey!") and move the application over to a more streamlined VM. That is, until I get it all into containers.

## Sources

I took lots of content and guidance from the (Arch Wiki)[https://wiki.archlinux.org/]. I would recommend bookmarking this if you haven't already as it is an invaluable reference for the Linux adventures (Not just Arch!).
