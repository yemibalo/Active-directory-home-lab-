# Active-directory-home-lab-
Hands-on Windows Server Active Directory lab demonstrating domain controller configuration, user and group management, Organizational Units, Group Policy security, DNS, and Windows 11 domain integration using VirtualBox.
# Active Directory Home Lab – Windows Server

## Project Overview

This project involved building and configuring a Windows Server Active Directory environment in VirtualBox to gain practical experience in identity management, domain administration, and Windows security.

The lab simulates a small business IT environment where users, groups, computers, and security policies are centrally managed.

## Objectives

- Install and configure Active Directory Domain Services (AD DS).
- Create and manage a Windows domain.
- Organise users and resources using Organizational Units (OUs).
- Implement Group Policy Objects (GPOs).
- Configure workstation security policies.
- Join a Windows 11 workstation to the domain.
- Verify DNS resolution and domain controller health.

## Lab Environment

| Component | Configuration |
|---|---|
| Virtualisation | Oracle VirtualBox 7.2.4 |
| Server OS | Windows Server |
| Domain Controller | TECH_DC01 |
| Domain Name | techsolutions.local |
| Domain Controller IP | 192.168.56.10 |
| Client OS | Windows 11 Pro |
| Client Hostname | YEMI |
| Network | Host-only Adapter |

## Technologies Used

- Windows Server
- Active Directory Domain Services (AD DS)
- DNS
- Group Policy Management
- Windows 11
- Oracle VirtualBox

## Implementation

### 1. Active Directory Configuration

Installed and configured Active Directory Domain Services and promoted the Windows Server machine to a domain controller.

Created the domain:

`techsolutions.local`

### 2. Organizational Unit Structure

Created the following Organizational Units to organise the domain environment:

- Departments
- Groups
- Servers
- Workstations

### 3. User and Group Management

Created domain users and groups to demonstrate centralised identity and access management.

### 4. Group Policy Configuration

Created and configured security-related Group Policy Objects:

- GPO_Workstation_Security
- GPO_Domain_Account_Policy
- Default Domain Policy

Verified that the policies were successfully applied to the domain-joined workstation using `gpresult /r`.

### 5. Domain Workstation Integration

Successfully joined the Windows 11 workstation (YEMI) to the `techsolutions.local` domain.

Verified that the workstation appeared in Active Directory Users and Computers.

### 6. DNS and Domain Controller Verification

Performed DNS resolution checks using `nslookup`.

Used the following command to check domain controller health:

`dcdiag /q`

The diagnostic command returned no reported errors.

## Verification Commands

The following commands were used during testing:

**Check domain controller information:**
```cmd
hostname
```

**Verify Group Policy application:**
```cmd
gpresult /r
```

**Refresh Group Policy:**
```cmd
gpupdate /force
```

**Test DNS resolution:**
```cmd
nslookup TECH_DC01.techsolutions.local
```

**Check domain controller health:**
```cmd
dcdiag /q
```

## Project Outcomes

Through this project, I gained practical experience in:

- Windows Server administration.
- Active Directory domain management.
- User and group administration.
- Organizational Unit management.
- Group Policy configuration and verification.
- DNS troubleshooting and resolution.
- Domain workstation integration.
- Basic infrastructure security administration.

## Screenshots

Screenshots documenting the implementation and verification process are available in the project folders.

## Conclusion

This project provided hands-on experience with Microsoft Active Directory and Windows Server administration in a simulated business environment.

It strengthened my understanding of enterprise identity management, access control, Group Policy, and domain infrastructure.

**Tools:** Windows Server | Active Directory | DNS | Group Policy | Windows 11 | VirtualBox
