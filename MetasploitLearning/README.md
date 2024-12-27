# Metasploit Learning

In this lab we will be simulating a simple Network with known vulnerabilities to learn the basic principles of the Metasploit framework.

#### Objective:
Learn the basics of the Metasploit Framework, including how to use it for scanning, exploiting vulnerabilities, and post-exploitation activities.

#### Setup:
1. **Metasploit Container**: Set up a Docker container with Metasploit installed. This will be your attack machine.
2. **Vulnerable Targets**: Deploy one or more Docker containers running vulnerable services or applications. You could use containers with vulnerable versions of software like an FTP server, a web application, or an operating system image.

#### Tasks:
1. **Environment Familiarization**:
   - Understand the Metasploit interface.
   - Learn how to update Metasploit and load modules.

2. **Host Discovery**:
   - Use Metasploit's `db_nmap` module to perform network scanning and automatically store the output in Metasploit's database.

3. **Vulnerability Scanning**:
   - Utilize Metasploit's scanning modules to identify vulnerabilities in the target containers.
   - Learn how to interpret scan results and choose appropriate exploits.

4. **Exploitation**:
   - Select an exploit based on the vulnerability scan results.
   - Configure and launch the exploit against a target to gain access.
   - Understand the options and configurations necessary for successful exploitation.

5. **Post-Exploitation**:
   - Use Metasploit's post-exploitation modules to gather further information from the exploited system.
   - Explore how to pivot from the compromised host to access other parts of the network.

6. **Reporting**:
   - Generate a report of the activities performed, including discovered hosts, identified vulnerabilities, and exploited systems.

#### Learning Outcomes:
- Gain hands-on experience with Metasploit's core functionalities.
- Understand how to transition from reconnaissance to gaining and expanding access within a network.
- Develop skills in using Metasploit's database to manage and utilize gathered data effectively.

This lab will provide a foundational understanding of how to use Metasploit effectively in real-world scenarios, preparing you for more complex security testing tasks.
