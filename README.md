WhatsApp-Based Port Scanner Alert System
Cybersecurity Automation Project Report

1. # Introduction

This project demonstrates a lightweight network monitoring tool that automatically scans a target host for vulnerable ports and sends real-time alerts through WhatsApp. The purpose is to simulate early-warning intrusion detection and practice Python automation within a home-lab cybersecurity environment. The project avoids third-party paid APIs and instead uses WhatsApp Web automation.

2. # Objectives

Detect open ports on a target system within a local network

Automate alert notifications using the user’s existing WhatsApp account

Build a simple, customizable security tool using Python

Strengthen understanding of port scanning and basic threat monitoring

3. # Tools & Technologies

Python 3

socket – used to perform TCP port probing

pywhatkit – used to automate WhatsApp Web messaging

datetime & time – used for logging and timing

VS Code – development and execution environment

4. # Methodology

A list of the most commonly exploited ports (FTP, SSH, Telnet, SMB, HTTP, 8080, etc.) is defined.

The script attempts TCP connections to each port on the target IP address.

Open ports are collected and logged with timestamps.

If one or more ports are open, the script triggers an automated WhatsApp alert using pywhatkit, which opens WhatsApp Web and sends the alert directly to the user’s phone.

The browser closes after sending the message, maintaining a clean workflow.

5. Results

The script successfully identifies open ports and sends formatted WhatsApp alert messages that include:

Timestamp

Target IP

List of detected open ports

Basic security advisory

This provides a practical and functional notification mechanism for small-scale monitoring without the need for email servers or SMS APIs.

6. Key Features

Real-time WhatsApp alerts

No Twilio, SMTP, or external API required

Fast TCP scanning using Python sockets

Simple to modify for different networks or ports

Good foundation for building custom SOC-style tools

7. # Limitations

WhatsApp Web must stay logged in for messages to send

Not a replacement for enterprise vulnerability scanners

Single-threaded scanning (can be improved with multi-threading)

8. # Future Enhancements

Continuous monitoring loop (scan every X minutes)

Logging results to a file or database

Multi-threaded or asynchronous port scanning

Service banner grabbing for deeper analysis

Adding firewall auto-block rules for detected threats

9. # Conclusion

This project provides a practical demonstration of how Python can automate cybersecurity monitoring tasks. By combining port scanning with WhatsApp notifications, the tool delivers an immediate and accessible alert system that can be used in home labs, student projects, or small-scale security environments. The project reinforces knowledge of networking fundamentals and real-world automation techniques.

# Screenshots
