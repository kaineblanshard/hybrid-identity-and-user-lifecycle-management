# Active Directory - Building My Own Lab

## About This Project

I'm building my own Active Directory environment using Windows Server 2022 so I can get more practical experience with Windows administration and managing users in a business environment.

I want to create a small company-style network where I can practise tasks that would normally be carried out by an IT support or second-line technician.

I'm building it up gradually, starting with the server and Active Directory, then moving on to users, groups, permissions, Group Policy and PowerShell.

I'd also like to connect the environment to Microsoft Entra ID later so I can get some experience with a hybrid setup 

## My Lab Setup

I'm using:

- An HP ProLiant server.
- TrueNAS to run my virtual machines.
- Windows Server 2022.
- A virtual machine called DC01.
- 6GB RAM, 2 CPU cores and 80GB storage.
- A separate network for the lab.

## What I Want to Practise

As the project develops, I want to cover:

- Installing and managing Active Directory.
- Setting up and understanding DNS.
- Creating users and organising them into departments.
- Creating security groups and distribution groups.
- Managing permissions and access.
- Setting up Group Policy.
- Using PowerShell to carry out administration tasks.
- Managing user accounts when staff join, change roles or leave.
- Connecting Active Directory to Microsoft Entra ID.

## User Account Management

One of the main parts of this project will be practising how user accounts are managed throughout their time at a company.

I'll be using the lab to practise:

- **New starters:** Creating accounts, setting passwords and giving users the correct access.
- **Changes to roles:** Moving users between departments and changing their group memberships and permissions.
- **Leavers:** Disabling accounts and removing access when someone leaves the company.

## What I'm Using

- Windows Server 2022
- Active Directory
- DNS
- Group Policy
- PowerShell
- TrueNAS
- Microsoft Entra ID (planned)

## Project Progress

**Status: In Progress**

I've set up the Windows Server virtual machine, installed Active Directory and started building the user and group structure.

I've also set up a separate lab network and installed OPNsense to provide controlled internet access.

There is still plenty to build and test, so I'll keep updating this project as I work through each stage.

## Project Notes

I'll use this repository to keep track of what I've done, any problems I've come across, how I've fixed them and what I've learned along the way.
