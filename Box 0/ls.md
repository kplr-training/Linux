# La commande `LS`

La commande `ls` est une commande couramment utilisée dans les systèmes d'exploitation Unix et Linux pour lister le contenu d'un répertoire. Elle affiche les fichiers, les répertoires et d'autres informations sur les éléments présents dans le répertoire spécifié ou dans le répertoire de travail actuel.

La syntaxe de base de la commande `ls` est la suivante:
```
ls [options] [répertoire]
```

Voici quelques options couramment utilisées avec la commande "ls" :

- `-l` : Affiche les détails des fichiers et répertoires sous forme de liste, avec des informations telles que les autorisations, le propriétaire, la taille, la date de modification, etc.
- `-a` : Affiche tous les fichiers, y compris les fichiers cachés (ceux dont le nom commence par un point).
- `-h` : Affiche les tailles des fichiers de manière lisible par l'homme, en utilisant des unités de taille (Ko, Mo, Go, etc.) plutôt que des octets.
- `-r` : Trie les fichiers en ordre inverse.
- `-t` : Trie les fichiers par date de modification, affichant les plus récents en premier.
- `-R` : Liste récursivement les fichiers et répertoires dans tous les sous-répertoires.

## Exemples d'utilisation :

1. Afficher le contenu du répertoire de travail actuel :
   ```
   ls
   ```

2. Afficher le contenu d'un répertoire spécifique :
   ```
   ls /chemin/vers/repertoire
   ```

3. Afficher le contenu avec des détails :
   ```
   ls -l
   ```

4. Afficher tous les fichiers, y compris les fichiers cachés :
   ```
   ls -a
   ```

5. Afficher les fichiers triés par date de modification :
   ```
   ls -t
   ```

6. Afficher les fichiers triés par ordre inverse :
   ```
   ls -r
   ```

7. Afficher les tailles des fichiers de manière lisible par l'homme :
   ```
   ls -h
   ```

8. Afficher récursivement le contenu de tous les sous-répertoires :
   ```
   ls -R
   ```

Ce ne sont que quelques exemples d'utilisation de la commande "ls". Il existe de nombreuses autres options disponibles pour personnaliser la sortie en fonction de vos besoins. Vous pouvez consulter la page de manuel de "ls" en utilisant la commande `man ls` pour obtenir plus d'informations sur ses fonctionnalités et options.

## Documentation

https://man7.org/linux/man-pages/man1/ls.1.html

https://fr.wikipedia.org/wiki/Ls
