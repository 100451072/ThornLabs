# Atomic Red Panda

In this lab we will be simulating the use of Atomic Red (based in the MITRE ATT&CK Matrix) and the implementation of Blue Team Techniques to recognize and respond to this threats.

## Overview
This lab is designed to simulate cybersecurity attack scenarios using Atomic Red Team. Allowing users to execute, tests, and analyze different attack techniques in a controlled, isolated setting using Docker containers.

## Attack
The attacks that we are going to be simulated follow the steps described in the MITRE ATT&CK:

Take into account that any attack chain from the MITRE ATT&CK Matrix can be executed and studied.

## Blue Team Tools
### 1. **Logging and Monitoring Tools**

- **ELK Stack (Elasticsearch, Logstash, Kibana)**:
  - Collects and visualizes logs from your Docker containers. Logstash can be used to aggregate and parse logs, Elasticsearch for log storage, and Kibana for visualization.

- **Prometheus and Grafana**:
  - Prometheus is an open-source monitoring solution that collects metrics from your Docker containers at defined intervals. Grafana can then be used to visualize those metrics in a user-friendly dashboard.

- **Syslog-ng or rsyslog**:
  - These are powerful syslog servers for log management, which can be used to centralize logs from various containers for analysis and archiving.

### 2. **Intrusion Detection Systems (IDS)**

- **Suricata**:
  - A network-based IDS that can be used to monitor network traffic in and out of Docker containers and detect suspicious activities based on signatures.

- **Ossec**:
  - An open-source, host-based IDS that provides log analysis, file integrity checking, policy monitoring, rootkit detection, and real-time alerting for Docker hosts.

### 3. **File Integrity Monitoring**

- **AIDE (Advanced Intrusion Detection Environment)**:
  - A file integrity monitoring tool that can help detect unauthorized changes to files within your Docker containers.

### 4. **Security Auditing Tools**

- **Lynis**:
  - An open-source security auditing tool for Unix-based systems, useful for performing in-depth security scans and vulnerability assessments of your Docker host and containers.

### 5. **Container Security Tools**

- **Clair**:
  - An open-source project designed to perform static analysis of vulnerabilities in application containers (including Docker).

- **Docker Bench for Security**:
  - A script that checks for dozens of common best-practices around deploying Docker containers in production, based on the CIS Docker Benchmark.

### 6. **Network Security Tools**

- **Fail2Ban**:
  - Scans log files and bans IPs that show malicious signs, such as too many password failures, seeking for exploits, etc., useful for protecting services running within Docker containers.

- **Wireshark or tcpdump**:
  - Network protocol analyzers that can capture and interactively browse the traffic running on a network. These tools can be used to monitor the traffic in and out of your Docker network.

### 7. **Endpoint Protection and Response**

- **Wazuh**:
  - A security monitoring solution that extends its capabilities to security events and information management (SIEM), playing a crucial role in IT security, and compliance.

Each tool serves specific purposes and can be configured to monitor and protect your Docker environments effectively. Integrating these tools into your Docker setup enhances your ability to detect, respond to, and mitigate threats within your containerized applications.

## Setup Instructions
1. **Environment Preparation**:
    - Ensure Docker is installed on your system. You can download it from [Docker Hub](https://hub.docker.com/).
    - Clone the Atomic Red Team repository from GitHub:
      ```
      git clone https://github.com/redcanaryco/atomic-red-team.git
      ```

2. **Docker Setup**:
    - Build the Docker Image:
    ```bash
    docker build -t atomic-red-team .
    ```
    - Run the Container:
    ```bash
    docker run -it --name atomic-test-env atomic-red-team
    ```

## Running the Lab
1. **Access the Control Container**:
    - Use the following command to access the main control container where Atomic Red Team is set up:
      ```
      docker exec -it atomic_control bash
      ```

## Execute the Attack
1. **Attack chain execution**:
    - Execute the attack chain explained in the Attack section above.

## Analyzing Results
1. **Log Collection**:
    - Access logs and outputs from the test executions are stored in:
      ```
      /var/log/atomic_logs/
      ```
    - Review these logs to analyze the behavior and outcome of the tests.

2. **Reporting**:
    - Generate reports based on the logs collected to understand the impact and detection capabilities:
      ```
      python generate_report.py
      ```

## Cleanup
1. **Teardown Environment**:
    - To clean up and remove all Docker containers used in the lab, run:
      ```
      docker-compose down
      ```

## Contributing
- If you find any issues or have improvements, please submit a pull request or open an issue in the repository.

## License
- This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details.

## Acknowledgments
- Thanks to the Red Canary team for providing the Atomic Red Team as an open-source resource.
