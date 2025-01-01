# Metasploit Learning

In this lab we will be simulating a simple Network with known vulnerabilities to learn the basic principles of the Metasploit framework.

## Objective:
Learn the basics of the Metasploit Framework, including how to use it for scanning, exploiting vulnerabilities, and post-exploitation activities.

## Lab-1
   - In this first lab we will be deploying a docker container with a vulnerable version of Apache:
      - Appache 2.4.49/2.4.50 ([Exploit DB](https://www.exploit-db.com/exploits/50512))

## Lab-2 
      - SSH

## Lab-3
      - FTP

## Building and Running the Dockerfile

   1. Build the Docker image with the following command:

      ```
      sudo docker build -t vulnerable_services .
      ```
      
   2. Run the container with:

      ```
      sudo docker run -d -p 80:80 --name my_vulnerable_container vulnerable_services
      ```

      This setup provides a basic environment for practicing exploitation techniques. Remember to customize configurations and software versions based on specific vulnerabilities you wish to explore.

   3. Optional: Check the Container's Logs

      If you want to see what's happening inside the container, such as checking if Apache started correctly, you can use the following command to view the container's logs:

      docker logs my_vulnerable_apache

      This command will show you the output from the container, including any startup messages from Apache.

## Tasks:
1. **Environment Familiarization**:
   - Understand the Metasploit interface.
   - Learn how to update Metasploit and load modules.

2. **Host Discovery**:
   - Use Nmap to scan the network.

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
