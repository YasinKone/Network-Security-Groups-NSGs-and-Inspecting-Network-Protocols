<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1: Make 2 Azure virtual machines one running windows and the other running ubuntu
- Step 2: connect to your windows VM usisng RDP then download wireshark
- Step 3: open up wire shark and press the blue button in the top left corner to start capturing packets
- Step 4: Experiment with the two VMs now and view the traffic with Wireshark.

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/L3T0lWa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open up VM1 using RDP to login use you VMs public IP address then press more choices then enter the username in and password you made for it. When you finally get in download wireshark
</p>
<br />

<p>
<img src="https://i.imgur.com/Io4PVjI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
open up wire shark and press the blue button in the top left corner to start capturing packets
</p>
<br />

<p>
<img src="https://i.imgur.com/bNVDXXg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Experiment with the two VMs now. Like using the windows VM send ICMP traffic to VM2 then make a wire wall on azure to block ICMP traffic (dont forget to filter it by ICMP traffic), using VM1 ssh into VM2 (dont forget to filter by ssh traffic in wireshark), get a new IP address for VM1 using the command ipconfig /renew (filter wireshark traffic by DHCP), use the nslookup command in powershell on different host names (filter wireshark by dns traffic).
</p>
<br />
