# docker-ansible
![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/kalw/docker-ansible.svg?style=plastic)


Ansible docker image with prepared bash aliases

To use these:

1. Copy `.bash_aliases_ansible` file to somewhere (e.g. ~/.bash_aliases_ansible).
2. Add the following line to your .bashrc/.zshrc: 

```
source ~/.bash_aliases_ansible
```
Note that it will try to mount directory you're on into the container.
This will give you acccess to files like this: 

``` 
$cat ./host.file
127.0.0.1
$ansible -m ping -i host.file
```

If you're on osx w/docker-for-mac remember that you're home (/Users/my_user) only is accessible to docker volume mounts.  

Then you can use commands:

```
ansible all -i hosts -m setup

ansible-playbook -i hosts site.yml

ansible-galaxy install -r requirements.yml

ansible-vault encrypt foo.yml

ansible-doc

```

The editor for the `ansible-vault create` command is nano 
