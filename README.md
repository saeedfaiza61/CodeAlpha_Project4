# CodeAlpha_Project4
Network-Based Intrusion Detection System (NIDS) using Suricata on Kali Linux.
# Network Intrusion Detection System (NIDS)

## Project Overview

This project implements a Network-based Intrusion Detection System (NIDS)
using Suricata on Kali Linux.

The system monitors network traffic, detects suspicious activity using
custom Suricata rules, records security incidents, performs response
actions, and visualizes detected incidents.

## Objectives

The main objectives of this project are:

1. Set up a network-based intrusion detection system.
2. Configure custom rules and alerts.
3. Monitor network traffic for potential threats.
4. Implement a response mechanism for detected intrusions.
5. Visualize detected security incidents.

## Technologies Used

- Kali Linux
- Suricata
- Python 3
- Custom Suricata Rules
- Network traffic monitoring
- Matplotlib (for visualization, if used by visualize.py)

## Project Files

### custom.rules

Contains custom Suricata detection rules used to identify suspicious
network activity.

### incident.logs

Stores information about detected security incidents.

### response.py

Python script used to perform a response action when suspicious
activity is detected.

### blocked.ip.txt

Contains IP addresses identified for blocking by the response mechanism.

### visualize.py

Python script used to visualize detected incidents.

## System Workflow

Network Traffic
        |
        v
     Suricata
        |
        v
  Custom Rules
        |
        v
     Alert
        |
        +----------------+
        |                |
        v                v
 incident.logs      response.py
                         |
                         v
                  blocked.ip.txt
                         |
                         v
                  visualize.py

## Detection Process

Suricata continuously monitors network traffic through the selected
network interface.

When traffic matches a rule defined in custom.rules, Suricata generates
an alert.

The alerts can be examined through Suricata log files such as:

- fast.log
- eve.json

## Response Mechanism

The response component processes detected suspicious activity and
records the relevant IP address in blocked.ip.txt.

This provides a basic automated response mechanism for the NIDS.

## Visualization

The visualize.py script processes the incident information and creates
a graphical representation of detected security events.
# Conclusion

The implemented NIDS demonstrates the basic workflow of a network
intrusion detection system. Suricata was used to monitor network
traffic and identify suspicious activity through custom rules.

The project also includes a response mechanism and visualization
component, providing an end-to-end demonstration of detection,
logging, response, and analysis.
