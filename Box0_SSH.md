# SSH : Secure Shell ou Secure Socket Shell

- `SSH` est un protocole de communication sécurisé utilisé pour établir des connexions sécurisées et chiffrées entre des ordinateurs distants. Il permet d'accéder et de contrôler des systèmes à distance de manière sécurisée sur des réseaux non sécurisés tels qu'Internet.

- SSH fournit un moyen sûr d'authentifier les utilisateurs par mot de passe et par clé publique, de transférer des données de manière cryptée et d'exécuter des commandes à distance. Il offre également des fonctionnalités avancées telles que le transfert de fichiers sécurisé (SFTP) et le tunneling de ports, permettant d'acheminer le trafic réseau à travers des connexions chiffrées.

- Lorsque vous vous connectez à un serveur distant via SSH, toutes les communications entre votre ordinateur local et le serveur distant sont cryptées. Cela protège vos informations sensibles, telles que les noms d'utilisateur, les mots de passe et les données transférées, contre les interceptions et les attaques.

- Pour établir une connexion SSH, vous avez besoin d'un client SSH sur votre ordinateur local et d'un serveur SSH sur l'ordinateur distant. Les systèmes d'exploitation Unix et Linux ont généralement un client SSH intégré en ligne de commande, appelé "ssh", tandis que les systèmes Windows peuvent utiliser des clients SSH tiers tels que PuTTY ou OpenSSH.

- Lorsque vous vous connectez à un serveur distant via SSH, vous devez fournir vos informations d'identification, telles que le nom d'utilisateur et le mot de passe. Une fois authentifié, vous pouvez exécuter des commandes à distance, transférer des fichiers, modifier des configurations et effectuer diverses tâches sur le serveur distant, en fonction de vos autorisations.


## Les commandes de base de SSH: 

Voici quelques commandes de base pour utiliser SSH avec des exemples :

1. Pour se connecter à un serveur distant via SSH :
   ```
   ssh utilisateur@adresse_ip
   ```
   Exemple : `ssh john@192.168.0.100`

   Cette commande établit une connexion SSH avec le serveur distant en utilisant le nom d'utilisateur "utilisateur" et l'adresse IP "adresse_ip". Vous serez invité à saisir le mot de passe de l'utilisateur pour vous authentifier.

3. Pour se connecter avec un port spécifique :
   ```
   ssh -p port utilisateur@adresse_ip
   ```
   Si le serveur distant utilise un port SSH différent de celui par défaut (port 22), vous pouvez spécifier le port avec l'option `-p`. Dans cet exemple, la connexion SSH est établie sur le port 2222.
   
   Exemple : `ssh -p 2222 john@192.168.0.100`


5. Vous pouvez également utiliser une clé privée pour l'authentification :
   ```
   ssh -i chemin_vers_la_clé_privée utilisateur@adresse_ip
   ```
   Exemple : `ssh -i ~/.ssh/id_rsa john@192.168.0.100`

   Si vous utilisez une authentification basée sur une clé publique/privée, vous pouvez spécifier le chemin vers la clé privée avec l'option `-i`. Dans cet exemple, la connexion SSH utilise la clé privée `id_rsa` située dans le répertoire `~/.ssh/` de l'utilisateur.

6. Exécuter une commande à distance via SSH :
   ```
   ssh utilisateur@adresse_ip "commande"
   ```
   Exemple : `ssh john@192.168.0.100 "ls -l"`

   Vous pouvez exécuter une commande à distance sur le serveur distant sans ouvrir une session interactive. Dans cet exemple, la commande `ls -l` est exécutée sur le serveur distant, affichant les détails des fichiers et répertoires.

7. Transférer des fichiers via SSH (SCP) :
   ```
   scp fichier_local utilisateur@adresse_ip:chemin_distant
   ```
   Exemple : `scp fichier.txt john@192.168.0.100:/home/john/`

   La commande SCP (Secure Copy) vous permet de transférer des fichiers entre votre ordinateur local et le serveur distant via SSH. Dans cet exemple, le fichier `fichier.txt` est copié depuis votre ordinateur local vers le répertoire `/home/john/` sur le serveur distant.

Ces commandes de base vous permettront de vous connecter, d'exécuter des commandes à distance et de transférer des fichiers en utilisant SSH. N'oubliez pas de remplacer "utilisateur" par votre nom d'utilisateur, "adresse_ip" par l'adresse IP du serveur distant et d'adapter les chemins et noms de fichiers selon vos besoins.

