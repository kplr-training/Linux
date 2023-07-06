## Les permissions sous Linux : `setuid`

Les permissions sous Linux contrôlent l'accès aux fichiers et répertoires. Elles permettent de définir qui peut lire, écrire et exécuter ces fichiers, ainsi que les actions spécifiques autorisées pour les utilisateurs, les groupes et les autres.

Les permissions sont généralement représentées par une série de caractères affichés lorsque vous exécutez la commande `ls -l` pour afficher le contenu d'un répertoire. Voici un exemple de sortie de la commande `ls -l` :

```
-rwxr-xr-x 1 utilisateur groupe 4096 déc 1 12:34 fichier
```

Dans cet exemple, les permissions sont représentées par les caractères `-rwxr-xr-x`. Voici une explication détaillée de ces caractères :

- Le premier caractère (`-`) indique le type de fichier. Dans cet exemple, il s'agit d'un fichier régulier. D'autres valeurs possibles sont `d` pour les répertoires, `l` pour les liens symboliques, `c` pour les fichiers caractères et `b` pour les fichiers blocs.

- Les neuf caractères suivants sont divisés en trois groupes de trois. Chaque groupe représente les permissions pour l'utilisateur propriétaire, le groupe et les autres utilisateurs respectivement. Les permissions possibles sont :

  - `r` (read) : Permet la lecture du fichier ou la liste du contenu du répertoire.
  - `w` (write) : Permet la modification ou la suppression du fichier, ainsi que la création, la suppression ou la modification du contenu du répertoire.
  - `x` (execute) : Permet l'exécution du fichier ou la recherche (accès) du répertoire.

Voici quelques exemples de commandes couramment utilisées pour gérer les permissions :

- `chmod` : Utilisée pour modifier les permissions d'un fichier ou d'un répertoire. Voici la syntaxe générale :
  ```
  chmod [options] permissions fichier_ou_répertoire
  ```

- `chown` : Utilisée pour changer le propriétaire et/ou le groupe d'un fichier ou d'un répertoire. Voici la syntaxe générale :
  ```
  chown [options] propriétaire:fichier_ou_groupe fichier_ou_répertoire
  ```

- `chgrp` : Utilisée pour changer le groupe d'un fichier ou d'un répertoire. Voici la syntaxe générale :
  ```
  chgrp [options] groupe fichier_ou_répertoire
  ```
### SETUID

Les fichiers setuid sont des fichiers exécutables qui ont un bit spécial activé. Lorsque le bit setuid est activé, le programme est exécuté avec les permissions du propriétaire du fichier au lieu des permissions de l'utilisateur exécutant le programme. Cela permet à un utilisateur d'exécuter un programme avec des privilèges spécifiques, généralement pour effectuer des tâches administratives restreintes.

Pour activer le bit setuid, vous pouvez utiliser la commande `chmod` avec l'option `u+s`. Par exemple :
```
chmod u+s fichier
```

Pour désactiver le bit setuid, vous pouvez utiliser l'option `u-s`. Par exemple :
```
chmod u-s fichier
```

Il est important de noter que l'utilisation du bit setuid doit être effectuée avec attention et prudence, car cela peut présenter des risques de sécurité si les fichiers setuid ne sont pas correctement protégés. 
