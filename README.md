
# Secondtry

## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![TODO: Update the path with the name of your diagram]
![Diagram - Copy](https://user-images.githubusercontent.com/28880848/110250780-4281a700-7f4b-11eb-8a67-0d6d93b78fb9.PNG)


These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Enter the playbook file._
![elkdockeryml](https://user-images.githubusercontent.com/28880848/110250808-69d87400-7f4b-11eb-9894-71b4b7ed3306.PNG)

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly availble, in addition to restricting in-bound access to the network.
- _TODO: What aspect of security do load balancers protect? What is the advantage of a jump box?_

Loadbalancers protect against DDoS attacks by failing over from the server being attacked to a redudnant server.  

Jumpbox give you a single point of entry to connect to other servers securely using SSH



- _TODO: What does Filebeat watch for?_  
filebeat monitors for and changes in the file system

- _TODO: What does Metricbeat record?_
Meticbeat collects metric and statistical information. 

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
|Jump Box  | Gateway  | 10.0.0.4   | Linux            |
|Web1      | Server   | 10.0.0.5   | Linux            |
|Web2      | Server   | 10.0.0.6   | Linux            |
|DVWVM2    | Server   | 10.0.0.7   | Linux            |
|Elkserver | Server   | 10.1.0.4   | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the elk machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: Add whitelisted IP addresses_
Local public IP address

Machines within the network can only be accessed by jumpbox provisioner. 
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_
Jump Box VM 10.0.0.4

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes                 | Home IP              |
| Web1     | no                  | 10.0.0.4             |
| Web2     | no                  | 10.0.0.4             |
| DVWVM2   | no                  | 10.0.0.4             |
| Elkserver| no                  | 10.0.0.4             |
              

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_ Anisble is used to automate task. 

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...
. Install Docker.IO
. Install Python-pip
. Install Docker
. Start the docker container /Launch

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output]
(Images/dockerPS.PNG)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_
DVWA-VM1 10.0.0.5
DVWA-VM2 10.0.0.6

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_
Filebeat and metricbeat

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the SSH file to Jumpbox Provisioner.

- Update the _____ file to include...

- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_

- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_

- _Which URL do you navigate to in order to check that the ELK server is running?
http://[your.VM.IP]:5601/app/kibana

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._


first_playbook.yml
yum update -y ansible
