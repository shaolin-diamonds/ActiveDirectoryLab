<h1>Active Directory Lab</h1>

<h2>Description</h2> Created an Active Directory lab using Virtualbox. Configuring this lab to helped understand how Active Directory worked and Windows networking in general. <br />

<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b>

<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
- <b>Windows 10</b>

<h2>Program walk-through:</h2>

<h3><a href="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/main/VM.md" target="_blank">1. Virtualbox Network Set up</a></h3>
<h3>2. Active Directory Tutorial</h3>
<h3><a href="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/main/PS_Script.md" target="_blank">3. Powershell Script to create users</a></h3>
<h3><a href="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/main/VM.md" target="_blank">4. Connect to Client Computer</a></h3>

<hr>

<h2 align="center">Active Directory Tutorial</h2>

<p align="center">
On the domain contoller, find both networks and figure out which is external and which is internal: <br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/007_DC%20networks.png" height="50%" width="50%" alt="Active Directory Steps"/>  
<br /> 
<br /> 
Set up the IP address for the internal network: <br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/008_DC%20internal%20IP%20setup.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br /> 
Now, have to install the Active Directory via Server Manager. Under Add Roles and Features: <br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/009_AD_001.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br /> 
After installation, find Active Directory Users and Computers under Windows Admin Tools: <br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/010_AD_domain%20admin%20acct_001.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br /> 
Under mydomain.com, create new Organizational Unit. I named it ADMINS:<br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/011_AD_domain%20admin%20acct_002.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
Add a new user:<br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/012_AD_domain%20admin%20acct_003.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
Make the new user an admin:<br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/013_AD_domain%20admin%20acct_004.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
Add the admin user to the domain admin group:<br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/014_AD_domain%20admin%20acct_005.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
Next step is to install RAS / NAT. To allow client VM to be on this private virtual network, but still be able to access internet through domain controller. Install RAS / NAT through Server Manager under Roles and Features: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/015_RAS%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/016_RAS%20set%20up%202.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/017_RAS%20set%20up%203.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/018_RAS%20set%20up%204.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/019_RAS%20set%20up%205.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/020_RAS%20set%20up%206.png" height="50%" width="50%" alt="Active Directory Steps"/>
<br /> 
<br />
Next step is to set up DHCP server on domain controller to allow our client VM to get IP address and browse the internet, even though they are on private internal network: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/021_DHCP%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/>
<br /> 
<br />
After DHCP installation, need to set up scope that will give IP addresses in this range: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/022_DHCP%20scope%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/>
<br /> 
<br />
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/023_DHCP%20scope%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/>
<br />
<br />
Give scope a name: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/024_DHCP%20scope%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/>
<br />
<br />
Set the range: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/025_DHCP%20scope%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/>
<br />
<br />
Set the exception: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/026_DHCP%20scope%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/>
<br />
<br />
Set the duration: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/027_DHCP%20scope%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/>
<br />
<br />
Configure DHCP options. We want to tell the clients which server to use for DNS and which server to use for the gateway. Want to configure those things because we want them to be able to get on the internet: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/028_DHCP%20scope%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/>
<br />
<br />
Add domain controller's IP Address for router because it has NAT configured: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/029_DHCP%20scope%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/>
<br />
<br />
What do you want to use for the DNS server: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/030_DHCP%20scope%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/>
<br />
<br />
Finish setting up scope: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/031_DHCP%20scope%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/>
<br />
<br />
Authorize and refresh the DHCP server: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/032_DHCP%20scope%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/>
<br />
<br />
We can see the scope: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/00c22e957d92f0a9edea180df7bce52e891e277a/ActiveDirectory/033_DHCP%20scope%20set%20up.png" height="50%" width="50%" alt="Active Directory Steps"/>
<h3><a href="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/main/PS_Script.md" target="_blank">3. Powershell Script to create users</a></h3>
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
