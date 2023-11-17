
**Q.3.1** Quel est le matériel réseau **A** ?  
Quel est son rôle sur ce schéma vis-à-vis des ordinateurs ?
C'est un switch, il permet aux différents ordinateurs de communiquer entre eux.

**Q.3.2** Quel est le matériel réseau **B** ?  
Quel est son rôle pour le réseau **10.10.0.0/16** ?
C'est un routeur, il permet à ce réseau de communiquer avec les réseaux 10.12.2.0/24 et 172.16.5.0/24

**Q.3.3** Que signifie **f0/0** et **g1/0** sur l’élément **B** ?
Ce sont les ports du routeur  f0/0 en FastEthernet et g1/0 en GigabitEthernet

**Q.3.4** Pour l'ordinateur **PC2**, que représente `/16` dans son adresse IP ?
C'est son CIDR avec un en 255.255.0.0

**Q.3.5** Pour ce même ordinateur, que représente l'adresse `10.10.255.254` ?
Elle représente la dernière adresse disponible


### [](https://odyssey.wildcodeschool.com/quests/2902#c-etude-th%C3%A9orique)c. Etude théorique

**Q.3.6** Pour les ordinateur PC1, PC2, et PC5 donne :

| PC | L'adresse de réseau | La première adresse disponible | La dernière adresse disponible | L'adresse de diffusion |
| --- | --- | --- | --- | --- |
| PC1 | 10.10.0.0 | 10.10.0.1 | 10.10.255.254 | 10.10.255.255 |
| PC2 | 10.11.0.0 | 10.11.0.1 | 10.11.255.254 | 10.11.255.255 |
| PC5 | 10.10.0.0 | 10.10.0.1 | 10.11.255.254 | 10.11.255.255 |

**Q.3.7** En t'aidant des informations que tu as fourni à la question 3.6, et à l'aide de tes connaissances, indique parmi tous les ordinateurs du schéma, lesquels vont pouvoir communiquer entre-eux.
Les PC 1,3 et 4 entre eux.
Les PC 2 et 5 entre eux.

**Q.3.8** De même, indique ceux qui vont pouvoir atteindre le réseau `172.16.5.0/24`.


**Q.3.9** Quel incidence y-a-t'il pour les ordinateurs PC2 et PC3 si on interverti leur ports de connexion sur le matériel **A** ?
Cela produirait des problèmes de connexion pour ces postes.

**Q.3.10** On souhaite mettre la configuration IP des ordinateurs en dynamique. Quelles sont les modifications possible ?
Il faut mettre en place un serveur DHCP dédié.

### [](https://odyssey.wildcodeschool.com/quests/2902#d-analyse-de-trames)d. Analyse de trames

**Fichier 1** :

**Q.3.11** Sur le paquet N°5, quelle est l'adresse mac du matériel qui initialise la communication ? Déduis-en le nom du matériel.
L'adresse mac est : 00:50:79:66:68:00 et c'est le PC1 qui initie la communication

**Q.3.12** Est-ce que la communication enregistrée dans cette capture a réussi ? Si oui, indique entre quels matériel, si non indique pourquoi cela n'a pas fonctionné.
Oui elle a fonctionné entre PC4 et PC1

**Q.3.13** Dans cette capture, à quel matériel correspond le **request** et le **reply** ? Donne le nom, l'adresse IP, et l'adresse mac de chaque materiel.
Le request vient de PC1, 10.10.4.1 , 00:50:79:66:68:00
Le reply vient de PC4, 10.10.4.2 , 00:50:79:66:68:03

**Q.3.14** Dans le paquet N°2, quel est le protocole encapsulé ? Quel est son rôle ?
C'est un protocole ARP qui fait correspondre une adresse mac et une adresse IP

**Q.3.15** Quels ont été les rôles des matériels **A** et **B** dans cette communication ?
Le switch A permet avec une adresse MAC (couche2) d'aller vers le routeur B en adresse IP (couche3)


**Fichier 2** :

**Q.3.16** Dans cette trame, qui initialise la communication ? Donne l'adresse IP ainsi que le nom du matériel.
C'est le PC3 10.10.80.3 qui initie la communication.

**Q.3.17** Quel est le protocole encapsulé ? Quel est son rôle ?
C'est le protocole ICMP qui permet la communication sur un réseau

**Q.3.18** Est-ce que cette communication a réussi ? Si oui, indique entre quels matériel, si non indique pourquoi cela n'a pas fonctionné.
Non il n'y a pas de réponse parce que l'hôte est inaccessible.

**Q.3.19** Explique la ligne du paquet N° 2
C'est la réponse à la requête du ping avec l'information de l'hôte inaccessible

**Q.3.20** Quels ont été les rôles des matériels **A** et **B** ?
Le switch A permet d'aller vers le routeur B qui ne permet pas le passage vers le réseau du PC2 et renvoi une réponse du port 10.10.255.254

**Fichier 3** :

**Q.3.21** Dans cette trame, donne les noms et les adresses IP des matériels sources et destination.
Adresses IP source : 10.10.4.2
Adresses IP destination : 172.16.5.253

**Q.3.22** Quelles sont les adresses mac source et destination ? Qu'en déduis-tu ?
Adresses MAC source : ca:01:da:d2:00:1c
Adresses MAC destination : ca:03:9e:ef:00:38
J'en déduis que la route a été tracée entre ces réseaux.

**Q.3.23** A quel emplacement du réseau a été enregistré cette communication ?
Il a été enregistré sur le réseau 172.16.5.0


