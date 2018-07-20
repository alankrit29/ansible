#### A BRIEF INTRODUCTION TO ANSIBLE    

Ansible is configuration management and provisioning tool, quite similar to puppet or chef. It is a simple IT automation system that handles configuration-management, application deployment, cloud provisioning, multiple task execution and multi-node orchestration, including trivializing things like zero downtime rolling updates with load balancers.

These configuration management systems are used to act as a servers for administration and operation that allow you to control many different systems in an automated way from one central location. Thus, we can have a centralized server to control and configure all the client machines.

For IT personnels, tasks can be repetitive and exploiting same amount of resources over similar tasks is not a good way to go. With this automation tool, IT admins can automate their tasks and speedup their efforts. It uses simple, less complex way to begin with it. It uses SSH connection from server side to client side and no configuration is required to be done on the clients side. Automation and configuration management makes a lot of sense when it cuts down setup time and efforts.

#### ANSIBLE SETUP

To begin with this project, first ensure that ansible is installed on your server. Refer to the following link to install ansible on your Ubuntu server:

> https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#latest-releases-via-apt-ubuntu

Now, in order to configure client machines ready from deployment, share ssh-copy-id from Ansible server to client machines. For installation of ansible and further server and client configuration, refer to link:

> https://cloudkul.com/blog/installation-ansible-ubuntu-14-04/

#### LAMP DEPLOYMENT USING ANSIBLE

> Clone this repository and create host entries from client machines in *host* file. By default, ansible takes values of host from */etc/ansible/host* file, but you can change its file path in config file */etc/ansible/ansible.cfg*.

> In *host* file set variable values from database name, mysql password, PHP version, Mysql version.

> Go to *group_vars* directory, create a file with name as the ssh host name, and create an entry for *ansible_ssh_user*.

> Now, run playbook in dry-run mode: ansible-playbook -v lamp.yml --check

> If all checks are passed, run the ansible lamp playbook as: ansible-playbook -v lamp.yml

After Ansible deployment, login client servers and check if everything is as good as it was planned.
