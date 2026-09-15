## WIN11-01 Workstation Created and Joined to adlab.test Domain

I created a new VM running a copy of Windows 11 Enterprise which will be used to simulate a workstation any employee would use. It uses DC01 for DNS because Active Directory uses DNS records to help clients find domain controllers and AD services.

The workstation needed a manual IP address because I haven't set up a Windows DHCP (Dynamic Host Configuration Protocol) server yet for automatically assigning IP addresses to machines under the adlab.test domain.

Joining the computer to the domain created a computer account/trust relationship and allowed centralized authentication and management. 

I verified that the domain login worked by signing in with one of the employee accounts I created earlier using the UPN `swilson@adlab.test`.