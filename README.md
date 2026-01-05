Project Overview

This project documents the investigation of a malicious .NET executable identified as the Yellow Cockatoo RAT (also known as Solarmarker). The analysis focuses on identifying key Indicators of Compromise (IOCs), understanding the malware's timeline, and uncovering its Command and Control (C2) infrastructure using open-source intelligence (OSINT) and behavioral analysis tools.

Objectives

Identify the initial submission timeline to global threat databases.
Locate artifacts dropped on the filesystem for persistence or data storage.
Determine the primary Command and Control (C2) server used for data exfiltration.

Tools & Resources Used

CyberDefenders: Blue team training platform.

VirusTotal: For static analysis, behavioral patterns, and community-sourced threat labels.

Red Canary (Threat Intel): Used to cross-reference behavioral artifacts and known malware patterns.

Kali Linux: Environment used for accessing the lab and performing investigations.

Key Findings

High Detection Rate: The file was flagged by 57 out of 72 security vendors, primarily labeled as a "Trojan.MSIL/Polazert."

Persistence Mechanism: The malware utilizes the AppData folder to store encrypted identification data, making it a key location for incident responders to sweep.

Data Exfiltration: The C2 communication involves sending byte-encoded JSON strings containing sensitive host metadata to the remote server.
