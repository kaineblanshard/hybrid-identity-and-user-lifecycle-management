
# 01 - Infrastructure Deployment

## 1. Overview

The foundation of this project is a self-hosted virtual
infrastructure environment.

A physical HP ProLiant server running TrueNAS was used
to provision and host a virtual machine running
Windows Server 2022.

This virtual machine will act as the foundation for
the Active Directory Domain Services deployment.

## 2. Physical Infrastructure

| Component | Details |
|---|---|
| Physical Server | HP ProLiant |
| Virtualisation Platform | TrueNAS |
| Workload | Windows Server 2022 |
| Purpose | Active Directory infrastructure |


## 3. Virtual Machine Configuration

A virtual machine was provisioned within TrueNAS
to host Windows Server 2022.

The following resources were allocated:

| Resource | Allocation |
|---|---|
| VM Name | DC01 |
| Operating System | Windows Server 2022 |
| CPU | 2 Cores |
| RAM | 6 GB |
| Storage | 80 GB |
| Hypervisor | TrueNAS |

### Resource Allocation Rationale

The virtual machine was allocated 2 CPU cores,
6 GB RAM and 80 GB storage to provide resources
for the Windows Server operating system and
Active Directory Domain Services lab environment.

The configuration provides a foundation for
testing domain services, DNS, Group Policy
and user lifecycle management.


## 4. Deployment Process

The following steps were completed:

1. Accessed the TrueNAS management interface.
2. Navigated to Virtual Machines.
3. Created a new virtual machine.
4. Configured CPU, memory and storage resources.
5. Attached Windows Server 2022 installation media.
6. Configured the virtual machine boot process.
7. Installed Windows Server 2022.
8. Accessed the installed operating system through
   the virtual machine console.

## 5. Evidence

### TrueNAS Virtual Machine Configuration

![TrueNAS VM Configuration](../screenshots/truenas-vm-configuration.png)

## 6. Outcome

A Windows Server 2022 virtual machine was successfully
provisioned and installed on the TrueNAS host.

This provides the infrastructure foundation for the
next stage: configuring networking and deploying
Active Directory Domain Services.
