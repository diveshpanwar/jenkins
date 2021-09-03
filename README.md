# jenkins

# hosts file
```
[all:vars]

ansible_connection = ssh


[test]
test1 ansible_host=remote_host ansible_user=remote_user ansible_private_key_file=/root/ansible/remote-key
```

# Play Book 1
```yaml
- hosts: test1
  tasks:
  - shell: echo "Hello World" > /tmp/ansible-file
 ```

# commands
```bash
ansible -i hosts -m ping test1
ansible-playbook -i hosts play.yml
```



