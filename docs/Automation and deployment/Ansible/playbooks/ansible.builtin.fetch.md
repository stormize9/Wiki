
##### Recevoir un fichier d'un hôte

```
---
- hosts: ansiblecli
  remote_user: aftec
  become: true

  tasks: 
  - name: Copy file with owner and permissions
    ansible.builtin.fetch:
      src: text.txt
      dest: /home/aftec/
```