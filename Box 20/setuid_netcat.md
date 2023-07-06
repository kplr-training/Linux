## Le Binaire Setuid et Netcat

Le bit setuid est une permission spéciale utilisée sur les fichiers exécutables sous Linux. Lorsqu'un fichier a le bit setuid activé, il est exécuté avec les privilèges de l'utilisateur propriétaire du fichier, plutôt que les privilèges de l'utilisateur qui l'exécute.

Cela permet d'exécuter le fichier avec des privilèges élevés, même si l'utilisateur n'a pas ces privilèges normalement. Cependant, l'utilisation du setuid peut présenter des risques de sécurité si les fichiers ne sont pas correctement protégés.

- Pour exécuter un binaire setuid avec un port, vous pouvez suivre les étapes suivantes :
  
  1. Assurez-vous que le fichier binaire a le bit setuid activé. Vous pouvez vérifier cela avec la commande `ls -l` et en vérifiant les permissions du fichier.
  2. Utilisez la commande `chmod` pour définir le bit setuid si ce n'est pas déjà fait. Par exemple, `chmod u+s nom_fichier_binaire`.
  3. Exécutez le binaire en spécifiant le port en tant qu'argument de ligne de commande. Par exemple, `./nom_fichier_binaire port`.
      Remplacez "nom_fichier_binaire" par le nom réel du fichier binaire setuid, et "port" par le numéro de port souhaité.

Netcat (nc) est un utilitaire de réseau polyvalent qui peut être utilisé pour lire ou écrire des données sur des connexions réseau. Il peut être utilisé pour créer des connexions TCP ou UDP, envoyer des fichiers ou des commandes sur le réseau, et bien plus encore.

Netcat est souvent utilisé pour des tâches de débogage, de transfert de fichiers ou pour établir des connexions réseau.

- Pour utiliser netcat pour écouter un port, vous pouvez exécuter la commande suivante :
  ```
  nc -l -p port
  ```
  Remplacez "port" par le numéro de port sur lequel vous souhaitez écouter. Netcat démarrera un écouteur sur ce port et attendra les connexions entrantes. Toute donnée reçue sur ce port sera affichée à l'écran.

Il est important de noter que l'utilisation du setuid et de netcat peut présenter des risques de sécurité si elle est mal utilisée. Assurez-vous de comprendre les implications et les bonnes pratiques de sécurité avant d'utiliser ces fonctionnalités.
