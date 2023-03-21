
##### Télécharger un fichier via une URL

```
---
- hosts: ansiblecli
  remote_user: aftec
  become: true

  tasks: 
  - name: Copy file with owner and permissions
    ansible.builtin.get_url:
      url: https://ftp.drupal.org/files/projects/drupal-8.4.4.tar.gz
      dest: /home/aftec/download_file/
      mode: '0440'
```