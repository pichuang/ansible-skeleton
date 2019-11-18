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
