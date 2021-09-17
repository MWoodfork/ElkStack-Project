# ElkStack-Project
First Cyber Security Project
## Automated ELK Stack Deployment
The files in this repository were used to configure the network depicted below.
HW12-SubmissionFile(Michael Woodfork).png
These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the YAML file may be used to install only certain pieces of it, such as Filebeat.
  - _TODO: Elk_playbook.yml
This document contains the following details:
- Description of the Topology 
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build
### Description of the Topology
The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.
Load balancing ensures that the application will be highly effective, in addition to restricting traffic Access to the network.
- _TODO: What aspect of security do load balancers protect? They prevent unwanted or unauthorized traffic from reaching the application. 
What is the advantage of a jump box? They add a security layer to the web servers preventing them from being exposed to the public.
Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the configuration files and system files.
- _TODO: What does Filebeat watch for? Watch for log files and events.
- _TODO: What does Metricbeat record? Metrics from on going services on the server.
The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.
| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump-Box | Gateway  | 10.0.0.1   | Linux            |
| Web1     | Webserver| 10.0.0.5   | Linux            |
| Web2     | Webserver| 10.0.0.6   | Linux            |
| Elk-VM   | Webserver| 10.1.0.4   | Linux            |

### Access Policies
The machines on the internal network are not exposed to the public Internet. 
Only the Jump-Box Provisioner machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: Add whitelisted IP addresses_99.32.151.109
Machines within the network can only be accessed by Jump-Box.
- _TODO: Which machine did you allow to access your ELK VM? My Computer  
         What was its IP address? 99.32.151.109
A summary of the access policies in place can be found in the table below.
| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump-Box | Yes                 | 10.0.0.4             |
| Web1     | No                  | 40.91.111.59         |
| Web2     | No                  | 40.91.111.59         |
| Elk-VM   | No                  | 10.1.0.4             |

### Elk Configuration
Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- 
_TODO: What is the main advantage of automating configuration with Ansible? It allows changes to be made within any of the VMs associated with it.
The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., Install Docker.io; Install Python3-pip; Install Python Dock Module; Download and configure an Elk-Docker container; Launch the Elk-Docker container 
- ...
- ...
The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.
![TODO: Update the path with the name of your screenshot of docker ps output] Capture DockerPS.PNG
### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_
  10.0.0.4; 10.0.0.5; 10.0.0.6


We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_
Filebeat and Metricbeat
These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. Filebeats monitors log files and log events of locations that are specified.

Metricbeat collects metric data from your target servers, this could be operating system metrics such as CPU or memory or data related to services running on the server. It can also be used to monitor other beats and ELK stack itself
### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 
SSH into the control node and follow the steps below:
- Copy the ansible config file to run playbook.
- Update the ansible host file to include...
- Run the playbook, and navigate to Jump-Box to check that the installation worked as expected.
_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it? Elk-playbook.yml
- _Which file do you update to make Ansible run the playbook on a specific machine? Ansible-playbook
How do I specify which machine to install the ELK server on versus which to install Filebeat on? By using the Ips of the servers
- _Which URL do you navigate to in order to check that the ELK server is running?  http://thatdaysipaddress:5601/app/kibana
