# KC7 Cybersecurity Investigation: Solving the HopsNStuff Breach

## Overview

In the **KC7 Case**, I investigated a sophisticated cyber attack on **HopsNStuff**, a brewery known for its secret ginger beer recipe. The attackers attempted to steal proprietary data, including the coveted ginger beer formula, using a variety of tactics. By diving deep into multiple data sources—including email traffic, server logs, and network activity—I was able to uncover the full extent of the attack and identify key steps to mitigate future threats.

## Objectives

Throughout this investigation, my primary goals were:
- To use Azure Data Explorer and various datasets to analyze the attack.
- To track the activities of the attackers across email, web traffic, and server logs.
- To apply investigative techniques to understand the tactics, techniques, and procedures (TTPs) of Advanced Persistent Threats (APTs).
- To leverage third-party data to discover the attackers’ identities and infrastructure.
- To develop actionable recommendations for HopsNStuff to protect themselves.

## Key Findings

### 1. Suspicious Files and Processes
   - **Dev-Requirements.zip**: This file was opened by several employees and was likely part of the initial malicious payload. The attackers used PowerShell to bypass execution policies and install malicious software, including Python and Chocolatey.
   - **RabbitMQ.exe**: A legitimate application commonly used for messaging services, it was hijacked by the attackers to run malicious payloads under suspicious processes, such as 7zip.exe.
   - **Mimikatz**: The use of Mimikatz for credential dumping was a critical finding. This tool is commonly used in credential harvesting, allowing the attackers to move laterally within the network.

### 2. Potential Watering Hole Attack
   - I found evidence suggesting a **watering hole attack**, where attackers compromised a frequently visited site, likely HopsNStuff’s own website, to infect employees. Files like **Ginger_beer_secret_recipe.pdf** and **Brewery_layout.pdf** were planted on multiple hosts. These files were part of the attack's phishing component, luring victims to open them.
   - The creation of these files and their exfiltration through 50 suspicious outbound connections indicated that they were used not just for infection, but also to facilitate data theft.

### 3. External IP Addresses and Exfiltration
   - Upon reviewing logs, I discovered suspicious login attempts from multiple external IPs across different countries (South America, Asia), signaling an **APT attack**. These attackers were using compromised credentials to move within the network.
   - **Rclone.exe**, a well-known data exfiltration tool, was identified as being used to steal data. The exfiltrated files were likely sensitive, including the ginger beer recipe, based on connections to a suspicious domain, `moneybags.biz`.

## Investigation Steps

1. **Identifying Affected Systems**:  
   I began by identifying the systems associated with the malicious file **Dev-Requirements.zip** and the Mimikatz activity. These systems were cross-referenced with IP addresses linked to the attack.

2. **Tracing Network Activity**:  
   Next, I traced the network activity, especially the 50 outbound connections linked to the suspicious files. I examined DNS logs, focusing on domains associated with exfiltration efforts, like `moneybags.biz`.

3. **Checking for Backdoors**:  
   I found evidence of the **HIGHNOON** backdoor during an analysis of TeamViewer sessions initiated by the attackers. Additionally, I searched for traces of deleted files that could provide further insight into the attack.

4. **Securing Compromised Systems**:  
   After identifying the compromised systems, I recommended isolating them from the network to contain the attack. I also advised resetting user credentials, particularly those involved in opening the malicious attachments.

5. **Forensics on Affected Hosts**:  
   Files like **Ginger_beer_secret_recipe.pdf** were thoroughly forensically examined. I cross-checked the external IPs involved with the logs to trace the source and methods of exfiltration.

## Recommendations for HopsNStuff

Based on my findings, I provided the following recommendations to help HopsNStuff strengthen their security posture:

1. **Network Segmentation**:  
   Implement stricter segmentation of the network to prevent lateral movement and limit access to sensitive files based on user roles.

2. **Email & Web Filtering**:  
   Tighten email filtering and use sandboxing or attachment scanning to prevent phishing emails from reaching employees. Proper web filtering can block access to known malicious sites.

3. **Credential Management**:  
   Enforce multi-factor authentication (MFA) across all systems and establish a policy for regular credential rotation to mitigate credential harvesting threats.

4. **Endpoint Detection & Response (EDR)**:  
   Enhance endpoint monitoring by implementing or improving EDR tools. This will allow for real-time detection of suspicious processes, file changes, and unusual network activity on endpoints.

## Conclusion

This investigation revealed a multi-layered attack on HopsNStuff, with the attackers utilizing various tactics such as phishing, credential harvesting, and data exfiltration. By following the recommended security measures, the company can better defend against future intrusions and safeguard its valuable intellectual property, including the ginger beer recipe.

For more information on cybersecurity investigations or to stay updated with future case studies, check out this repository.

---

**Contact Information**:  
For inquiries or additional resources, feel free to reach out to me at [email address] or visit my [professional website](link to your website).
