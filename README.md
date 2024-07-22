### Home-Detection-Lab 

### Introduction

This project outlines the creation of a basic home detection lab for cybersecurity training. The lab setup involves installing VirtualBox to create virtual machines, configuring a Windows 10 machine with Splunk and Sysmon for monitoring, and setting up a Kali Linux machine as an attacker. By simulating attacks and monitoring telemetry data, the lab provides hands-on experience in detecting and analyzing malicious activities using Splunk.

### Objectives

1. **Set Up Virtual Environment:** Install VirtualBox and create virtual machines for Windows 10 and Kali Linux.
2. **Configure Network:** Ensure secure communication between virtual machines using an internal network.
3. **Simulate Attacks:** Use Kali Linux to conduct network scans and deploy custom malware on the Windows 10 machine.
4. **Monitor and Detect:** Utilize Splunk and Sysmon on the Windows 10 machine to detect and analyze malicious activities.
5. **Enhance Skills:** Develop practical skills in setting up and managing virtual labs, using cybersecurity tools, and performing threat detection.

### Skills Learned

- Setting up and configuring virtual machines using VirtualBox.
- Installing and configuring Windows 10 and Kali Linux for cybersecurity purposes.
- Using Splunk and Sysmon for monitoring and detecting malicious activities.
- Creating and deploying custom malware using MSFvenom and Metasploit.
- Conducting network scans and exploiting vulnerabilities with Nmap and Metasploit.

### Tools Used

- **VirtualBox:** Virtualization software to create and manage virtual machines.
- **Windows 10:** Operating system for the target machine.
- **Kali Linux:** Operating system for the attacker machine.
- **Splunk:** Security information and event management (SIEM) tool for monitoring and analyzing telemetry data.
- **Sysmon:** Windows system service for logging system events.
- **Nmap:** Network scanning tool for discovering open ports.
- **MSFvenom and Metasploit:** Tools for creating and deploying custom malware.

### Steps Taken

1. **Install VirtualBox:**
   - Download and install VirtualBox on the host machine.
   - Create a new virtual machine for Windows 10 and another for Kali Linux.

2. **Install Windows 10:**
   - Install Windows 10 on the first virtual machine.
   - Install Splunk and configure it for monitoring.
   - Install Sysmon to log system events and send data to Splunk.

3. **Install Kali Linux:**
   - Install Kali Linux on the second virtual machine.
   - Configure both virtual machines to use an internal network to ensure secure communication.

4. **Network Configuration:**
   - Ensure that the internal network setup prevents any potential infection of the host machine.
   - Verify that Windows 10 and Kali Linux can communicate with each other over the internal network.

5. **Conduct Network Scan:**
   - Use Nmap from Kali Linux to scan the Windows 10 machine and discover open ports.
   - After the scan, it was discovered that port 3389 (Remote Desktop Protocol) is open on Windows 10.

6. **Disable Windows Defender:**
   - Temporarily disable Windows Defender on the Windows 10 machine to allow malware execution.

7. **Create and Deploy Malware:**
   - Use MSFvenom to create custom malware with the payload `windows/x64/meterpreter_reverse_tcp`.
   - Start Metasploit's msfconsole on Kali Linux and set up the multi/handler to receive the reverse TCP connection.

8. **Simulate Attack:**
   - Execute the malware on the Windows 10 machine.
   - Monitor and detect the malware execution in Splunk using the telemetry data provided by Sysmon.

### Conclusion

By setting up a basic home detection lab, this project provides a comprehensive hands-on experience in configuring virtual environments, simulating cyber attacks, and detecting malicious activities. The integration of Splunk and Sysmon on a Windows 10 machine allows for effective monitoring and analysis, while the use of Kali Linux as an attacker machine facilitates realistic attack simulations. This lab setup not only enhances practical cybersecurity skills but also underscores the importance of continuous monitoring and proactive threat detection in securing digital environments.
