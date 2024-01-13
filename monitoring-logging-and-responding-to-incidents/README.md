# Monitoring, Logging and Responding to Incidents

## Example Scenario

Imagine a scenario where a user unknowingly downloads a seemingly innocuous file from a malicious website. This file is a Trojan Emotet that, when executed, establishes a connection to a remote Command and Control server controlled by attackers. The compromised system now periodically communicates with the C2 server, awaiting further instructions.

The attackers, observing the compromised system, send commands to the Trojan. These commands might include:

- **Download and Execute Additional Malware**: The Trojan is instructed to download and execute more malicious files, expanding the scope of the attack.

- **Data Exfiltration**: The compromised system is directed to send sensitive data, such as login credentials or corporate documents, back to the C2 server.

- **Remote Access**: The attackers may use the C2 connection to gain remote access to the compromised system, effectively controlling it as if they were physically present.

The use of a Command and Control infrastructure allows attackers to adapt their tactics, techniques, and procedures (TTPs) dynamically, making detection and mitigation more challenging for defenders. Security measures often involve identifying and blocking C2 communications, isolating compromised systems, and removing the malicious payloads.

In this project, we will see an example of Command and Control activity.

# Project Details
This project "Intrusion and Detection Systems" is part of my Security Analyst Nanodegree curriculum at Udacity.
## Scenario

Jacqui, the security analyst for Yoyodyne's satellite office in Kalamazoo, is taking a much-needed vacation. Corporate has asked me to fill in for her while she enjoys some time on the beach.

### A message in my inbox reads:

From: jacqui@kz.yoyodyne

To: me@hq.yoyodyne

Subject: hope this helps!

I found a network diagram for you. A couple years old, but mostly up-to-date!

I jotted down some notes on the usual incident handling processes, at least here in the KZ office.

I launched a honeypot earlier this week. I meant to exclude it from the alerts, but what are the chances that any bad actors would have found it already?

Sorry I did not have time to put together more info! Good luck!

-j

## TO DO
My job include to analyse alerts in the Intrusion Detection System, set up SIEM to collect and analyse date, monitor systems for suspicious activity, document evidence and follow the incident handling procedure to respond to any issues you uncover.

## Thinking Like a Security Analyst

I will be spending a lot of time reviewing data in the logging and monitoring systems. This will include
monitoring and analyzing alerts from the host-based logs and network logs. Given that logging involves
both the host hardware as well as the applications running on that hardware, using host-based logs and
network packets, we may classify whether that a threat is a True positive or not.
 
#### Snort:

Starting with network IDS (Intrusion Detection System) logs (Snort) which provide data for packets
that match threat signatures, the question is: are there suspicious connections? If yes, identify the
IP address and ports involved in the connections.
 
#### Host logs: 

If there's an external IP address, pivot to the DNS (Domain Name System) logs and check for any
DNS replies that included the external IP address. DNS logging can help you monitor the data
exchanged during the resolution and spot threats such as malicious URLs or emails from known
phishing domains, malicious command-and-control (C2) domains, If yes, what was the associated
hostname? Pivot to the logs of the connection summaries - the Zeek logs and check if there were connections
to or from the same external address.
  Check HTTP logs for unusual, suspicious or malicious processes.
  

## Outline

- Analyse Alerts from the Intrusion Detection System using **Sguil**: Please go to [IDS-snort-alert-analysis](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/monitoring-logging-and-responding-to-incidents/IDS-snort-alert-analysis.pdf) to follow analysis.

- Live Packet Capture with **Tcpdump**: Multiple Snort alerts were triggered by a single DNS request. We have identified the DNS request in Sguil that triggered the multiple alerts and recorded the same request from the Security Onion VM using tcpdump. See [dns.pcap]() for captured packet. 


- Read and analyse Packet Capture with **Wireshark**

- Create new **Snort** rules to detect all alerts. See [local.rules](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/monitoring-logging-and-responding-to-incidents/local.rules) for the snort rules. 

- Use **Splunk** to Collect and Analyse Data

- Use the **Incident Response Playbook** to determine the next Steps: Containment, Analysis and Recovery
