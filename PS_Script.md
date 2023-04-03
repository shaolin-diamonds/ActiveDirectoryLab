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
<h3>3. Powershell Script to create users</h3>
<h3><a href="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/main/VM.md" target="_blank">4. Connect to Client Computer</a></h3>

<hr>

<h3>3. Powershell Script to create users</h3>

<p align="center">
Use name generator to create 1,000 names and put into a plaintext file:<br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/f215b8276f1ec80e47fa0170f64e2c09ad5803d4/ActiveDirectory/034_PowerShell%20names.png" height="50%" width="50%" alt="Active Directory Steps"/>  
<br /> 
<br /> 
Open PowerShell ISE as administator: <br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/f215b8276f1ec80e47fa0170f64e2c09ad5803d4/ActiveDirectory/035_PowerShell%20ISE.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br /> 
Open the PowerShell script: <br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/f215b8276f1ec80e47fa0170f64e2c09ad5803d4/ActiveDirectory/036_PowerShell%20script.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br /> 
Variables used: <br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/f215b8276f1ec80e47fa0170f64e2c09ad5803d4/ActiveDirectory/037_PowerShell%20script.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br /> 
Converting password variable to more secure object:<br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/f215b8276f1ec80e47fa0170f64e2c09ad5803d4/ActiveDirectory/038_PowerShell%20script.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
This line creates a new Organizational Unit named _USER that unchecks box for accidental deletion:<br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/f215b8276f1ec80e47fa0170f64e2c09ad5803d4/ActiveDirectory/039_PowerShell%20script.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
Foreach loop, that creates user account into the _USER OU for each line in the name.txt:<br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/f215b8276f1ec80e47fa0170f64e2c09ad5803d4/ActiveDirectory/040_PowerShell%20script.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
Change Directory to where the script and plaintext file is before running:<br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/f215b8276f1ec80e47fa0170f64e2c09ad5803d4/ActiveDirectory/041_PowerShell%20change%20directory.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
Hit run and it starts creating the users: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/f215b8276f1ec80e47fa0170f64e2c09ad5803d4/ActiveDirectory/042_PowerShell%20run.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
Go back to Active Directory, Users and Computers, and find one of the users: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/f215b8276f1ec80e47fa0170f64e2c09ad5803d4/ActiveDirectory/043_AD%20run.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/f215b8276f1ec80e47fa0170f64e2c09ad5803d4/ActiveDirectory/044_AD%20find.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
Also can see the users under the _USERS OU: <br/>
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/f215b8276f1ec80e47fa0170f64e2c09ad5803d4/ActiveDirectory/045_AD%20users.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
<h3><a href="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/main/VM.md" target="_blank">4. Connect to Client Computer</a></h3>
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
