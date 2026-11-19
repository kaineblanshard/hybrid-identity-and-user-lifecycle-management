# Active Directory Users, Groups and File Sharing

## What I wanted to do

After setting up Windows Server and Active Directory, I wanted to get some more practice managing users and groups.

I also wanted to learn how permissions work when different departments need access to their own shared folders.

I carried this out in my home lab using my domain controller, DC01.

## 1. Creating users

I started by adding some users to Active Directory and placing them in the correct departments.

The users I created included:

- Sarah Jones – Sales
- Sergio Aguero – IT

I used PowerShell to create users, choose which OU they belonged in, set passwords and enable their accounts.

## 2. Creating security groups

I then created groups to organise users by department.

The groups included:

- `GG_IT_Support`
- `GG_Finance_Staff`
- `GG_Sales_Staff`

I also created some Domain Local groups to control access to shared folders and other resources.

One example was `DL_Share_Sales_RW`, which would be used to give Sales staff access to the Sales folder.

## 3. Adding users to groups

I added Sarah Jones to `GG_Sales_Staff` and Sergio Aguero to `GG_IT_Support`.

I then added `GG_Sales_Staff` to `DL_Share_Sales_RW`.

This means that instead of giving every Sales user permission to the folder individually, I can manage access through groups.

I also learned the difference between Global groups and Domain Local groups:

- Global groups are used to organise users, such as people working in Sales or IT.
- Domain Local groups are used to give people access to resources, such as shared folders.

## 4. Creating a shared folder

I created a folder on DC01 for the Sales department:

`C:\Shares\Sales`

I then changed its permissions so that the Sales group could make changes to files and folders.

I also kept access for Windows system accounts and administrators.

I learned that Windows has two sets of permissions to consider when sharing a folder:

- Folder permissions, which control what someone can do with the files on the server.
- Sharing permissions, which control access when connecting over the network.

Both need to be set correctly.

## 5. Sharing the folder over the network

I created an SMB share called `Sales`.

This made the folder available over the network using:

`\\DC01\Sales`

I set the sharing permissions so that Domain Admins had full access and the Sales permissions group could make changes.

## 6. Testing access

I created a test file inside the Sales folder called:

`Test-Sales-File.txt`

I then checked the group memberships and permissions to make sure everything was set up as expected.

I used Sarah's account to test access to the shared folder. She was able to open it and see the test file.

I also tried testing access using Sergio's IT account. He was able to see the file during my test, even though he was not listed as a member of the Sales groups.

I wasn't able to confirm why this happened, so I haven't treated the test as a successful permissions check. This is something I can come back to and investigate.

## What I learned

This was my first time doing this much work with PowerShell, so it was a lot of figuring out errors.

I learned how to create users and groups, add users to groups, set folder permissions and create a shared folder.

I also have a better understanding of how Active Directory groups can be used to control access rather than giving permissions to individual users.

I still need more practice with PowerShell, especially understanding commands and being able to write them without relying on instructions.

I'll continue building on this lab by learning more about Group Policy, DNS, DHCP and Windows client management.
