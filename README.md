This readme file describes the purpose and usage of two Ansible playbooks.

Prerequisites
Ansible installed on your machine.
Ansible inventory file with hosts defined.
SSH access to the target hosts.
Internet connectivity on the target hosts.
Task1 Playbook
The task1.yml playbook installs Docker, Git and Python3 on the app host.

Tasks:
Downloads Docker script and installs it on the target.
Installs Git and Python3 on the target.
How to run:
To execute the playbook, run the following command:

ansible-playbook -i <inventory-file> task1.yml
Note: Replace <inventory-file> with the path to your Ansible inventory file.

Task2 Playbook
The task2.yml playbook installs pip modules, creates a git archive from a repository, starts and enables Docker service, copies docker-compose file to the target host, and starts the services on the target host.

Tasks:
Upgrades pip on the target host.
Installs pip modules on the target host.
Creates a git archive from a repository on the target host.
Starts and enables Docker service on the target host.
Copies docker-compose file to the target host.
Creates and starts services on the target host.
How to run:
To execute the playbook, run the following command:

ansible-playbook -i <inventory-file> task2.yml -e ansible_python_interpreter=/usr/bin/python3
Note: Replace <inventory-file> with the path to your Ansible inventory file.
