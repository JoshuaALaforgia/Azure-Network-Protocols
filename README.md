# Azure-Network-Protocols
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

- Step 1: Connect to VM-1 & VM-2 with Remote Desktop
- Step 2: Install Wireshark on VM-1 to anayalze the incoming traffic 
- Step 3: Capture packets with wireshark and monitor traffic
- Step 4: Filter traffic to only view icmp
- Step 5: Block icmp traffic to VM-2 with Firewall Configurations from VM-1

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/feiEwo0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open Remote desktop and paste the public ip address from VM-1 and click connect.
</p>
<br />

<p>
<img src="https://i.imgur.com/M3Pj8iP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


Once you've entered your username and password that we created, navigate to the edge browser.
</p>
<br />

<p>
<img src="https://i.imgur.com/7UZ5UiW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When you get to the browser, search wireshark download
</p>
<br />

<p>
<img src="https://i.imgur.com/mz8mMBq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once Wireshark is installed, click the ethernet button followed by the blue fin in the top left hand corner
</p>
<br />
<p>
<img src="https://i.imgur.com/FT3E7X8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
These are the packets of data that is being communicated between VM-1 and VM-2
</p>
<br />

<img src="https://i.imgur.com/yUZU9NE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Filter traffic for only icmp traffic
</p>
<br />

<img src="https://i.imgur.com/9HWpUaS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To Block ICMP traffic navigate to NSG or Network Security Group
</p>
<br />

<img src="https://i.imgur.com/3BJmcHj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Then we are going to add an inbound security rule
</p>
<br />

<img src="https://i.imgur.com/ufDlHnj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Deny all icmp traffic with the priority off port 200
</p>
<br />

<img src="https://i.imgur.com/m9GhDz3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
All ICMP Traffic Successfully Stopped.
</p>
<br />
