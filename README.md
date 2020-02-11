# tp-1-axel-protiere-hugo-venancio

## Exercice 2. Prise en main de l’interpréteur de commandes

### Manuel

1. `man which` which retourne le chemin du fichier associé à l'execution d'une commande

2. il faut saisir `/<MonMotAChercher>`

3. 
il faut appuyer sur q pour quitter le manuel

4. `man 6 <comande>`Cette section parle de jeux


### Navigation dans l'arborescence des fichiers

1. `cd /var/log`
2. `cd ..`
3. `cd ~`
4. revenez au dossier précédent (/var) sans utiliser de chemin
`cd ..`
5. essayez d’accéder au dossier /root ; que se passe-t-il ?
cd /root → Permission denied
6.`sudo cd /root` → Command not found
cd est une commande interne au shell. On ne peut utiliser sudo sur les commandes internes.



### Commandes importantes

1. `date` permet d'afficher la date et l'heure
`date "+%H:%M:%S` si on veut seulement l'heure
2. `time` execute un programme donné et affiche des informations sur les ressources utilisées 
3. `which ls` 
le programme ls est situé dans usr/bin/ls
4. Il n'existe pas d'entrée de manuel pour cette commande
`alias ll =  'ls -alF'`\n
`man ls` 

