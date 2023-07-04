## Dashed Filename

**Note préliminaire : Il est important de noter que l'utilisation de noms de fichiers commençant par un tiret ("-") peut entraîner des problèmes et des erreurs avec certaines commandes Unix/Linux, car elles peuvent interpréter le nom de fichier comme une option de ligne de commande.**

Dans les systèmes d'exploitation Unix ou Linux, travailler avec des noms de fichier contenant un tiret nécessite une certaine attention. Dans certains cas, vous devrez manipuler des fichiers commençant par un tiret (-) en tant que premier caractère.En effet, le tiret (-) est généralement utilisé par les commandes pour spécifier des options et des arguments.

Dans ce guide, nous vous montrerons comment créer, supprimer, répertorier, lire et copier des fichiers dont le nom commence par un tiret (-).

### 1. Créer un nom de fichier commençant par un tiret
   
Généralement, la commande "touch" est utilisée pour créer un fichier vide dans les systèmes d'exploitation Linux. Cependant, lorsque vous essayez de créer un fichier vide qui commence par un tiret (-), vous ne pouvez pas le créer.

Prenons un exemple pour mieux comprendre.
```
touch -
```

**La commande ci-dessus a réussi, mais le fichier n'est pas créé.**

Prenons un autre exemple :
```
touch -filename
```

Vous devriez voir l'erreur suivante :

```
touch: option invalide -- 'i'
Essayez 'touch --help' pour plus d'informations.
```

**Vous devrez passer un argument spécial, "--", avant le fichier commençant par un tiret (-) pour résoudre ce problème.**
```
touch -- -filename
```

Maintenant, le fichier est bien créé sous le nom `-filename`

### 2. Supprimer un nom de fichier commençant par un tiret

Vous devrez également spécifier l'argument "--" avant le fichier commençant par un tiret (-) pour supprimer le fichier.Si vous ne le faites pas, vous devriez obtenir l'erreur suivante :
```
rm: option invalide -- 'l'
Essayez 'rm ./-filename' pour supprimer le fichier '-filename'.
Essayez 'rm --help' pour plus d'informations.
```

Maintenant, essayez de supprimer le fichier en passant l'argument "--" :
```
rm -rf -- -filename
```
Cela devrait réussir.

### 3. Ouvrir et lire un nom de fichier commençant par un tiret
Imaginez que vous avez un fichier  dont le nom commence par un tiret qui contient le message `Salut, comment ça va ?`.
Si vous essayez de lire le fichie avec la commande "cat", Vous devriez certainement obtenir une erreur :
```
cat: option invalide -- 'f'
Essayez 'cat --help' pour plus d'informations.
```

Dans ce cas, vous devrez spécifier l'option "<" avant le fichier commençant par un tiret (-).
```
cat < -filename
```
Vous devriez obtenir la sortie suivante :
```
Salut, comment ça va ?
```
Vous pouvez également utiliser l'option "./" avant le fichier commençant par un tiret (-) pour afficher le contenu du fichier :
```
cat ./-filename
```

### 4. Copier un nom de fichier commençant par un tiret

Vous devrez également spécifier l'option "--" avant le fichier commençant par un tiret pour le copier ou le déplacer.
```
cp -- -filename /opt
```
### 5. Lister les informations du fichier dont le nom commençant par un tiret

Pour ce faire, vous utilisez l'option "--" avant le fichier commençant par un tiret pour répertorier le fichier "-filename" :
```
ls -l -- -filename
```
Vous devriez voir une sortie similaire à la suivante :
```
-rw-rw-r-- 1 vyom vyom 0 23 oct 15:55 -filename
```

Dans le guide ci-dessus, vous avez appris comment créer, supprimer, répertorier et lire un fichier dont le nom commence par un tiret. Nous espérons que vous avez maintenant suffisamment de connaissances pour gérer les fichiers commençant par un tiret.
