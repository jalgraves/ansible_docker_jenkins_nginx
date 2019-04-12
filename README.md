# Ansible Docker Jenkins NGINX
Ansible playbook for provisioning a new server with Docker, Jenkins, and NGINX

Built using ansible-playbook version 2.54

*caution work in progress*
### Requirements
* A domain name with a DNS **A** record pointing to the IP address of the server being provisioned.
### Usage

##### Add the domain name to the hosts file

##### Export the domain name and email address for the SSL certificates

    export JENKINS_CERT_DOMAIN=<your-domain.com>
    export JENKINS_CERT_EMAIL=<you@whereever.com>

##### Export the default password for the Jenkins' admin user

    export JENKINS_ADMIN="whateverpasswordyouwant"

##### Run the playbook

    ansible-playbook -b -K main.yml -i hosts
