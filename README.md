# Data Capsule Appliance Host

This projects provides the code for automating the Data Capsule Host deployment. 

## Getting Started

Clone this repo using 

```
git clone https://github.com/Data-to-Insight-Center/Data-Capsule-Appliance-Host.git
```

### Prerequisites

You need to install Ansible in the machine that you are using for host provisioning. Refer to http://docs.ansible.com/ansible/latest/intro_installation.html for more details. 

In the host machine, you need to have ssh and python installed (for Ansible).

You need to have an account to login in to the target machine with sudo access. 

### Deploying

1. Add the IP Addresses of the hosts that you need to provision in to the hosts file. 

2. Then run the following command inside the cloned directory. Be sure to replace the <login_username> with your remote username. 

```
ansible-playbook --user=<login_username> -k -i hosts site.yml --ask-become-pass
```

3. Then you will be prompted to enter two password as following. Enter the login remote user password for the first prompt and that user's
sudo password for the second prompt.

```
SSH password:<login_user_password>
SUDO password[defaults to SSH password]:<login_user_sudo_password>
```

This would start up the provisioning of the host machine! You should not see any errors in the terminal when this is being executed. 