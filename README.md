# docker-ansible

Ansible docker image with prepared bash aliases

To use these:

1. Copy `.bash_aliases_ansible` file to somewhere (e.g. ~/.bash_aliases_ansible).
2. Add the following line to your .bashrc/.zshrc: 

```
source ~/.bash_aliases_ansible
```
Then you can use commands:

```
ansible all -i hosts -m setup

ansible-playbook -i hosts site.yml

ansible-galaxy install -r requirements.yml

ansible-vault encrypt foo.yml

ansible-doc

```

The editor for the `ansible-vault create` command is nano 
