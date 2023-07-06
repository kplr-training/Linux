## Scripting

Le scripting en Linux fait référence à la création et à l'exécution de scripts, qui sont des fichiers contenant une série de commandes et d'instructions, généralement écrits dans un langage de script comme Bash, Python, Perl, Ruby, etc. Les scripts permettent d'automatiser des tâches récurrentes, de traiter des données, de configurer le système et d'effectuer diverses opérations.

Voici les étapes de base pour créer et exécuter un script en Linux :

1. **Création d'un fichier de script** :
   - Ouvrez un éditeur de texte tel que Vim, Nano ou Gedit.
   - Créez un nouveau fichier et donnez-lui une extension appropriée (par exemple, .sh pour les scripts Bash).
   - Écrivez vos commandes et instructions dans le fichier, en suivant la syntaxe appropriée du langage de script choisi.

2. **Ajout des permissions d'exécution** :
   - Pour pouvoir exécuter le script, vous devez lui donner les permissions d'exécution.
   - Utilisez la commande `chmod` pour ajouter les permissions d'exécution au fichier de script. Par exemple :
     ```
     chmod +x nom_script.sh
     ```

3. **Exécution du script** :
   - Pour exécuter un script, utilisez la commande suivie du nom du fichier de script. Par exemple :
     ```
     ./nom_script.sh
     ```

Syntaxe des commandes de base dans un script :

- Commentaires : Les commentaires dans un script sont précédés par le caractère `#` et sont utilisés pour fournir des informations sur le script. Par exemple :
  ```bash
  # Ceci est un commentaire expliquant le script
  ```

- Variables : Les variables sont utilisées pour stocker des valeurs et peuvent être utilisées dans les commandes du script. Par exemple :
  ```bash
  nom="John"
  age=25
  echo "Bonjour, je m'appelle $nom et j'ai $age ans."
  ```

- Commandes conditionnelles : Les commandes conditionnelles sont utilisées pour effectuer des actions basées sur une condition. Par exemple :
  ```bash
  if [ $age -gt 18 ]; then
    echo "Vous êtes majeur."
  else
    echo "Vous êtes mineur."
  fi
  ```

- Boucles : Les boucles sont utilisées pour répéter des instructions. Par exemple :
  ```bash
  for i in 1 2 3; do
    echo "Valeur : $i"
  done
  ```

Ces exemples sont basés sur le langage de script Bash, mais la syntaxe peut varier selon le langage de script utilisé. 
