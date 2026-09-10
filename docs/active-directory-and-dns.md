**Setting up Active Directory and DNS**
Installed Active Directory Domain Services on DC01. This will let us create and manage users, groups, permissions, policies, and computers.
DC01 was then promoted to a domain controller and a new forest was created since there isn't any AD environment set up yet.
The root domain name of the forest was set to `adlab.test` which represents the Active Directory domain that all users and computers will belong to.
DC01 is also running DNS which will translate hostnames into IP addresses so computers can locate resources. Domain clients need to use the AD DNS server so they can find resources and services inside the `adlab.test` domain.
A reverse lookup zone was also created so that IP addresses could be translated back into hostnames.
Lastly, I used `nslookup dc01.adlab.test` in PowerShell so that I could verify the DNS resolution was working properly.
!\[Active Directory domain](screenshots/ad-domain-created.png)
DC01 is also running DNS which will translate hostnames into IP addresses so computers can locate resources. Domain clients need to use the AD DNS server so they can find resources and services inside the `adlab.test` domain.
!\[DNS forward lookup zone](screenshots/dns-forward-zone.png)
A reverse lookup zone was also created so that IP addresses could be translated back into hostnames.
Lastly, I used `nslookup dc01.adlab.test` in PowerShell so that I could verify the DNS resolution was working properly.
!\[DNS resolution test](screenshots/dns-resolution-test.png)
