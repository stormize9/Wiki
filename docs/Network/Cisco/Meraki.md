
## Solution wifi Cisco Meraki

### Présentation

L'offre de Meraki se découpe en deux parties : un contrôleur hébergé (Cloud / saas), tableau de bord pour la configuration du système et des équipements physiques (hardware) ce qui fait qu'on qualifie la technologie de Cloud Hybride.

Les points d'accès Meraki fonctionnent de façon dite maillée (Topologie mesh). Ils basculent donc tout seuls de points d'accès à répéteurs si nécessaire en cas de déconnexion du câble RJ45 par exemple. La technologie Mesh permet aussi d'installer du wifi dans un bâtiment sans avoir à câbler chaque borne (en l'absence d'alimentation par POE). La borne principale sera branchée au LAN et l'Internet sera transmis aux autres bornes par répétition du signal de borne à borne. À noter cependant que chaque répétition fait perdre du débit. Dans un déploiement Mesh, il est ainsi recommandé de ne pas répéter plus de trois ou quatre fois le signal afin d'assurer le maintien d'un bon débit Internet..

### Installation

-   Installation des bornes sur switch POE
-   Configurations interfaces switchs
-   Activer DHCP pour que les bornes récupèrent une IP
-   Ouverture des flux vers contrôleur externe si firewall

### Troubleshooting

-   Vérifier si un DHCP n'est pas déjà présent et attribuerai une autre IP aux bornes.