# itsec
Summary of everything I learned in TryHackme and other cool applications about IT Security.

- [itsec](#itsec)
  - [Commands](#commands)
    - [history](#history)
    - [whoami](#whoami)
    - [cat (concatenate)](#cat-concatenate)
    - [SCP (Secure Copy)](#scp-secure-copy)
    - [wget](#wget)
      - [Example](#example)
    - [ps](#ps)
    - [top](#top)
    - [kill](#kill)
    - [SIG Codes](#sig-codes)
    - [gobuster](#gobuster)
    - [nmap (Network mapper)](#nmap-network-mapper)
    - [exiftool](#exiftool)
    - [systemctl](#systemctl)
    - [echo](#echo)
    - [fg](#fg)
  - [Linux](#linux)
    - [How do processes start?](#how-do-processes-start)
    - [Backgrounding and Foregrounding](#backgrounding-and-foregrounding)
    - [Crontabs](#crontabs)
    - [Package Management](#package-management)
  - [Offensive Security](#offensive-security)
  - [Defensive Security](#defensive-security)
    - [What is it](#what-is-it)
    - [SOC (Security Operations Center)](#soc-security-operations-center)
    - [DFIR (Digital Forensics and Incident Response)](#dfir-digital-forensics-and-incident-response)
      - [_Incident Response_](#incident-response)
      - [Malware Analysis](#malware-analysis)
  - [Jobs](#jobs)
    - [Security Analyst](#security-analyst)
    - [Security Engineer](#security-engineer)
    - [Incident Responder](#incident-responder)
    - [Digital Forensics Examiner](#digital-forensics-examiner)
    - [Malware Analyst](#malware-analyst)
    - [Penetration Tester](#penetration-tester)
    - [Red Teamer](#red-teamer)
  - [(Web) Application security risks](#web-application-security-risks)
    - [Injection](#injection)
    - [Identification and Authentication Failure](#identification-and-authentication-failure)
    - [Broken Access Control](#broken-access-control)
    - [Cryptographic Failure](#cryptographic-failure)
    - [IDOR (Insecure Direct Object References)](#idor-insecure-direct-object-references)
  - [OS Security](#os-security)
  - [Network Security](#network-security)
    - [Hardware Appliance](#hardware-appliance)
    - [Software Appliance](#software-appliance)
    - [7 Steps of Cyber Kill Chain](#7-steps-of-cyber-kill-chain)
    - [Digital Forensics](#digital-forensics)
  - [Security Operations](#security-operations)
    - [Data Sources](#data-sources)
    - [Services](#services)
  - [Formats](#formats)
    - [EXIF](#exif)
  - [Networking](#networking)
    - [OSI model](#osi-model)
    - [Encapsulation of data](#encapsulation-of-data)
    - [TCP/IP Model](#tcpip-model)
  - [Protocols](#protocols)
    - [DHCP (Dynamic Host Configuration Protocol)](#dhcp-dynamic-host-configuration-protocol)
    - [FTP](#ftp)

## Commands

### history

- Prints commands used by user

### whoami

- Shows the user you are logged in with.

### cat (concatenate)

- prints contents of file on the screen

### SCP (Secure Copy)

- Uses SSH for authentication and encryption of files

### wget 

- Downloads files from an URL

#### Example

```
wget http://127.0.0.1:8000/file
```

### ps
Lists processes. Process ID is incremented from kernel.

```
ps - show processes of current user
ps aux - show processes of all users
```

### top
Real time statistic about processes , refreshes every 10 seconds, can use arrow keys to browse various rows

### kill
Kill process with id 

### SIG Codes

SIGTERM - Kill process, but allow cleanup of task

SIGKILL - Kill process, dont do any cleanup 

SIGSTOP - Stop process

### gobuster

Bruteforces website with subdirectories.
-u : specifies website
-w : list of words

### nmap (Network mapper)

- parameter is IP address
- scans ports for services

Scans everything you need.

- `-p-` to scan all ports
- `--script=` for scripts to be executed

### exiftool

- reads EXIF data from images
- Usage: exiftool <image>

### systemctl

- some apps can be started on the boot of the system
- Usage: systemctl start/stop/enable/disable
  
### echo

### fg

- get a process to the foreground

### dig

- Dig allows us to manually query recursive DNS servers of our choice for information about domains
- `dig <domain> @<dns-server-ip>`
- response
  - Answer: TTL in seconds

## Linux 

### How do processes start?

- OS uses namespaces to split up resources for computer
- systemd sits between OS and user

### Backgrounding and Foregrounding

- & operator 

### Crontabs

- Jobs or processes that need to be executed in a certain time intervall
- Example: 0 *12 * * * cp -R /home/cmnatic/Documents /var/backups/
- \* means we don't care
- Usage: crontab -e
- Format: MIN HOUR DOM (Date Of Month) MON (Month Of Year) DOW (Day Of Week) CMD
- @reboot means that it runs on reboot

### Package Management

- Devs can submit their software
- Usage: add-apt-repository to add repo
- 

## Offensive Security

- active hacking 
- breaking into system, exploiting bugs, finding loopholes

## Defensive Security

### What is it
  -   protecting networks and systems by analyzing and securing threats
  -   investigating infected computers to understand how it was hackend
  -   preventing intrusions from occurring
  -   blue teams are part of def sec
  -   cyber security awareness for users
  -   documenting and managing assets
  -   updating and patching systems
  -   setting up security devides
  -   setting up logging and monitoring devices
  
### SOC (Security Operations Center)

Team that monitors network and systems for malicious cyber attacks or intent.

- Vulnerabilities
- Policy violations
- Unauthorized activity
- Network intrusions

_Threat Intelligence_: Gather information to prepare better against enemies.
 

### DFIR (Digital Forensics and Incident Response)

Analyze evidence of an attack and its perpetrators.

Things that are being analyzed:

- File System
- System Memory
- System Logs
- Network Logs

#### _Incident Response_ 
If an incident occurs there are 4 major phases

1. Preparation
2. Detection and Analysis
3. Containemnt, Eradication and Recovery
4. Post-Incident Activity

#### Malware Analysis

- Static analysis (inspect without running it)
- Dynamic analysis (inspect in controlled environment)
- Ransomware makes user pay for decryption of their files
- Trojan Horses 
- Virus


## Jobs

### Security Analyst
- Analyze company stuff with stakeholders
- Documentation and report about safety of networks
- Develop security plans

### Security Engineer
- Testing and screening security measures across software
- monitor networks and reports
- identify and implement systems needed for optimal security

### Incident Responder
- MTTD, MTTA, MTTR (Detect, Acknowledge, Recover) from attacks
- Developing response plan
- Maintaining best practices
- Post-incident reporting and preparation for future attacks

### Digital Forensics Examiner
- Detective
- Collect evidence 
- Analyze evidence
- Document findings
  
### Malware Analyst
- Analysing suspicious programs and reporting about what they do
- Static analyis / dynamic analysis of amlware
- Document and report findings

### Penetration Tester
- Conduct tests on computer systems
- Perform security assesments, audits and analyse policies
- Evaluate and report on insights

### Red Teamer

## (Web) Application security risks

### Injection

Refers to vulnerability of application where user can insert malicious code as input.

### Identification and Authentication Failure

- no account lockout after certain amount of failed attempts
- Storing user password in plaintext

### Broken Access Control

- everybody can only access the sites that they are supposed

### Cryptographic Failure

- Using HTTP instead of HTTPS
- The used cryptographic algorithm must be strong

### IDOR (Insecure Direct Object References)

- Enumerating objects, products or user_ids is not considered safe since it can be brute-forced

## OS Security

OS is connection between Hardware and Software. 

Security is concerned with attacks against:

1. Confidentiality
2. Integrity
3. Availability


- Authentication and Weak Passwords
- Weak File Permissions
- Access to Malicious Programs


## Network Security

- Secures link between different devices
- Consists of different hardware and software solutions

### Hardware Appliance

- Firewall
  - Allows and block connections defined by rules
- IDS (Intrusion Detection System)
- IPS (Intrustion Prevention System)
- VPN (Virtual Private Network)
  - ensure network traffic cannot be read

### Software Appliance

- Antivirus Software
- Host firewall
  - firewall on your OS as "software"

### 7 Steps of Cyber Kill Chain

1. Recon
   - Attacker tries to learn about hte target
2. Weaponization
   - Preparing a file with malicious code
3. Delivery
   - Code is delivered through mail or USB
4. Exploitation
5. Installation
6. Command & Control
7. Actions on Objectives

### Digital Forensics

- Chain of Custody to ensure that only authorized investigators have access to evidence
- proper search authority: legal authority
- validation with mathematics: with a hash function we can make sure that the file was not modified
- use of validated tools
- repeatability: findings of digital forensics can be reproduced as long as the proper skills and tools are available
- reporting: report with evidence

## Security Operations

- find vulnerability in networks
- detect unauthorized activity
- discover policy violations
- detect intrusions
- support with the incident response
- might use SIEM (Security Information and Event Mangement) system

### Data Sources

- SOC uses many data sources to monitor the network
- Server logs
  - logs on the webservers etc
- DNS activity
  - inspect DNS queries by looking with which domains internal systems are trying to communicate with
- Firewall logs
  - reveal which packets tried to cross firewall
- DHCP logs
  - Inspect DHCP transactions

### Services

- Reactive
  - Monitor security posture
  - Vulneravbility management
  - Malware analysis
  - Intrustion detection
  - Reporting
- Proactive
  - NSM
  - Threat hunting
  - Thread Intelligence

- NSM (Network Security Monitoring)

## Formats

### EXIF

Exchangable Image File Format, has metadata about images files

## Networking

### OSI model

- Application
  - Provides networkig options to programs running on a computer
  - When data is given, it gets passed down into the presentation layer
- Presentation
  - translates data into a standardised format and handles encryption, compression or other transformations of the data
- Session
  - tries to connect to other computer across the network
  - each session is unique to the communication (two tabs possible)
- Transport
  - TCP (data is transmitted correctly, but slow)/UDP (data might not be transmitted correctly, fast)
  - data is divided into bite-sized chunks (TCP -> segments, UDP -> datagrams)
- Network
  - resp. for locating destination of your request
  - logical addressing (IP addresses) are used which are software controlled
- Data Link
  - physical addressing of the transmission
  - receives packet from network layer and adds physical MAC address of the receiving endpoint
  - checks if recieved data has been corrupted during transmission
- Physical
  - data -> electrical pulses -> data

###  Encapsulation of data

- each layer of OSI adds additional info
- Special name for encapsulated data:
  - Layer 1: Bits
  - Layer 2: Frames
  - Layer 3: Packets
  - Layer 4: Segments/Datagrams
  - Layer 5-7: Data
- encapsulation helps with standardizing the data so that everybody communicates in the same way
  
### TCP/IP Model

- Application
- Transport
- Internet
- Network Interface

### DNS (Domain Name System)

- Computer sends a request to a DNS server
- Servers IP is already specified (most of the time via the router or manually)
- If server is not found in cache, recursive DNS Server is asked and passes the request to a root name server
- Root name server passes request to appropriate TLD Server

### TLD (Top-Level Domain) Server

- Are split up in extensions
- E.g. .com will be sent to the TLD Server that handles those domains

### Authorative Server

- TLD passes request to authorative server
- Actually has an entry for every domain in the world
- Returns the domain info

Can all be seen via the [dig](#dig) command.

## Protocols

### DHCP (Dynamic Host Configuration Protocol)

- assigns IP address to systems that try to connect to network

### FTP
- Layer 7 of OSI, can be accessed with FTP client

## Hacking

- Knowledge is power, the more you know about the target system, the better
- Get an idea of the landscape you are attacking

### Port Scanning

- Computer uses multiple ports to connect to different web services
- Port scanning to see if a port is open or not
- nmap industry standard to perform port scan -> can even execute exploits
