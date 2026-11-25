# 01 - Setting Up the Server

## 1. What I wanted to do

The first step of this project was getting a Windows Server machine set up so I could start learning and practising Active Directory.

I used an HP ProLiant server running TrueNAS to create a virtual machine for Windows Server 2022.

This server would eventually be used to manage users, computers, groups and practice some networking

## 2. The equipment and setup

I used:

- HP ProLiant physical server.
- TrueNAS to manage the virtual machines.
- Windows Server 2022 as the operating system.
- A virtual machine I named called DC01.

I gave the virtual machine:

- 2 CPU cores.
- 6GB RAM.
- 80GB storage.

These resources were enough to get Windows Server running (Physical PC has 32gb so I had to allocate accordingly as i will likely set up more VM at some point)

## 3. What I did

I completed the following:

1. Logged into the TrueNAS interface.
2. Went to the Virtual Machines section.
3. Created a new virtual machine.
4. Set the name to DC01.
5. Allocated the memory, CPU and storage.
6. Uploaded and selected the Windows Server 2022 installation file.
7. Started the virtual machine and installed Windows Server.
8. Accessed Windows Server through the TrueNAS console.

  ## 4. Setting up the network in TrueNAS

One of the things I needed to work out was how to keep the lab network separate from my normal home network, as this kept disconnecting all the other devices on the network.

TrueNAS was already using one of the server's network ports for its normal connection so I didn't want to change this.

I created a separate network bridge in TrueNAS called br1 and didnt assign any IP address to it for the lab.

The idea was to keep the existing network connection available for normal access to TrueNAS, while using the new bridge for the Active Directory lab.

I then connected the DC01 virtual machine to this new bridge rather than the normal network bridge.

This worked as after running the machine on an isolated network there was no more issues with other devices using the same network in the house

At this stage, the lab was isolated and didn't have internet access, so I wanted to set up Active Directory before worrying about syncing it to Entra. 

## 5. Evidence

I saved a screenshot of the virtual machine setup to show how DC01 was configured.

![TrueNAS VM Configuration](../screenshots/truenas-vm-configuration.png)

## 6. My position after this

I created and installed my Windows Server 2022 virtual machine.

This gave me a working server to use for the rest of the project.
