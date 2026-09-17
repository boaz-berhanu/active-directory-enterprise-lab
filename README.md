# Active Directory Enterprise Lab

A virtualized Windows enterprise lab built with Windows Server 2025, Windows 11 Enterprise, and VMware Workstation Pro. The environment simulates a small business network using Active Directory Domain Services, DNS, Group Policy, security groups, and centralized file services.

## Environment

| System | Operating System | Role |
|---|---|---|
| `DC01` | Windows Server 2025 | Domain Controller, AD DS, DNS |
| `SRV01` | Windows Server 2025 | File Server |
| `WIN11-01` | Windows 11 Enterprise | Domain-joined workstation |

**Domain:** `adlab.test`  
**Virtual Network:** `10.10.10.0/24`

## What I Implemented

- Created the `adlab.test` Active Directory domain
- Configured `DC01` as a domain controller and DNS server
- Created organizational units for users, computers, administrators, and departments
- Created domain users and global security groups
- Used separate standard and administrative accounts
- Joined a Windows 11 workstation to the domain
- Configured Group Policy for workstation security and department-specific restrictions
- Created `SRV01` as a separate domain-joined file server
- Created departmental network shares
- Configured NTFS permissions using Active Directory security groups
- Verified authorized and unauthorized access to departmental resources

## Network Design

| Device | IP Address |
|---|---|
| VMware Host Adapter | `10.10.10.1` |
| VMware NAT Gateway | `10.10.10.2` |
| `DC01` | `10.10.10.10` |
| `SRV01` | `10.10.10.20` |
| `WIN11-01` | `10.10.10.50` |

## Documentation

- [Architecture](docs/architecture.md)
- [Active Directory and DNS](docs/active-directory-and-dns.md)
- [Users, Groups, and OUs](docs/users-groups-and-ous.md)
- [Domain-Joined Workstation](docs/domain-joined-workstation.md)
- [Group Policy](docs/group-policy.md)
- [File Services and Permissions](docs/file-services-and-permissions.md)

## Skills Practiced

- Active Directory Domain Services
- DNS
- Windows Server administration
- Windows domain authentication
- Organizational Units
- Active Directory users and security groups
- Group Policy
- NTFS and share permissions
- Windows file sharing
- VMware Workstation Pro
- PowerShell verification and troubleshooting

## Next Steps

- Configure Windows Server DHCP
- Add a secondary domain controller for redundancy
- Configure Windows LAPS
- Automate user administration with PowerShell
- Perform and document additional troubleshooting scenarios