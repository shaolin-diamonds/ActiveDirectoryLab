<h1>Active Directory Lab</h1>

<h2>Description</h2> Created an Active Directory lab using Virtualbox. Configuring this lab to helped understand how Active Directory worked and Windows networking in general. <br />

<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b>

<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
- <b>Windows 10</b>

<h2>Program walk-through:</h2>

<h3><a href="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/main/VM.md" target="_blank">1. Virtualbox Network Set up</a></h3>
<h3><a href="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/main/ADLab.md" target="_blank">2. Active Directory Tutorial</a></h3>
<h3><a href="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/main/PS_Script.md" target="_blank">3. Powershell Script to create users</a></h3>
<h3>4. Connect to Client Computer</h3>

<hr>

<h3>4. Connect to Client Computer</h3>

<p align="center">
After creating Windows 10 VM, go to command line and use 'ipconfig' to see internet settings:<br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/17cd30d6dfdd20db9766b301b9333decce9f4f32/ActiveDirectory/046_client.png" height="50%" width="50%" alt="Active Directory Steps"/>  
<br /> 
<br /> 
Ping a website to check IP address. Since Google.com resolved that means DNS server is working and because can ping to internet means the whole infrastucure is working: <br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/17cd30d6dfdd20db9766b301b9333decce9f4f32/ActiveDirectory/047_client.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br /> 
We can ping mydomain.com, which is domain controller, and it responds: <br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/17cd30d6dfdd20db9766b301b9333decce9f4f32/ActiveDirectory/048_client.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br /> 
Under System, go to Rename PC (advanced): <br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/17cd30d6dfdd20db9766b301b9333decce9f4f32/ActiveDirectory/049_client.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br /> 
With this, we can join the domain at the same time as renaming the PC:<br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/17cd30d6dfdd20db9766b301b9333decce9f4f32/ActiveDirectory/050_client.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
Use one of the users created with the PS script:<br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/17cd30d6dfdd20db9766b301b9333decce9f4f32/ActiveDirectory/051_client.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/17cd30d6dfdd20db9766b301b9333decce9f4f32/ActiveDirectory/052_client.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
When the client gets address it will show up under leases:<br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/17cd30d6dfdd20db9766b301b9333decce9f4f32/ActiveDirectory/053_client.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
Under Active Directory Users and Computers, client computer will also show up as a member of the domain. If removed, created user accounts will not be able to log in: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/17cd30d6dfdd20db9766b301b9333decce9f4f32/ActiveDirectory/054_client.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
Sign into the client using one of the user accounts created: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/17cd30d6dfdd20db9766b301b9333decce9f4f32/ActiveDirectory/055_client.png" height="50%" width="50%" alt="Active Directory Steps"/> 
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
