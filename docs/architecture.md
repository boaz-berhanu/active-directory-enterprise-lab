\# Active Directory Enterprise Lab Architecture



\## Domain Information



\*\*Domain Name:\*\* `adlab.test`

\*\*NetBIOS Name:\*\* `ADLAB`



\## Virtualization Platform



\* VMware Workstation Pro

\* VMware NAT Network: `VMnet8`



\## Network Configuration



\*\*Network:\*\* `10.10.10.0/24`

\*\*Subnet Mask:\*\* `255.255.255.0`



| Device              | IP Address    | Purpose                              |

| ------------------- | ------------- | ------------------------------------ |

| VMware Host Adapter | `10.10.10.1`  | Host access to virtual network       |

| VMware NAT Gateway  | `10.10.10.2`  | Internet access for virtual machines |

| DC01                | `10.10.10.10` | Primary Domain Controller and DNS    |

| DC02                | `10.10.10.11` | Secondary Domain Controller and DNS  |

| SRV01               | `10.10.10.20` | File Server and DHCP Server          |

| WIN11-01            | DHCP          | Domain-joined Windows 11 workstation |

| WIN11-02            | DHCP          | Domain-joined Windows 11 workstation |



\## DHCP Plan



\*\*DHCP Server:\*\* `SRV01`



\*\*Client Address Pool:\*\*



`10.10.10.100 - 10.10.10.199`



VMware's built-in DHCP service will be disabled so that Windows Server DHCP can be configured and managed as part of the lab.



\## Planned Servers and Workstations



\### DC01



\* Windows Server 2025

\* Primary Domain Controller

\* Active Directory Domain Services

\* DNS



\### DC02



\* Windows Server 2025

\* Additional Domain Controller

\* DNS

\* Provides Active Directory redundancy



\### SRV01



\* Windows Server 2025

\* DHCP Server

\* File Server



\### WIN11-01



\* Windows 11 Enterprise

\* Domain-joined client workstation



\### WIN11-02



\* Windows 11 Enterprise

\* Second domain-joined client workstation



