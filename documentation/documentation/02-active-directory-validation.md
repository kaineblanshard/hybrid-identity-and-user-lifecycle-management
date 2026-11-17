
# 02 - Active Directory Deployment & Validation

## 1. Overview

Active Directory Domain Services (AD DS) was deployed
on the Windows Server 2022 virtual machine hosted
within the TrueNAS environment.

The server was promoted to a domain controller,
establishing the lab.practice Active Directory domain.

## 2. Domain Configuration

| Setting | Value |
|---|---|
| Domain Controller | DC01 |
| Domain Name | lab.practice |
| Operating System | Windows Server 2022 |
| Domain Services | AD DS |
| DNS | Active Directory-integrated DNS |
| IP Address | 10.10.10.10 |
| Network | Isolated virtual bridge |

## 3. Validation

The following PowerShell commands were executed
to validate the Active Directory environment.

### Domain Information

```powershell
Get-ADDomain
```

### Forest Information

```powershell
Get-ADForest
```

### Essential Services

```powershell
Get-Service NTDS,DNS,Netlogon,KDC
```

### Domain Controller Diagnostics

```powershell
dcdiag
```

## 4. Validation Results

All executed validation checks completed successfully.

- Domain information retrieved successfully.
- Forest information retrieved successfully.
- Essential Active Directory services running.
- Domain controller diagnostic checks completed.

## 5. Network Isolation

The virtual machine operates on an isolated
TrueNAS bridge.

This separates the lab environment from the
household network and allows controlled testing
of Active Directory infrastructure.

## 6. Outcome

A functional Active Directory domain controller
has been deployed and validated.

The environment is ready for the next stage:
designing the Active Directory organisational
structure and implementing identity management.
