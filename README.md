<h1>Phishing Email Analysis Lab</h1>



<h2>Description</h2>
This project simulates a SOC analyst phishing investigation workflow using a cloud-hosted virtual machine. A controlled Azure environment was deployed to safely analyze real-world phishing email samples sourced from an open-source threat intelligence repository. The goal was to examine email headers, authentication results, sender infrastructure, and common phishing indicators while following SOC best practices.
<br />


<h2>Skills demonstrated</h2>

- <b>Cloud lab deployment (Azure)</b> 
- <b>Secure virtual machine configuration</b>
- <b>Phishing email hadeer analysis</b>
- <b>SPF/DKM/DMARC interpretation</b>
- <b>IOC identification</b>
- <b>Threat Analysis Documentation</b>

<h2>Environments Used </h2>

- <b>Cloud Provider:</b> Microsft Azure
- <b>OS:</b> Windows 11 VM
- <b>Network:</b> Custom Vnet+NSG
- <b> Data Source:</b> Public phishing email samples

<h2>Program walk-through:</h2>

<p align="center">
<br> <b>Step 1: Created a Dedicated Azure Resource Group</b></br>
<br />
<br> Created a dedicated Azure Resource Group to logically isolate all phishing lab resources. This aligns with SOC cloud hygiene and resource management best practices. </br>
<img src="https://imgur.com/4Efszq8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br> <b> Step 2: Deployed a Custom Virtual Network (VNet) </b> <br/>
<br />
<br> Deployed a custom Virtual Network to control network segmentation for the lab environment. </br>
<img src="https://imgur.com/fY6eAKr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br> <b> Step 3: Created and Configured a Windows 11 Virtual Machine </b> <br/>
<br /> 
<br> Provisioned a Windows 11 VM inside the VNet for phishing analysis. </br>
<br> - Assigned public IP for controlled RDP access. </br> 
<br> - Applied Network Security Group (NSG) rules. </br>
<br> - Used Azure availability zone settings. </br>
<img src="https://imgur.com/4rAf2jg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br> <b> Step 4: Idetified a Phishing Dataset From github </b>  <br/>
<br> Located an open-source phishing intelligence repository containing real phishing email samples in .eml format.</br>
<img src="https://imgur.com/0j2Olz6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br> <b> Step 5: Retrieved Phishing Email Samples </b>  <br/>
 <br> Navigated the repository to access individual phishing email samples stored under the /email directory. </br>
<img src="https://imgur.com/4Rgr5lJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br> <b> Step 6: Opened and Analyzed Raw Email Headers </b> <br/>
<br> Opened phishing email samples inside the VM and reviewed raw headers. </br>
<br> <b> Key Artifacts Analyzed: </b> </br>
<br> - From, Return-Path, Reply-To </br>
<br> - Received Chain </br>
<br> - Message-ID </br>
<br> - MIME encoding </br> 
<img src="https://imgur.com/4Rgr5lJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br> <b> Step 7:  Evaluated Email Authentication </b> <br/>
<br> Reviewed authentication results embedded in the headers. </br>
<br> <b> Findings included: </b> </br> 
<br> - SPF results (pass/fail) </br>
<br> - DKIM signatures </br>
<br> - DMARC Alignment issues </br> 
<img src="https://imgur.com/V40EMn8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br> <b> Step 8: Idetified Indicators of Compromise (IOCs) </b> </br>
<br> Extracted and identified suspicious indicators, including:	Suspicious sender domains, Mismatched Reply-To addresses, Unusual mail relay paths, and Generic or deceptive subject lines </br>
<img src="https://imgur.com/YSUXgxO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br> <b> Step 9 (Final): Correlated Findings and Documented Results </b> </br> 
<br> Correlated technical indicators with common phishing tactics such as: Brand impersonation, Financial incentive messaging, and Abuse of legitimate mail infrastructure.
<img src="https://imgur.com/uk4qugT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br> <b> Outcome </b> </br>
<br>This lab successfully demonstrated an end-to-end SOC phishing analysis workflow, from environment setup to IOC identification. The project reflects how phishing investigations are handled in real-world SOC environments using cloud-based sandboxes.

</p>
