<h1>Virtual Network Peering</h1>

<h2>Description</h2>
This lab will show how Azure Virtual Network Peering works.<br/><br />

Azure Virtual Network Peering is a networking feature in Microsoft Azure that allows you to connect virtual networks seamlessly. When you have multiple virtual networks in Azure, they may need to communicate with each other. Virtual Network Peering enables this communication by allowing traffic to flow securely between the peered virtual networks.
<br/><br/>
Here's how it works:
<br/><br/>
<b>Direct Communication:</b> Once virtual networks are peered, resources within them can communicate with each other directly using private IP addresses, just as if they were in the same network.<br/>
<b>Transitive Routing:</b> Peering connections can be established across different Azure regions, enabling transitive routing. This means that if Virtual Network A is peered with Virtual Network B and Virtual Network B is peered with Virtual Network C, then resources in Virtual Network A can communicate with resources in Virtual Network C through Virtual Network B.<br/>
<b>Network Isolation:</b> Despite the direct communication between peered virtual networks, they remain isolated from each other from a security standpoint. Network security groups and other network security features can still be applied to control traffic between them.<br/>
<b>Cost-effective:</b> Since Azure Virtual Network Peering operates within the Azure backbone network, there is no need for a VPN gateway or a public IP address, making it a cost-effective solution for connecting virtual networks.<br/><br/>

Overall, Azure Virtual Network Peering simplifies network architecture and enhances connectivity between resources deployed in different virtual networks within Azure.
<br/><br/>

<h2>Environments Used </h2>

- <b>Packet Tracer</b>

<h2>Lab walk-through:</h2>

<p align="center">
<h4>Lab Topology:</h4>
In this Lab there are 2 virtual machines. The 2 virtual machines are on diffent virtual networks and they cannot communicate.<br/>
VM1 has IIS installed and no public IP address.<br/>
VM2 will be used to reach VM1's IIS server on its private address.
<br/>
<img src="https://i.imgur.com/9y9iFZd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/S672qdB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/D2neFpq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<h4> Before Virtual Network peering:</h4>
VM2 cannot reach the IIS server on VM1.<br />
<img src="https://i.imgur.com/TJwpoEX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br/>
<br />

<h4>Virtal Network Peering Configuration:</h4> 
<img src="https://i.imgur.com/vwMyJ2Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br/>
<br />

<h4>After Virtual Network Peering:</h4> 
VM2 can reach the IIS server on VM1.<br />
<img src="https://i.imgur.com/U7QbkdL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><br/>
<br />

