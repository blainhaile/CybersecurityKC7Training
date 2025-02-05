<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KC7 Cybersecurity Investigation</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <header>
        <h1>KC7 Cybersecurity Investigation: Solving the HopsNStuff Breach</h1>
    </header>

    <section id="overview">
        <h2>Overview</h2>
        <p>In the <strong>KC7 Case</strong>, I investigated a sophisticated cyber attack on <strong>HopsNStuff</strong>, a brewery known for its secret ginger beer recipe. The attackers attempted to steal proprietary data, including the coveted ginger beer formula, using a variety of tactics. By diving deep into multiple data sources—including email traffic, server logs, and network activity—I was able to uncover the full extent of the attack and identify key steps to mitigate future threats.</p>
    </section>

    <section id="objectives">
        <h2>Objectives</h2>
        <ul>
            <li>Use Azure Data Explorer and various datasets to analyze the attack.</li>
            <li>Track the activities of the attackers across email, web traffic, and server logs.</li>
            <li>Apply investigative techniques to understand the tactics, techniques, and procedures (TTPs) of Advanced Persistent Threats (APTs).</li>
            <li>Leverage third-party data to discover the attackers’ identities and infrastructure.</li>
            <li>Develop actionable recommendations for HopsNStuff to protect themselves.</li>
        </ul>
    </section>

    <section id="key-findings">
        <h2>Key Findings</h2>
        <h3>1. Suspicious Files and Processes</h3>
        <ul>
            <li><strong>Dev-Requirements.zip:</strong> This file was opened by several employees and was likely part of the initial malicious payload. The attackers used PowerShell to bypass execution policies and install malicious software, including Python and Chocolatey.</li>
            <li><strong>RabbitMQ.exe:</strong> A legitimate application commonly used for messaging services, it was hijacked by the attackers to run malicious payloads under suspicious processes, such as 7zip.exe.</li>
            <li><strong>Mimikatz:</strong> The use of Mimikatz for credential dumping was a critical finding. This tool is commonly used in credential harvesting, allowing the attackers to move laterally within the network.</li>
        </ul>

        <h3>2. Potential Watering Hole Attack</h3>
        <ul>
            <li>I found evidence suggesting a <strong>watering hole attack</strong>, where attackers compromised a frequently visited site, likely HopsNStuff’s own website, to infect employees. Files like <strong>Ginger_beer_secret_recipe.pdf</strong> and <strong>Brewery_layout.pdf</strong> were planted on multiple hosts. These files were part of the attack's phishing component, luring victims to open them.</li>
            <li>The creation of these files and their exfiltration through 50 suspicious outbound connections indicated that they were used not just for infection, but also to facilitate data theft.</li>
        </ul>

        <h3>3. External IP Addresses and Exfiltration</h3>
        <ul>
            <li>Upon reviewing logs, I discovered suspicious login attempts from multiple external IPs across different countries (South America, Asia), signaling an <strong>APT attack</strong>. These attackers were using compromised credentials to move within the network.</li>
            <li><strong>Rclone.exe</strong>, a well-known data exfiltration tool, was identified as being used to steal data. The exfiltrated files were likely sensitive, including the ginger beer recipe, based on connections to a suspicious domain, <strong>moneybags.biz</strong>.</li>
        </ul>
    </section>

    <section id="investigation-steps">
        <h2>Investigation Steps</h2>
        <ol>
            <li><strong>Identifying Affected Systems:</strong> Cross-referenced the systems associated with the malicious file <strong>Dev-Requirements.zip</strong> and the Mimikatz activity with IP addresses linked to the attack.</li>
            <li><strong>Tracing Network Activity:</strong> Traced the 50 outbound connections related to suspicious files and analyzed DNS logs to trace the exfiltration efforts to <strong>moneybags.biz</strong>.</li>
            <li><strong>Checking for Backdoors:</strong> Investigated evidence of the <strong>HIGHNOON</strong> backdoor in TeamViewer sessions initiated by the attackers.</li>
            <li><strong>Securing Compromised Systems:</strong> Recommended isolating compromised systems, resetting user credentials, and implementing stricter email filtering policies.</li>
            <li><strong>Forensics on Affected Hosts:</strong> Thoroughly examined hosts with the files <strong>Ginger_beer_secret_recipe.pdf</strong> and <strong>Brewery_layout.pdf</strong> and cross-checked external IP addresses involved in the attack.</li>
        </ol>
    </section>

    <section id="recommendations">
        <h2>Recommendations for HopsNStuff</h2>
        <ul>
            <li><strong>Network Segmentation:</strong> Implement stricter segmentation to limit lateral movement and access to sensitive files.</li>
            <li><strong>Email & Web Filtering:</strong> Tighten security around inbound emails and ensure proper web filtering to block malicious sites.</li>
            <li><strong>Credential Management:</strong> Enforce multi-factor authentication (MFA) and regularly rotate user credentials to mitigate the risk of credential harvesting.</li>
            <li><strong>Endpoint Detection & Response (EDR):</strong> Implement or enhance EDR tools to monitor and respond to suspicious processes and file changes on endpoints in real-time.</li>
        </ul>
    </section>

    <footer>
        <p>For more information, feel free to contact me at <a href="mailto:your-email@example.com">your-email@example.com</a></p>
    </footer>

</body>
</html>
