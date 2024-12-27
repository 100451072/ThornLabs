# ThornLabs
Cybersecurity Labs

Cybersecurity labs using Docker, organized by varying levels of difficulty:

### Beginner
1. **Basic Network Scanning Lab**:
   - **Objective**: Learn to use Nmap for network discovery.
   - **Setup**: Configure a Docker network with multiple containers simulating different network hosts. Each host should have varying configurations and services exposed.
   - **Tasks**: Discover all active hosts, identify open ports, and determine services running on each host.

2. **Phishing Simulation**:
   - **Objective**: Understand how phishing works and the basics of crafting phishing emails.
   - **Setup**: Use a simple SMTP server in a container and another container as the target.
   - **Tasks**: Send simulated phishing emails and analyze the actions taken by the receiving container.

### Intermediate
3. **Web Application Penetration Testing Lab**:
   - **Objective**: Learn to identify and exploit common web vulnerabilities.
   - **Setup**: Deploy vulnerable web applications like OWASP Juice Shop or DVWA in containers.
   - **Tasks**: Execute SQL injection, XSS, and CSRF attacks. Practice mitigating these vulnerabilities.

4. **Incident Response with Atomic Red Team**:
   - **Name**: AtomicRedPanda.
   - **Objective**: Simulate attack scenarios and practice incident response.
   - **Setup**: Use Atomic Red Team to trigger different TTPs (Tactics, Techniques, and Procedures) in your containerized environment.
   - **Tasks**: Detect and respond to simulated attacks using tools like Splunk or ELK stack for log analysis.

### Advanced
5. **Network Segmentation and Firewall Rules Testing**:
   - **Objective**: Understand network segmentation and practice crafting and applying firewall rules.
   - **Setup**: Create a complex Docker network that mimics a segmented corporate network with Docker-compose.
   - **Tasks**: Implement and test firewall rules between segments to ensure only authorized traffic flows between containers.

6. **Malware Analysis Lab**:
   - **Objective**: Analyze malware behavior in a controlled environment.
   - **Setup**: Use Docker to create a safe, isolated lab environment where you can run and analyze malware samples.
   - **Tasks**: Automate the collection of malware analysis data like network traffic, changed files, and system calls.

### Expert
7. **Advanced Persistent Threat (APT) Simulation**:
   - **Objective**: Simulate an APT to understand stealth techniques and long-term impact.
   - **Setup**: Create a multi-stage attack involving initial exploitation, establishing backdoors, lateral movement, and data exfiltration.
   - **Tasks**: Implement and respond to each stage, enhancing detection and response strategies.

8. **Zero Day Exploit Research Lab**:
   - **Objective**: Explore vulnerability research and exploit development.
   - **Setup**: Use containers to isolate various applications or systems with known vulnerabilities, escalating in difficulty, possibly even unknown vulnerabilities.
   - **Tasks**: Research, develop, and test exploits. Document findings and develop patches or mitigation strategies.

These projects can help you delve deeper into various aspects of cybersecurity, from the basics of network scanning to advanced research on zero-day exploits.
