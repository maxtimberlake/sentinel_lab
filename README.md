<h1>Failed RDP to IP Geolocation Information</h1>

<h2>Description</h2>
This project dives into cybersecurity by testing a virtual machine on Microsoft Azure. I intentionally turned off its protective firewall to see how it handles potential attacks. Using PowerShell and an IP Geolocator service, I tracked and mapped the data. I kept an eye on things with Azure Sentinel and used a special workbook to visualize the attack attempts, revealing a strong interest from someone in Poland. 
<br />


<h2>Languages and Utilities Used</h2>

- <b>KQL</b>
- <b>Powershell</b>

<h2>Environments Used </h2>

- <b>Microsoft Azure Virtual Machine</b>
- <b>Microsoft Azure Sentinel</b>
- <b>Microsoft Azure </b>
- <b>Windows 10 </b>
  


<h2>Project Start:</h2>


<p align="center">
Validating the Proof of Concept and testing the IP Geolocator service, a complimentary API with a daily allowance of up to 1000 requests.
<br />
<br/>
<img src="https://imgur.com/ucdVr8X.png" height="80%" width="80%" alt="SQL_Lab"/>
<br />
<br />

<p align="center">
Established a virtual machine on Microsoft Azure and intentionally exposed it to potential attackers by fully disabling the firewall for testing purposes. This picture showcases that the virtual machine was secure before we begin. 
<br />
<br /> 
<img src="https://imgur.com/fYiAQVN.png" height="80%" width="80%" alt="SQL"/>
<br />
<br />

<p align="center">
Established a virtual machine on Microsoft Azure and intentionally exposed it to potential attackers by fully disabling the firewall for testing purposes. (Part 2)
<br />
<br /> 
<img src="https://imgur.com/STRavrm.png" height="80%" width="80%" alt="SQL"/>
<br />
<br />

<p align="center">
Implemented a PowerShell script to relay Event Manager logs to the IP Geolocator service, generating a distinct log named 'failed_rdp.log' with geolocation parameters. This script also incorporated sample logs to facilitate Azure's algorithm training in case of delayed attacks. Linked this newly created log within Azure, establishing it as the primary data source for the map.:
<br />
<br /> 
<img src="https://imgur.com/bfw9124.png" height="80%" width="80%" alt="SQL"/>
<br />
<br />

<p align="center">
Utilized a Kusto Query Language (KQL) script within Azure to extract and effectively map the data sourced from the logs for later use (Before Running Script) <br/>
<br />
<br />
<img src="https://imgur.com/zB0lxxP.png" height="80%" width="80%" alt="SQL"/>
<br/>
<br/>

<p align="center">
Utilized a Kusto Query Language (KQL) script within Azure to extract and effectively map the data sourced from the logs for later use (After Running Script)
<br />
<br/>
<img src="https://imgur.com/W3t8Unk.png" height="80%" width="80%" alt="SQL_Lab"/>
<br />
<br />

<p align="center">
Enabled Azure Sentinel to ensure continuous monitoring of incoming new entries from "failed_rdp.log"
<br />
<br /> 
<img src="https://imgur.com/OIg8eXo.png" height="80%" width="80%" alt="SQL"/>
<br />
<br />

<p align="center">
Created a new workbook within Azure, serving as the foundation for the map. Employed the identical code used for data extraction as parameters for the map. Activating the map was straightforward, involving a simple adjustment in the workbook's visualization to 'map' and configuring it with the parameters recently established:
<br />
<br /> 
<img src="https://imgur.com/pL2qQIG.png" height="80%" width="80%" alt="SQL"/>
<br />
<br />

<p align="center">
After leaving the virtual machine running for approximately 5-6 hours, this intriguing activity surfaced. It appears someone from Poland is quite determined to gain access – quite the persistence!:<br/>
<br />
<br />
<img src="https://imgur.com/0XiGqes.png" height="80%" width="80%" alt="SQL"/>
<br/>
<br/>
<br />
<br />
<br />


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

