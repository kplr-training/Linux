## La commande `Nmap`

Nmap (Network Mapper) est un outil open source utilisé pour l'exploration et la sécurisation des réseaux. Il permet d'analyser les hôtes et les services réseau, de découvrir les ports ouverts, d'identifier les systèmes d'exploitation, et bien plus encore. Nmap est largement utilisé par les administrateurs réseau, les pentesteurs et les professionnels de la sécurité pour évaluer la sécurité des réseaux.


Voici la syntaxe de base de la commande Nmap :

```
nmap [options] <cible>
```

Les options permettent de configurer le comportement de l'outil et de spécifier les types de scan à effectuer. Voici quelques options couramment utilisées :

- `-p`: Spécifie les ports à scanner. Par exemple, `-p 80,443` scanne les ports 80 et 443.
- `-sS`: Effectue un scan TCP SYN (scan de ports par défaut).
- `-sU`: Effectue un scan UDP.
- `-O`: Active la détection du système d'exploitation.
- `-v`: Active le mode verbeux pour afficher plus d'informations.
- `-A`: Active l'option de détection des services et de la version du logiciel.
- `-T<0-5>`: Définit le niveau d'agressivité du scan (de 0 à 5).

Voici quelques exemples d'utilisation de la commande Nmap :

1. Scan des ports TCP les plus courants sur une machine :

   ```
   nmap <cible>
   ```

   Par exemple :
   ```
   nmap 192.168.1.100
   ```

2. Scan de tous les ports sur une machine :

   ```
   nmap -p- <cible>
   ```

   Par exemple :
   ```
   nmap -p- 192.168.1.100
   ```

3. Scan d'une plage de ports spécifique :

   ```
   nmap -p <port_range> <cible>
   ```

   Par exemple :
   ```
   nmap -p 1-1000 192.168.1.100
   ```

4. Scan des ports UDP :

   ```
   nmap -sU <cible>
   ```

   Par exemple :
   ```
   nmap -sU 192.168.1.100
   ```

5. Détection du système d'exploitation :

   ```
   nmap -O <cible>
   ```

   Par exemple :
   ```
   nmap -O 192.168.1.100
   ```

6. Scan avec détection des services et de la version :

   ```
   nmap -A <cible>
   ```

   Par exemple :
   ```
   nmap -A 192.168.1.100
   ```

7. Scan rapide avec mode verbeux :

   ```
   nmap -v <cible>
   ```

   Par exemple :
   ```
   nmap -v 192.168.1.100
   ```

Ces exemples couvrent seulement quelques cas d'utilisation de Nmap. L'outil offre une multitude d'options et de fonctionnalités pour l'exploration et l'analyse des réseaux. Il est recommandé de consulter la documentation officielle de Nmap pour en savoir plus sur ses fonctionnalités avancées et ses options spécifiques.
