# Comandos-Ansible

- ssh-keygen ---> criar chave chaves id_rsa, id_rsa.pub
- ssh-copy-id root@nome_máquina ---> Copia chave pública para o outro host para não ser preciso ficar logando com a senha
- ansible -i hosts all -m ping ---> pinga para as máquinas que estão no arquivo host
- ansible -i hosts all -m apt -a "update_cache=yes name=git state=present" ---> instala o git nas máquinas
- ansible -i hosts all -m git -a "repo=https://github.com/alissondevolps/Comandos-kubernetes dest=/root/comando_kubernetes" ---> Faz o checkout do repositório para pasta comando_kubernetes
- ansible -i hosts all -m apt -a "update_cache=yes name=nginx state=present" ---> instala o nginx nas máquinas
- ansible -i hosts all -m apt -a "update_cache=yes name=nginx state=absent" ---> desinstala o nginx das máquinas
- ansible -i host NOME_DA_MAQUINA -m setup ---> O ansible da um check em tudo que está rodando na máquina
- ansible-playbook -i hosts playbook.yaml ---> Executa o arquivo de nome playbook.yaml
- ansible-galaxy init install_nginx ---> cria uma estrutura de pastas para configurar as roles 



# Links Documentação
- https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
- https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#pip-install
- https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html#installing-ansible-on-fedora-or-centos
- https://galaxy.ansible.com/community/docker


ansible-galaxy collection install community.docker
