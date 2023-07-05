## Public and Private keys

Les clés publiques et privées sont utilisées dans le cadre de la cryptographie à clé asymétrique pour sécuriser les communications et les connexions. En Linux, elles sont couramment utilisées pour se connecter en SSH de manière sécurisée.

Voici une explication détaillée sur les clés publiques et privées en Linux, ainsi que leur utilisation pour la connexion SSH :

1. Clé publique :

   Une clé publique est une partie d'une paire de clés asymétriques. Elle est destinée à être partagée publiquement, d'où son nom. La clé publique peut être utilisée pour chiffrer les données ou vérifier la signature numérique créée avec la clé privée correspondante. La clé publique est généralement stockée dans un fichier avec une extension `.pub`.

2. Clé privée :

   Une clé privée est l'autre partie de la paire de clés asymétriques. Contrairement à la clé publique, elle doit être gardée secrète et protégée. La clé privée est utilisée pour déchiffrer les données chiffrées avec la clé publique correspondante ou pour créer des signatures numériques. La clé privée est généralement stockée dans un fichier sans extension spécifique.

3. Génération de clés SSH :

   Pour utiliser les clés publiques et privées pour se connecter en SSH, vous devez générer une paire de clés. Vous pouvez le faire en utilisant la commande `ssh-keygen` avec la syntaxe suivante :
   ```
   ssh-keygen -t rsa -b 4096 -f chemin/clé
   ```
   Exemple : `ssh-keygen -t rsa -b 4096 -f ~/.ssh/id_rsa`
   
   Cette commande génère une paire de clés RSA avec une taille de 4096 bits et les stocke dans les fichiers `id_rsa` (clé privée) et `id_rsa.pub` (clé publique) dans le répertoire `~/.ssh/`.

4. Utilisation des clés SSH pour se connecter :

   Une fois que vous avez généré la paire de clés, vous pouvez utiliser la clé publique pour vous connecter à un serveur distant via SSH. Pour cela, vous devez ajouter votre clé publique au fichier `authorized_keys` sur le serveur distant. Vous pouvez le faire manuellement en copiant le contenu de la clé publique (`id_rsa.pub`) et en le collant dans le fichier `~/.ssh/authorized_keys` sur le serveur distant. Vous pouvez également utiliser la commande `ssh-copy-id` pour copier automatiquement votre clé publique sur le serveur distant :
   ```
   ssh-copy-id utilisateur@serveur
   ```
   Exemple : `ssh-copy-id user@example.com`
   
   Cette commande copie la clé publique de l'utilisateur local sur le serveur distant et l'ajoute au fichier `~/.ssh/authorized_keys` du compte utilisateur distant.

5. Connexion en SSH avec les clés :

   Une fois que votre clé publique est configurée sur le serveur distant, vous pouvez vous connecter en utilisant la clé privée correspondante. Utilisez la commande `ssh` avec l'option `-i` pour spécifier le chemin de la clé privée :
   ```
   ssh -i chemin/clé_privée utilisateur@serveur
   ```
   Exemple : `ssh -i ~/.ssh/id_rsa user@example.com`
   
   Cette commande se connecte au serveur distant en utilisant la clé privée `id_rsa` pour l'utilisateur spécifié.

En utilisant ces étapes, vous pouvez générer une paire de clés SSH, configurer la clé publique sur le serveur distant et vous connecter en utilisant la clé privée correspondante. Assurez-vous de protéger votre clé privée et de prendre des mesures de sécurité appropriées pour éviter tout accès non autorisé.
