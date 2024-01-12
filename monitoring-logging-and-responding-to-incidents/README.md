# Monitoring, Logging and Responding to Incidents

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

- Analyse Alerts from the Intrusion Detection System using **Sguil** see [IDS-snort-alert-analysis]( mm)Deliverables to see project output.

- Live Packet Capture with **Tcpdump**

- Read and analyse Packet Capture with **Wireshark**

- Create new **Snort** rules to detect all alerts 

- Use **Splunk** to Collect and Analyse Data

- Use the **Incident Response Playbook** to determine the next Steps: Containment, Analysis and Recovery

Please go to Deliverables to see project output.
