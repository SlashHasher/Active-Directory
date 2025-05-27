<h1> 🖥️ Enterprise Active Directory Deployment with SIEM and Automation (Vultr, Splunk, Slack, Shuffle) </h1>



<h2> 📄 Description</h2>
This project simulates a real-world enterprise Active Directory environment built on cloud infrastructure. It includes the design, deployment, and security hardening of a Windows-based AD domain, along with integration of Splunk for log analysis and Slack + Shuffle for automated incident response. The goal was to gain hands-on experience with identity management, monitoring, and security automation.
<br />


<h2> 🛠  Utilities Used</h2>

- <b> Windows Server 2019 – Domain controller and Active Directory services </b>
- <b> Splunk Enterprise – Log ingestion, monitoring, and alerting</b>
- <b> Shuffle (SOAR platform) – Security orchestration and automated response</b>
- <b> Slack – Alert notifications and workflow integration </b>
- <b> Vultr – Cloud hosting for virtual machines </b>
- <b> Remote Desktop (RDP) – Server access and administration </b>
- <b> Group Policy Management Console (GPMC) – Policy creation and deployment </b>
- <b> PowerShell – AD user and system configuration </b> 


<h2> 🌐 Environments Used</h2>

- <b> Cloud Infrastructure – Deployed all systems on Vultr virtual machines</b>
- <b> Windows Server Environment – Domain controller, DNS, and Active Directory </b>
- <b> Security Lab Environment – Isolated VM network for testing detection, logging, and automation </b>

<h2>Project Documentation & Walkthrough </h2>




<p align="center">
Choose and create VMs <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Customize and Deploy VMs <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Customize the firewall <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Change Firewall Rules <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
RDP into AD VM <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Add firewall rules to AD VM <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Do the same for the other VMs <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enable VPC <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
SSH into the Ubuntu VM <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 SSH successfull <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Add firewall and VPC to Ubuntu instance, which will disconnect us from SSH <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Ran into some trouble with networking <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Fixed Issue and now we can communicate between the VMs <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 We can ping the Ubuntu but cant ping the AD VM, so we have to fix the networking there as well <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Perfect, now all the machines can communicate <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
RDP into the AD machine, and configure AD services <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Creating new forest and promoting to Domain Controller <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Installation <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Signed Out, wait for restart <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
This VM is now the Active Directory Domain Controller <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Creating a new user, Bob Builder <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Now we can add Bob into our AD <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Set up the profile inside the VM <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Unfortunetly, there is an error, time to troubleshoot <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Since there is no DNS server selected, the machine couldnt reach the AD. Fixed by inputting the IP address of Domain Controller <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Testing again after troubleshooting <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
It worked, now this user, Bob, is part of our active directory domain <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Using the Console, we can successfully sign into Bob's accoumt <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Adding Bbob to allow RDP connections, because they were off by default for security <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Trying to RDP into the VM using Bob's account <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Now to install Splunk, we will connect to the Ubuntu VM <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Connect to the machine using SSH, and download Splunk <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Splunk Install is Completed <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
We cant connect to the Splunk Server yet. Time to troubleshoot again. <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Allowed port 8000 on Ubuntu VM <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
That seemed to fix the issue <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 We're Live on Splunk <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Installing apps which we will need later for our Log analysis <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a new Index, which I will title  z-ad <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Add new receiving port, being 9997 <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Download Splunk Forwarder on the test VM which will be the honeypot to generate logs <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Setup the Forwarder and Indexing settings <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Edit input config file and add our index <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Restart the Splunk Forwarding Service <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Check on the Splunk Server for telemetry <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Now we will do the same setup on the AD Controller VM <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Now on our Splunk Dashboard, we can see two hosts, which means out VMs are reporting correctly <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 We can see successfull logons by refining our research <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Changed the search to make it appear more concise and aesthetically pleasing <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Save as an Alert <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Now we are getting alerts on the Triggered Alerts tab <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Now its time to setup Shuffle <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Creating our Workflow <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Add Shuffle Webhook to Splunk Alerts <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 The alerts are now showing on Shuffle <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Setup Slack <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Setup Slack <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure our alerts <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Alerts Working as Inteded <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Adding email feature to notify for alerts <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Verification of Successfull email notifications <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Add Active Directory to Shuffle to allow disabling of accounts with unauthorized access <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Workflow is all Done <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Alerts on Slack working as Intended <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Alerts on Splunk working as Inteded <br/>
<img src="https://i.imgur.com/bE1mmgC.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
<h2> ✅ Conclusion</h2>
This project served as a comprehensive, real-world simulation of deploying and securing an enterprise-grade Active Directory environment in the cloud. From initial architecture planning to implementing automated security workflows, each phase contributed to a deeper understanding of Windows-based identity management, log monitoring, and incident response.

By building the domain from scratch, integrating Splunk for centralized logging, and automating alert handling with Shuffle and Slack, I explored how large-scale organizations manage and secure their infrastructure. The process involved several technical challenges, including domain controller configuration issues, log forwarding misconfigurations, and automation setup problems. Solving these problems helped reinforce key skills in system administration, debugging, and integrating security tools.

I plan to continue building on this lab by adding threat simulations, detection rules, and additional incident response playbooks. These additions will bring the environment even closer to the workflows used in real-world security operations centers.

Thank you for viewing my work 🖤
<br />





































<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
