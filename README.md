## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

- URL:


These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the playbook file may be used to install only certain pieces of it, such as Filebeat.

- URL:
- URL:

These contain the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting access to the network.
- Load balancers play an important security role.  They distribute traffic between web servers, which helps defend against a distributed denial of service attack (DDoS). This protects the availability of the server. The advantage of a jump box is having a seperate computer connect directly to computers in a security zone.  This also allows for a single system connections for security updates, such as inbound networking rules.  

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the files and system logs.
- Filebeat watches for log files or locations specified, collects the logs, and sends them to Elasticsearch or Logstash for indexing.
- Metricbeat watches for system log changes and sends the metrics and data to Elasticsearch or Logstash.

The configuration details of each machine may be found below.
Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.1.0.10   | Linux Ubuntu 18.04            |
| Web-1     |  Web Server        | 10.1.0.11           | Linux Ubuntu 18.04                |
| Web-2     |  Web Server        | 10.1.0.8           |Linux Ubuntu 18.04                  |
| ELK Stack     | ELK Server         | 10.0.0.4           |Linux Ubuntu 18.04                  |


### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump Box VM machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- The Load Balancer also accepts connections from the internet through port 80.  
- Access to the Jump Box VM is from white listed home IP address.

Machines within the network can only be accessed by SSH Port 22.
- Jump Box VM (10.1.0.10) has access to the ELK VM.

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes              | Port 80, 13.83.12.147    |
| Load Balancer         | Yes                    | Port 80, 13.83.12.147                     |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- the ELK playbook could be used to spin up 1 or 1,000 VMs. It is efficient and accurate in the roll out of VMs.

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...


### Target Machines & Beats
This ELK server is configured to monitor the following machines:

- 10.1.0.11 (Web-1)
- 10.1.0.8 (Web-2)

We have installed the following Beats on these machines:
- 10.0.0.4 (ELK Server)

These Beats allow us to collect the following information from each machine:
-`Winlogbeat` collects Windows logs, which we use to track user logon events

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running? 52.249.197.220:5601

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
