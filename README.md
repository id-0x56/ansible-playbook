## Ansible playbooks

- *kubelet, kubeadm, kubectl*
- *docker, docker-compose*
- *curl, git, mc*

### Installation
```
sudo apt update && sudo apt install -y ansible sshpass
```
```
export ANSIBLE_HOST_KEY_CHECKING=False
```

### Configure
```
ansible-playbook -i inventory playbook-00-update.yml --user=ubuntu --ask-pass --ask-become-pass
```
```
ansible-playbook -i inventory playbook-01-ssh.yml --user=ubuntu --ask-pass
```
```
ansible-playbook -i inventory playbook-02-default.yml --user=ubuntu --ask-become-pass
```
```
ansible-playbook -i inventory playbook-03-kubernetes.yml --user=ubuntu --ask-become-pass
```
```
ansible-playbook -i inventory playbook-04-php.yml --user=ubuntu --ask-become-pass
```

### Ping
```
ansible all -i inventory -m ping --user=ubuntu --ask-pass
```

### Usage
*Try it now!*
