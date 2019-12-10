# Ansible Skeleton

```bash
git clone <new empty project>
cd ./<new empty project>
git clone http://github.com/pichuang/ansible-skeleton
ls -la
```

## Tips
1. ping all
```bash
ansible -i hosts all -m ping
```

2. ad-hoc command
```bash
ansible -i hosts all -m shell -a "yum -y install rsync"
```

3. copy files
```bash
ansible -i hosts all -m copy -a "src=/ooxx dest=/xxoo"
```

4. As a root, deploy SSH Key to all machines
```bash
ansible-playbook -i hosts ./utils/deploy_root_sshkey.yml -k
```

## Miscs
- Generate SSH Key
```bash
ssh-keygen -t rsa -b 4096 -f ~/.ssh/id_rsa -q -N ""
cat ~/.ssh/id_rsa.pub
```
