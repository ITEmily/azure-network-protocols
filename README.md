<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1: Create a Resource Group and then find and click on Virtual Machines
- Step 2: Create a Windows 10 Virtual Machine and then Create a Linux (Ubuntu) Virtual Machine
- Step 3: Use Remote Desktop to connect to the Windows 10 Virtual Machine
- Step 4: Download Wireshark
- Step 5: Filter for ICMP traffic and ping Linux VM from the Window VM
- Step 6: Observe the ping requests and replies within Wireshark
- Step 7: Initiate a non-stop ping from Windows 10 VM to the Linux VM. Then, open the Network Security Group for the Linux VM and disable incoming ICMP trafffic.
- Step 8: "SSH into" your Linux VM and observe SSH traffic in Wireshark.
- Step 9: Observe DHCP Traffic by using ipconfig /renew to issue your Windows 10 VM a new IP address.
- Step 10: Observe DNS traffic by using nslookup for Disney and Google.
- Step 11: Observe RDP traffic by filtering tcp.port==3389 traffic in Wireshark.

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/CmtzSeG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1:  Create a Resource Group and then find and click on Virtual Machines
</p>
<br />

<p>
<img src="https://i.imgur.com/iTShPLl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 2: Create a Windows 10 Virtual Machine and then Create a Linux (Ubuntu) Virtual Machine
</p>
<br />

<p>
<img src="https://i.imgur.com/mOA6hCC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 3: Use Remote Desktop to connect to the Windows 10 Virtual Machine
</p>
<br />

<p>
<img src=https://i.imgur.com/MI2TUW1.png"" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 4: Download Wireshark
</p>
<br />

<p>
<img src="https://i.imgur.com/0oi4o7M.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 5: Filter for ICMP traffic and ping Linux VM from the Window VM
</p>
<br />

<p>
<img src="https://i.imgur.com/rALBH07.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 6: Observe the ping requests and replies within Wireshark. You can also observe the wireshark traffic when pinging public websites such as www.google.com.
</p>
<br />

<p>
<img src="https://i.imgur.com/KflLbk6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 7: Initiate a non-stop ping from Windows 10 VM to the Linux VM. Then, open the Network Security Group for the Linux VM and disable incoming ICMP trafffic. To do this, search for Network Security Group in Azure, click on "Inbound Security Rules" and then click on "+ Add".
</p>
<br />

<p>
<img src="https://i.imgur.com/4PE66zJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Step 8: "SSH into" your Linux VM and observe SSH traffic in Wireshark.
</p>
<br />

<p>
<img src="https://i.imgur.com/w9CxQm6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 9: Observe DHCP Traffic by using ipconfig /renew to issue your Windows 10 VM a new IP address.
</p>
<br />

<p>
<img src="https://i.imgur.com/xqeom8U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 10: Observe DNS traffic by using nslookup for Disney and Google.
</p>
<br />

<p>
<img src="https://i.imgur.com/xDYXR1a.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 11: Observe RDP traffic by filtering tcp.port==3389 traffic in Wireshark.
</p>
<br />
