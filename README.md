# Ansible Docker Jenkins NGINX
Ansible playbook for provisioning a new server with Docker, Jenkins, and NGINX

*caution work in progress*
### Usage
Built using ansible-playbook version 2.54

Add the IP address of the server being provisioned to hosts file

Locally export the domain name for the SSL certificates

    export JENKINS_DOMAIN=<your-domain.com>

export the default password for the Jenkins' admin user

    export JENKINS_ADMIN="whateverpasswordyouwant"

Run the playbook

    ansible-playbook -b -K main.yml -i hosts
