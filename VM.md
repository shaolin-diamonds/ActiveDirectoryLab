<h1>Active Directory Lab</h1>

<h2>Description</h2> Created an Active Directory lab using Virtualbox. Configuring this lab to helped understand how Active Directory worked and Windows networking in general. <br />

<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b>

<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
- <b>Windows 10</b>

<h2>Program walk-through:</h2>

<h3>1. Virtualbox Network Set up</h3>
<h3><a href="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/main/ADLab.md" target="_blank">2. Active Directory Tutorial</a></h3>
<h3><a href="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/main/VM.md" target="_blank">3. Powershell Script to create users</a></h3>
<h3><a href="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/main/VM.md" target="_blank">4. Connect to Client Computer</a></h3>
<hr>
<p align="center"> 
For the domain controller, we want to have two NICs (Network interface controllers). One to be used by the internet running NAT and then one that's for the internal virtualbox network. Adapter 1 is already attached to NAT, the external internet. Add another Network Adapter for the internal network: <br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/13174afefe14ce89cf3935db7713d742cd2012e1/ActiveDirectory/002_DC%20first%20network%20connection.png" height="50%" width="50%" alt="Active Directory Steps"/>  
<br /> 
<br /> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/13174afefe14ce89cf3935db7713d742cd2012e1/ActiveDirectory/003_DC%20second%20network%20connection.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br /> 
For the Client, set up with internal network: <br/> 
<img src="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/13174afefe14ce89cf3935db7713d742cd2012e1/ActiveDirectory/006_Client%20connect%20to%20internal.png" height="50%" width="50%" alt="Active Directory Steps"/> 
<br /> 
<br />
<h3><a href="https://github.com/shaolin-diamonds/ActiveDirectoryLab/blob/main/ADLab.md" target="_blank">2. Active Directory Tutorial</a></h3>
</p>
