## Netcat

Netcat, également connu sous le nom de "nc", est un outil polyvalent utilisé pour la communication réseau sous Linux. Il peut agir à la fois comme un client et un serveur, permettant d'établir des connexions TCP ou UDP, d'envoyer et de recevoir des données sur des ports spécifiques, et d'effectuer diverses opérations réseau.

Syntaxe des commandes de base avec Netcat :

1. **Créer un serveur TCP** :
   ```
   nc -l -p <port>
   ```
   Cette commande lance un serveur Netcat en mode écoute sur le port spécifié. Toutes les connexions entrantes sur ce port seront gérées par Netcat.

2. **Créer un client TCP** :
   ```
   nc <adresse_ip> <port>
   ```
   Cette commande permet de se connecter à un serveur distant en spécifiant l'adresse IP et le port. Netcat établira une connexion TCP avec le serveur.

3. **Créer un serveur UDP** :
   ```
   nc -u -l -p <port>
   ```
   Cette commande lance un serveur Netcat en mode écoute sur le port spécifié en utilisant le protocole UDP.

4. **Créer un client UDP** :
   ```
   nc -u <adresse_ip> <port>
   ```
   Cette commande permet de se connecter à un serveur distant en utilisant le protocole UDP.

5. **Transférer un fichier** :
   ```
   nc -w 3 <adresse_ip> <port> < fichier
   ```
   Cette commande envoie un fichier à un serveur distant en spécifiant l'adresse IP et le port. Le fichier est transmis via la connexion TCP.

6. **Lire les données d'un port** :
   ```
   nc -l -p <port>
   ```
   Cette commande permet de lire les données entrantes sur un port spécifique. Utile pour recevoir des données envoyées par un autre programme ou un autre serveur.

Ces exemples illustrent quelques utilisations courantes de Netcat. Il est important de noter que Netcat est un outil puissant et peut être utilisé de diverses manières pour la communication réseau et le transfert de données. 
