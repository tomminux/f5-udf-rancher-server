# f5-udf-rancher-server
Ansible playbook to install and manage Rancher Server

On infra-server execute:

    cat .ssh/id_rsa.pub

On rancher-server hosts execute:
    
    echo "<id_rsa.pub of infra-server here" >> .ssh/authorized_keys
    sudo su -
    echo "<id_rsa.pub of infra-server here" >> .ssh/authorized_keys

and execute the Ansible Playbook

    cd ~/f5-udf-rancher-server/ansible
    ansible-playbook playbooks/install-rancher-server.yaml

