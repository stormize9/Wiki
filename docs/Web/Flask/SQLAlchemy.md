
##### Mettre à jour la bdd :

Modification / Suppression des attributs existants :

```
- Stopper le serveur
```

```
- Suppression du fichier db.db et du dossier migrations
```

Puis rentrer les commandes suivantes en CLI :

```
flask db init
flask db migrate -m "Initial migration."
flask db upgrade
```

Ajout d'un attribut :

```
flask db stamp head
flask db migrate
flask db upgrade
```