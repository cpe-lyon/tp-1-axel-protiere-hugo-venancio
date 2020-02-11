# TP 1. Installation d’Ubuntu Server et priseen main du shell

## Exercice 2. Prise en main de l’interpréteur de commandes

### Manuel

1. `man which` which retourne le chemin du fichier associé à l'execution d'une commande

2. il faut saisir `/<MonMotAChercher>`

3. il faut appuyer sur q pour quitter le manuel

4. `man 6 <comande>`Cette section parle de jeux


### Navigation dans l'arborescence des fichiers

1. `cd /var/log`
2. `cd ..`
3. `cd ~`
4. revenez au dossier précédent (/var) sans utiliser de chemin
`cd ..`
5. essayez d’accéder au dossier /root ; que se passe-t-il ?
cd /root → Permission denied
6. `sudo cd /root`  Command not found
cd est une commande interne au shell. On ne peut utiliser sudo sur les commandes internes. 
7. 
```
cd ~
mkdir Dossier1 & mkdir Dossier2
cd Dossier1 & mkdir Fichier1
cd ..
cd Dossier2
mkdir Dossier2.1 & mkdir Dossier2.2
cd Dossier2.2 & mkdir Fichier2 & mkdir Fichier3
```
8. Fichier1 est correctement suprimé, mais erreur pour Dossier1 car c’est un dossier
9. `rmdir Dossier1`
10. Dossier2 n’est pas vide
11. il faut utiliser `rm -rf Dossier2`


### Commandes importantes

1. `date` permet d'afficher la date et l'heure  
`date "+%H:%M:%S` si on veut seulement l'heure  
2. `time` execute un programme donné et affiche des informations sur les ressources utilisées   
3. `which ls`  
le programme ls est situé dans usr/bin/ls
4. Il n'existe pas d'entrée de manuel pour cette commande  
`alias ll =  'ls -alF'`  
`ls` sert à afficher tous les fichiers du répertoire  
`-a` pour afficher aussi les fichiers cachés  
`-l` pour afficher les détails  
`-F` ajoute un caractère à chaque nom de fichier pour indiquer son type  
5. `ls /bin`  
6. `ls ..` permet d'afficher les fichiers du répertoire précédent (chemin relatif)  
7. `pwd`
8. `echo ‘yo’ > plop` → ecrit “yo” dans le fichier plop (remplacer)
9. `echo ‘yo’ >> plop` → ecrit “yo” dans le fichier plop (écrire à la suite)
10. `file` determine le type de fichier
11. Le fichier titi possède le même contenu que le fichier toto, même quand ce dernier est mis à jour. En revanche, si on supprime toto, titi n'est pas supprimé
12. Les deux fichiers sont liés, changer le contenu de l'un change le contenu de l'autre.  
Si on supprime le fichier de base, le deuxième fichier (anciennement lié) n'existe plus, mais le lien est encore présent. Le fichier apparait en rouge dans `ls`
13. CTRL + S → Stopper  
CTR + Q → Reprendre  
14. `head -5 <file>`  `tail -n 5 <file>`  `head -20 <file> | tail -n 10 `
15. Less : Lire un fichier page par page, dmesg : afficher les logs (messages) du noyau
`dmesg | less` affiche donc les messages du noyau page par page
16. Le fichier `/etc/passwd` stocke les informations essentielles requises lors de la connexion. 
`man 5 passwd` permet d'afficher la page manuel de ce fichier
17. `cut -c1 /etc/passwd | sort -r`
18. `getent passwd | wc -l`
20. `find -name "passwd"`
21. `find -name "passwd" > list_passwd_files.txt 2>/dev/null
22. 
23. `sudo apt install mlocate`  
`locate history.log`
24. Non, locate ne trouve pas le fichier
