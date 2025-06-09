
# Sysmon Log Parser

![Sysmon Logo](https://upload.wikimedia.org/wikipedia/commons/1/19/Sysinternals_Sysmon_Logo.png)

## Overview

The **Sysmon Log Parser** is a PowerShell script designed to extract, filter, and export key Windows Sysmon event logs related to system activity. This tool focuses on capturing high-value event IDs — specifically:

- **Event ID 1**: Process Creation  
- **Event ID 3**: Network Connection  
- **Event ID 11**: File Creation  

By parsing these events and exporting them to a CSV file, this script aids Security Operations Center (SOC) analysts in monitoring system behaviors and identifying potential threats efficiently.

---

## Features

- Retrieves Sysmon Operational logs for specified Event IDs  
- Outputs parsed data including timestamp, event ID, and detailed message  
- Saves results as a CSV file in the user’s Documents folder for easy access  
- Lightweight and easy to customize or extend for additional event monitoring

---

## Installation & Usage

### Prerequisites

- Windows 10 or later with Sysmon installed and running  
- PowerShell (version 5.1 or later)  
- Sysmon configured to log Event IDs 1, 3, and 11 (default or custom configuration)

### Steps

1. Clone or download this repository  
2. Open PowerShell and navigate to the script’s directory, e.g., your Documents folder:  
   ```powershell
   cd "$env:USERPROFILE\Documents"

	3.	Run the script:

.\SysmonLogParser.ps1


	4.	After execution, check the generated CSV file at:

C:\Users\<YourUsername>\Documents\SysmonLogResults.csv



⸻

Sample Output

TimeCreated	EventID	Message
2025-06-09 22:30:00	1	Process Create: Image: C:\Windows\cmd.exe
2025-06-09 22:31:15	3	Network Connect: Source IP: 192.168.1.5
2025-06-09 22:32:10	11	File Created: Path: C:\Temp\test.txt


⸻

Future Enhancements
	•	Integrate filters to isolate suspicious or anomalous events
	•	Automate email alerts based on event patterns
	•	Expand to monitor additional Sysmon Event IDs relevant to threat detection
	•	Create a GUI wrapper for ease of use by non-technical analysts

⸻

About Me

I’m a cybersecurity enthusiast actively building my SOC analyst toolkit through practical projects like this. My passion is bridging the gap between raw data and actionable security insights, empowering organizations to stay ahead of threats.

⸻

License

This project is open-source and available under the MIT License.

⸻

Created by Mary O
