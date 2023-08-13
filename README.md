
<h1>Firewalls & Protocols</h1>
This project is a tutorial on analyzing different types network traffic using Wireshark. We will also familiarize ourselves with Network Security Groups (NSGs). <br />


<h2>How to:</h2>


<p>
Inspect Network Traffic </p>
<p>
Use Network Security Groups </p>



<h2>Technologies Used</h2>

- Command-Line Tools
- Network Protocols
- Wireshark

<h2>OS Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>Stages</h2>

- Stage 1: Wireshark
- Stage 2: ICMP
- Stage 3: NSG
- Stage 4: Traffic

<h2>Steps</h2>

<p>
<h2>Stage 1: Wireshark</h2>

Step 1: In your VM, download Wireshark using your default browser.

Step 2: Once downloaded, open Wireshark using the start menu.

![](media/STEP%202%20-%20OPEN%20WIRESHARK.png)

Step 3: When selecting a capture filter, choose Ethernet; then click the blue fin at the top left beneath the File button.

![](media/STEP%203%20-%20BEGIN%20CAPTURE.png)

</p>
<br />


<p>
<h2>Stage 2: ICMP</h2>

Step 4: Filter for ICMP traffic

Step 5: With the private IP address of your Linux VM, use PowerShell to ping that machine from your Windows VM.

Step 6: Observe ping requests/replies in Wireshark

</p>
<br />


<p>
<h2>Stage 3: NSG</h2>

Step 7: Initiate an endless ping from your Windows VM to your Linux VM

Step 8: Open Network Security Group on your Ubuntu VM and disable inbound ICMP traffic

Step 9: Use Wireshark to view observe the incoming ICMP traffic be denied.
</p>
<br />

<p>
<h2>Stage 4: Traffic</h2>

Step 10: SSH - In Wireshark, filter for SSH traffic; SSH into your Linux VM using it’s private IP address. Send commands to this machine and observe from back in Wireshark.

Step 11: DHCP - In Wireshark, filter for DHCP traffic; on your Windows VM, type ipconfig /renew in the command line to issue yourself a new IP address. Observe the traffic back in Wireshark

Step 12: DNS - In Wireshark, filter for DNS traffic; using your Windows VM’s command line, type nslookup to find the IP address for a common domain like reddit or twitter. Observe the traffic back in Wireshark.

Step 13: RDP - In Wireshark, filter for RDP traffic; notice a constant stream of traffic? This is because you’re currently connected via Remote Desktop (RDP)
<br />
