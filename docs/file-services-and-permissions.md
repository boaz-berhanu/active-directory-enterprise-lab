## Creation of Shared Folders and Permissions

I created another VM running Windows Server 2025 Standard Desktop Experience and named it `SRV01` to be used as a file server for departments to store and access documents and media. `SRV01` exists separately from `DC01` so that traffic can be split up between the two machines and to avoid having a single point of failure. `SRV01` points to `DC01` for DNS so that AD tools can be used on SRV01 and so that the files on `SRV01` can be accessed by the users and groups stored on `DC01`. 

I made a folder on `SRV01` at `C:\Shares`, and 3 more within `Shares` named `HR`, `Finance`, and `Public`. The three were each shared by going to the `Properties --> Sharing --> Advanced Sharing --> Check Share this Folder`. Then their UNC (Universal Naming Convention) was `\\SRV01\[Name of Folder]`, (ex: `\\SRV01\HR`). I then edited the NTFS permissions of each folder by going to the `Security tab --> Edit --> Add --> \[Name of Group to be added]`, (ex: `GG_HR`). I assigned permissions to groups rather than individual users because it is faster and more efficient than going through and adding permissions one by one. 

After adding the permissions, I tested access by logging in as an HR user, and typing `\\SRV01\HR` in the File Explorer address bar, and it worked. I able to access the Public Folder at `\\SRV01\Public` because I set the permissions to `ADLAB\Users` for it, and was denied access for Finance folder. The same test was conducted using a Finance user account.

