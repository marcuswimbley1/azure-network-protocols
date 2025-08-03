<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
<p>In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups.</p>

<h2>Environments and Technologies Used</h2>

- <b>Microsoft Azure (Virtual Machines/Compute)</b>
- <b>Remote Desktop</b>
- <b>Various Command-Line Tools</b>
- <b>Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)</b>
- <b>Wireshark (Protocol Analyzer)</b>

<h2>Environments Used </h2>

- <b>Windows 10 (22H2)</b>
- <b>Ubuntu Server 22.04</b>

<h2>High-level Steps Taken</h2>

- <b>Created two virtual machines in the same virtual network</b>
- <b>Set up a Network Security Group (NSG) to control traffic</b>
- <b>Added inbound and outbound rules in the NSG</b>
- <b>Attached the NSG to a virtual machine</b>

<h2>Actions and Oberservations</h2>
<h2>NSG Overview</h2>

Step 1 - Two virtual machines were created in Azure and placed in the same virtual network to allow communication between them.
<h2>Assigning the NSG to the VM</h2>

Step 2 -This shows the Network Security Group attached to the VM's network interface, where traffic rules are applied.
<h2>Creating a Deny ICMP Rule</h2>

Step 3 -A custom inbound rule was created to block ICMP traffic. The rule uses protocol-specific filtering and a high priority to override default allow rules.
<h2>Ping Test</h2>

Step 4 - A ping test was performed after applying a custom Deny-ICMP rule in the Network Security Group. The request was blocked, confirming that the security rule is working as intended.
