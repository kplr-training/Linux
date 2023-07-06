## Telnet et Netcat

Telnet et Netcat sont deux utilitaires de communication en ligne de commande utilisés pour établir des connexions réseau et transférer des données. Cependant, ils ne sont pas spécifiquement conçus pour se connecter en SSH, mais plutôt pour d'autres protocoles réseau tels que Telnet et TCP/IP. 

#### 1. Telnet :

   Telnet est un protocole de communication réseau qui permet d'établir des connexions distantes avec un serveur distant. Il est principalement utilisé pour accéder à des systèmes distants et exécuter des commandes à distance. Cependant, il transmet les données en clair, ce qui pose des problèmes de sécurité.

   Syntaxe de base :
   ```
   telnet adresse_ip port
   ```
   Exemple :
   ```
   telnet example.com 23
   ```
   Cette commande se connecte à l'adresse IP du serveur `example.com` sur le port 23 à l'aide du protocole Telnet.

   Remarque : Il est déconseillé d'utiliser Telnet pour les connexions réseau non sécurisées, car les données sont transmises en texte brut et peuvent être interceptées.

#### 2. Netcat (nc) :
   
   Netcat, également connu sous le nom de `nc`, est un utilitaire réseau polyvalent qui permet d'établir des connexions TCP/UDP, d'écouter des ports, de transférer des données, etc. Il peut être utilisé pour effectuer des tâches telles que la redirection de ports, le transfert de fichiers ou même l'établissement de tunnels réseau.

   Syntaxe de base (établissement de connexion) :
   ```
   nc adresse_ip port
   ```
   Exemple :
   ```
   nc example.com 22
   ```
   Cette commande se connecte à l'adresse IP du serveur `example.com` sur le port 22 (port SSH par défaut) à l'aide de Netcat.

   Remarque : L'utilisation de Netcat pour établir une connexion SSH n'est pas recommandée, car il ne fournit pas les mécanismes de sécurité intégrés de SSH, tels que le chiffrement des données.
   
   Pour se connecter en SSH de manière sécurisée, il est recommandé d'utiliser la commande `ssh` qui est spécifiquement conçue pour cela.
