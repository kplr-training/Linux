# Gestion des espaces dans le nom du fichier

Lorsque vous travaillez avec des noms de fichiers contenant des espaces, il est important de prendre certaines précautions pour éviter les erreurs ou les problèmes lors de l'utilisation des commandes en ligne. Voici comment gérer les espaces dans les noms de fichiers avec quelques exemples de commandes :

1. Créer un fichier avec un nom contenant des espaces :
   ```
   touch "nom du fichier.txt"
   ```
   Exemple : `touch "mon fichier.txt"`

   En entourant le nom du fichier avec des guillemets doubles, vous pouvez créer un fichier avec un nom contenant des espaces. Dans cet exemple, un fichier nommé "mon fichier.txt" est créé.

2. Afficher le contenu d'un fichier avec un nom contenant des espaces :
   ```
   cat "nom du fichier.txt"
   ```
   Exemple : `cat "mon fichier.txt"`

   La commande "cat" permet d'afficher le contenu d'un fichier. En utilisant des guillemets doubles, vous pouvez spécifier le nom du fichier qui contient des espaces. Dans cet exemple, le contenu du fichier "mon fichier.txt" est affiché.

3. Renommer un fichier avec un nom contenant des espaces :
   ```
   mv "ancien nom.txt" "nouveau nom.txt"
   ```
   Exemple : `mv "mon fichier.txt" "mon nouveau fichier.txt"`

   La commande "mv" est utilisée pour renommer un fichier. En entourant les anciens et nouveaux noms de fichiers avec des guillemets doubles, vous pouvez renommer un fichier qui contient des espaces. Dans cet exemple, le fichier "mon fichier.txt" est renommé en "mon nouveau fichier.txt".

4. Supprimer un fichier avec un nom contenant des espaces :
   ```
   rm "nom du fichier.txt"
   ```
   Exemple : `rm "mon fichier.txt"`

   La commande "rm" permet de supprimer un fichier. En utilisant des guillemets doubles, vous pouvez spécifier le nom du fichier qui contient des espaces. Dans cet exemple, le fichier "mon fichier.txt" est supprimé.

5. Copier un fichier avec un nom contenant des espaces :
   ```
   cp "nom du fichier.txt" destination/
   ```
   Exemple : `cp "mon fichier.txt" dossier/`

   La commande "cp" est utilisée pour copier un fichier. En utilisant des guillemets doubles, vous pouvez spécifier le nom du fichier qui contient des espaces. Dans cet exemple, le fichier "mon fichier.txt" est copié dans le dossier spécifié.

Assurez-vous d'utiliser des guillemets doubles autour des noms de fichiers contenant des espaces pour éviter toute confusion avec les caractères spéciaux ou les séparateurs utilisés par les commandes en ligne.
