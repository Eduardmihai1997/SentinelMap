<h1>SIEM-Azure Sentinel Map with Live Cyber Attacks</h1>


<h2>Description</h2>
In this lab, I setup Azure Sentinel (SIEM) and connect it to a live virtual machine acting as a honey pot. I did this to observe live attacks (RDP Brute Force) from all around the world. I used a custom PowerShell script to look up the attackers Geolocation information and plot it on the Azure Sentinel Map! 


<h2>Technologies Used</h2>

- <b>Microsoft Azure/Log Analytics Workspace and Sentinel (Mircosoft's SIEM)</b> 
- <b>Powershell</b> 
- <b>Remote desktop protocol</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2> 

- <b>Create a virtual machine in Azure (honeypot-vm) and turning firewalls off ( to make it vulnerable to brute force attacks)</b>
- <b>Create a log repository in Azure (Log Analytics Workspace)</b> 
<img src="https://i.imgur.com/YPa8lor.png" height="80%" width="80%"/>
<br></br>

- <b>Log into VM with Remote Desktop(with 1 log fail)</b>  
- <b>ObserveEvent Viewer Logs for the failed log(4625) in VM</b?
<img src="https://i.imgur.com/tbKw3Zd.png" height="80%" width="80%" />
<br></br>

- <b>Run a configured script(to get Geo Data from attackers)</b>
- <b>Get Geolocation.io API Key</b>
<img src="https://i.imgur.com/EiBr31T.png" height="80%" width="80%" />
 <br></br>

- <b>Create a custom geolocation log in Log Analytics Workspace</b> 
- <b>Secure connection between honeypot-vm and log analytics</b>
<img src="https://i.imgur.com/0Avpw9p.png" height="80%" width="80%" />
<br></br>

- <b> Extract geo-data from the RawData of sample logs</b>
- <b> Extracting more data from the sample log</b>
<img src="https://i.imgur.com/rv69y55.png" height="80%" width="80%" />
<br></br> 

- <b> Set up the map within Microsoft Sentinel<b/>
- <b> Threat visualization</b>
<img src="https://i.imgur.com/tkjkhdp.png" height="80%" width="80%" />
<img src="https://i.imgur.com/lk4peN5.png" height="80%" width="80%" />
<br></br>

