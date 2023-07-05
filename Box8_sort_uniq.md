## Les commandes `Sort` et `Uniq`

1. Commande `sort` :
   
    La commande `sort` est utilisée pour trier les lignes d'un fichier ou de l'entrée standard. Elle permet de classer les données par ordre alphabétique ou numérique. Voici la syntaxe de base :
    
    ```
    sort options fichier
    ```
    
    - `options` : Les options permettent de personnaliser le comportement de la commande `sort`. Par exemple, `-r` permet de trier en ordre décroissant, `-n` pour un tri numérique, `-u` pour supprimer les doublons, etc.
    
    - `fichier` : Le fichier contenant les données à trier. Si aucun fichier n'est spécifié, `sort` utilise l'entrée standard.
    
    #### Exemple 1 : Tri par ordre alphabétique
      ```
      sort fichier.txt
      ```
          
      Cette commande trie les lignes du fichier `fichier.txt` par ordre alphabétique. Le résultat est affiché à l'écran.
          
    #### Exemple 2 : Tri numérique en ordre décroissant
   
      ```  
      sort -rn fichier.txt
      ```  
      Cette commande trie les lignes du fichier `fichier.txt` par ordre numérique décroissant. Les options `-rn` indiquent à `sort` d'effectuer un tri numérique et d'afficher les résultats dans l'ordre décroissant.

2. Commande `uniq` :
   
    La commande `uniq` est utilisée pour supprimer les lignes consécutives en double dans un fichier ou l'entrée standard. Elle permet de trouver et de filtrer les lignes uniques. Voici la syntaxe de base :
    
    ```
    uniq options fichier
    ```
    
    - `options` : Les options permettent de personnaliser le comportement de la commande `uniq`. Par exemple, `-c` pour compter le nombre d'occurrences de chaque ligne, `-d` pour afficher uniquement les lignes en double, etc.
    
    - `fichier` : Le fichier contenant les données à traiter. Si aucun fichier n'est spécifié, `uniq` utilise l'entrée standard.
    
    #### Exemple 1 : Suppression des doublons
   
          
          uniq fichier.txt
          
      Cette commande supprime les lignes consécutives en double dans le fichier `fichier.txt`. Seule une occurrence de chaque ligne unique est affichée.
          
    #### Exemple 2 : Compter les occurrences des lignes
   
          
          uniq -c fichier.txt
          
     Cette commande compte le nombre d'occurrences de chaque ligne dans le fichier `fichier.txt` et les affiche en préfixant chaque ligne avec son compte.
    
    #### Exemple 3 : Filtrer les lignes en double
          
          uniq -d fichier.txt
          
     Cette commande affiche uniquement les lignes consécutives en double dans le fichier `fichier.txt`.

Vous pouvez combiner les commandes `sort` et `uniq` en utilisant les pipes (`|`) pour obtenir des résultats plus précis. Par exemple, vous pouvez trier les lignes d'un fichier avec `sort` avant de les passer à `uniq` pour supprimer les doublons consécutifs.

Ces exemples vous donnent un aperçu de l'utilisation des commandes `sort` et `uniq`. N'hésitez pas à explorer davantage leurs options et fonctionnalités pour les utiliser de manière plus avancée.
