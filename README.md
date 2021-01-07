# f5-udf-nginx-plus
Ansible playbook to install and manage NGINX Plus from F5

On infra-server execute:

    cat .ssh/id_rsa.pub

On nginx-plus hosts execute:
    
    echo "<id_rsa.pub of infra-server here" >> .ssh/authorized_keys
    sudo su -
    echo "<id_rsa.pub of infra-server here" >> .ssh/authorized_keys

Put the license files in /home/ubuntu on infra-server

    /home/ubuntu/nginx-repo.{key,crt}

and execute the Ansible Playbook

    cd ~/f5-udf-nginx-plus/ansible
    ansible-playbook playbooks/install-n-plus.yaml

