## Rot13

Rot13 est un simple algorithme de chiffrement utilisé pour obscurcir un texte en remplaçant chaque lettre par une autre lettre située 13 positions plus loin dans l'alphabet. C'est une forme de chiffrement par substitution monoalphabétique.

En Linux, vous pouvez utiliser la commande `tr` pour appliquer le chiffrement Rot13. Voici la syntaxe de base et des exemples variés :

Syntaxe de base :
```
echo "texte à chiffrer" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

- `echo "texte à chiffrer"` : Cette partie représente le texte que vous souhaitez chiffrer. Vous pouvez remplacer "texte à chiffrer" par le texte de votre choix, en veillant à le mettre entre guillemets.

- `tr 'A-Za-z' 'N-ZA-Mn-za-m'` : Cette partie indique à la commande `tr` de traduire les caractères de l'alphabet anglais de la plage A-Z (majuscules) et a-z (minuscules) vers les caractères de la plage N-ZA-M (majuscules) et n-za-m (minuscules), respectivement. Cela effectue le décalage de 13 positions pour chaque lettre.

Exemples :
1. Chiffrement Rot13 d'un texte :

   ```
   echo "Bonjour, OpenAI!" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
   ```
   Résultat : `Obawbe, BcrnNV!`

2. Déchiffrement Rot13 d'un texte chiffré :

   ```
   echo "Obawbe, BcrnNV!" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
   ```
   Résultat : `Bonjour, OpenAI!`

3. Chiffrement Rot13 d'un fichier texte :

   ```
   tr 'A-Za-z' 'N-ZA-Mn-za-m' < fichier.txt
   ```
   Résultat : le contenu du fichier.txt est affiché avec le chiffrement Rot13 appliqué.

4. Déchiffrement Rot13 d'un fichier texte chiffré :

    ```
   tr 'A-Za-z' 'N-ZA-Mn-za-m' < fichier_chiffre.txt
   ```
   Résultat : le contenu du fichier_chiffre.txt est affiché avec le déchiffrement Rot13 appliqué.

Ces exemples vous montrent comment utiliser la commande `tr` pour appliquer le chiffrement Rot13 à un texte ou à un fichier texte en utilisant la syntaxe de base. Notez que le chiffrement Rot13 est une opération réversible, ce qui signifie que l'application du chiffrement une deuxième fois permet de retrouver le texte d'origine.
