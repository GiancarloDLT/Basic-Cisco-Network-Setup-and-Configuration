<h1>Basic Cisco Network Setup and Configuration</h1>


<h2>Description</h2>
This project is designed to provide a foundational understanding of basic network configuration using Cisco devices. It demonstrates how to set up a simple network with multiple computers, switches, and a router. The goal is to configure devices with appropriate IP addresses, subnets, and default gateways to ensure proper communication between devices across different subnets. The significance of this project lies in its ability to showcase essential networking concepts such as IP addressing, routing, and network connectivity, laying the groundwork for more advanced networking and configuration tasks.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Cisco Packet Tracer</b> 


<h2>Environments Used </h2>

- <b>macOS</b>

<h2>Walk-through:</h2>
<br>
<br>
<p align="left">
<b> This following screenshot demonstrates the initial setup of a basic network configuration. It features four computers divided into two distinct subnets, connected through two switches and one router. This layout forms the foundation for understanding how devices in separate subnets communicate and how traffic is managed between them using a router. The configuration allows for practical exploration of subnetting, routing, and switching concepts.<b/>
  <img src="https://i.imgur.com/NKicltx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br>
<br>


<b> In this step, we connect the network devices. PC0's Fast Ethernet port is linked to Switch 1's Fast Ethernet port 0/1, and PC1's Fast Ethernet port is also connected to Switch 1's Fast Ethernet port 0/1. Similarly, PC2's Fast Ethernet port is connected to Switch 2's Fast Ethernet port 0/1, while PC3’s Fast Ethernet port is connected to Switch 2’s Fast Ethernet port 0/1. Next, Switch 1’s Gigabit Ethernet port is connected to Router's Gigabit Ethernet 0/0 port, and Switch 2’s Gigabit Ethernet port is linked to the Router’s Gigabit Ethernet 0/1 port. This setup ensures the correct physical connections for each device, forming the core of the network topology.<b/> 
<br>
<br>
  <img src="https://i.imgur.com/ExzRcAP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<b> In the previous screenshot, we noticed that the wires connected to the router were highlighted with red errors, indicating that the router was not yet configured. This screenshot shows the configuration process. To start, click on the router and select the CLI (Command Line Interface). When prompted to enter the initial configuration dialog, type "no" to skip it. Once you’re in the CLI, type enable to enter privileged exec mode. Then, type configure terminal to enter global configuration mode. From there, type interface g0/0 to access the router's GigabitEthernet0/0 interface configuration. Assign an IP address with the command ip address 192.168.1.1 255.255.255.0, but keep in mind that you can choose your own network address and subnet as long as you use the appropriate subnet mask for your selected classful or classless network. For example, for a Class C network, a subnet mask of 255.255.255.0 is commonly used, but if you're using a Class A or Class B address, the subnet mask would be different (such as 255.0.0.0 for Class A or 255.255.0.0 for Class B). To activate the interface, type no shutdown. After completing these steps, the interface will come up, and you should see these messages confirming the status. Finally, type exit to return to the previous mode. This indicates that the router's interface is now active and ready to route traffic between the subnets.<b/> 
<br>
<br>
  <img src="https://i.imgur.com/UY4oXyI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br>
<br>
  <img src="https://i.imgur.com/aPy5U8t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<b> Next, we configure the IP addresses for the computers based on their respective subnets. To begin this process, click on PC0, navigate to the "Desktop" tab, and select "IP Configuration." Assign the appropriate IP address to PC0 within the gateway subnet; in this case, the IP address 192.168.1.2 is assigned. For PC1, assign the IP address 192.168.1.3 and configure both PC0 and PC1's default gateways to 192.168.1.1, which corresponds to the router's interface in the 192.168.1.0 subnet.<b/> 
<br>
<br>
  <img src="https://i.imgur.com/xaO4Isq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/GEhLthW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/T8WGnWO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<b> Similarly, for PC2, configure the IP address 192.168.2.2 and assign the default gateway as 192.168.2.1 in the 192.168.2.0 subnet. For PC3, assign the IP address 192.168.2.3 and set the default gateway to 192.168.2.1, following the same subnet as PC2. This ensures that each computer in the network is properly configured with a unique IP address within their respective subnets and that all computers have the correct default gateway to communicate with devices on other subnets..<b/> 
<br>
<br>
  <img src="https://i.imgur.com/0oqSwyY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/qt5ZvOH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<b> At this stage, the network should be fully configured with the proper interfaces and IP addresses. I have included comments detailing the configuration of each interface and IP address, helping to clarify how the devices are set up and ensuring everything is correctly assigned.<b/> 
<br>
<br>
  <img src="https://i.imgur.com/0OWsOhH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<b> At this point, we should have established connectivity between the two computer sets across both network subnets. To verify the network connectivity, click on PC0, go to the "Desktop" tab, and then select "Command Prompt." In the command prompt, try pinging either PC2 or PC3. As demonstrated in the screenshot, the ping is successful, confirming that communication between the two subnets is working as intended..<b/> 
<br>
<br>
  <img src="https://i.imgur.com/tQ35DAM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
