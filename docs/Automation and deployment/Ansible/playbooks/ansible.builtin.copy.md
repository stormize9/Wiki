

##### Envoyer fichier vers hôte

```
---
- hosts: ansiblecli
  remote_user: aftec
  become: true

  tasks: 
  - name: Copy file with owner and permissions
    ansible.builtin.copy:
      src: text.txt
      dest: /home/aftec/
      owner: aftec
      mode: '0644'
```

##### Envoyer données vers un fichier hôte

```
---
- hosts: ansiblesrv
  remote_user: aftec
  become: true

  tasks: 
  - name: Copy file with owner and permissions
    ansible.builtin.copy:
      dest: /home/aftec/text.txt
      owner: aftec
      mode: '0644'
      content: "Je suis un fichier de test
      Je suis déployé sur le serveur {{ inventory_hostname }}"
```