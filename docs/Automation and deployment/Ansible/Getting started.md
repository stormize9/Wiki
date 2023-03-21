
#### Installation 

```
dnf search ansible
sudo dnf install ansible-core
```


---


#### Récupérer données d'un groupe d'hôtes / hôte

```
ansible -m setup ansiblecli | less
```

#### Déployer logiciels

```
ansible tp_ansible --become -m dnf -a "name=httpd"
```

#### Activer le service

```
ansible tp_ansible --become -m systemd -a "name=httpd state=started enabled=true"
```


---