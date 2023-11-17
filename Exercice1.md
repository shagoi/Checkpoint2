
### Q.1.1

Pourquoi le ping avec les adresses IP des machines ne fonctionnent pas ? 
Les deux machines ne sont pas sur le même réseau et le pare feu est activé.

Explique ce que tu as fait et montre le par des copies d'écran
Désactivation du pare feu:
![img](https://github.com/shagoi/donnees/blob/main/supp_parefeu.png?raw=true)

Modification de l'adresse IP:
![img](https://github.com/shagoi/donnees/blob/main/modif_ip.png?raw=true)

Copie d'écran d'un ping fonctionnel:
![img](https://github.com/shagoi/donnees/blob/main/ping.png?raw=true)


### Q.1.3 Modifie la configuration réseau du client pour qu'il soit en DHCP.

Explique pourquoi le client ne récupère pas la 1ère adresse disponible sur la plage DHCP du serveur ?  
Le client obtient la première adresse disponible dans la plage autorisée:
![img](https://github.com/shagoi/donnees/blob/main/plage_dhcp.png?raw=true)

Copie d'écran montrant l'adresse IP prise par le client:
![img](https://github.com/shagoi/donnees/blob/main/ip_client1.png?raw=true)


### Q.1.4 Est-ce que ce client peut avoir l'adresse IP `172.16.10.15` en DHCP ?

Le client peut avoir l'adresse IP `172.16.10.15` en DHCP en lui attribuant par défaut:
![img](https://github.com/shagoi/donnees/blob/main/reservation_dhcp.png?raw=true)

Copie d'écran du résultat de la commande `ipconfig /all` sur le client:
![img](https://github.com/shagoi/donnees/blob/main/ipconfig_all.png?raw=true)
