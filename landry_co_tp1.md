# Exercice 2. Prise en main de l’interpréteur de commandes

## :closed_book: Manuel

1. _A l’aide du manuel, identifiez le rôle de la commande which_<br>
La commande `which` permet de localiser une commande.

2. _Quand on consulte cette page, comment peut-on rechercher, par exemple, le mot option ?_<br>
L'option `-k` peut-être utilisé dans la command `man` afin de rechercher un mot clé. Par exemple `man -k option`.
Voici le retour :
```
btrfs (5)            - topics about the BTRFS filesystem (mount options, supported file attributes and other)
dhcp-options (5)     - Dynamic Host Configuration Protocol options
getopt (1)           - parse command options (enhanced)
git-config (1)       - Get and set repository or global options
git-hash-object (1)  - Compute object ID and optionally creates a blob from a file
grog (1)             - guess options for a following groff command
hosts_options (5)    - host access control language extensions
mount.fuse (8)       - format and options for the fuse file systems
netplan-try (8)      - try a configuration, optionally rolling it back
posixoptions (7)     - optional parts of the POSIX standard
sg_read (8)          - read multiple blocks of data, optionally with SCSI READ commands
shred (1)            - overwrite a file to hide its contents, and optionally delete it
xfs (5)              - layout, mount options, and supported file attributes for the XFS filesystem
```

3. _Comment quitte-t-on le manuel ?_<br>
Pour quitter une page du manuel, il suffit de presser la touche `q`.

4. _Chaque section du manuel a une première page, qui présente le contenu de la section. Afficher la
première page de la section 6 ; de quoi parle cette section ?_<br>
Il suffit d'utiliser la commande `man 6 intro`.

```
    DESCRIPTION
       Section 6 of the manual describes the games and funny little programs available on the system.
```

## :round_pushpin: Navigation dans l’arborescence des fichiers 

1. _allez dans le dossier /var/log_<br>
Pour se rendre dans un dossier de façon absolue, la commande à utiliser est `cd /<chemin d'accès>`. Par exemple `cd /var/log`.


2. _remontez dans le dossier parent (/var) en utilisant un chemin relatif_<br>
Il existe néanmoins des raccourcis pour permettre d'utiliser des chemins relatifs. Par exemple pour remonter d'un échelon dans l'arborescence il est possible d'utiliser la command `cd ..`.

3. _retournez dans le dossier personnel_<br>
Afin de retourner dans son dossier rapidement avec la commande `cd`.

4. _revenez au dossier précédent (/var)_<br>
Pour retourner au dossier précédement visité, il existe la commande `cd -`.

5. _essayez d’accéder au dossier /root ; que se passe-t-il ?_<br>
Accès refusé.

6. _essayez la commande sudo cd /root ; que se passe-t-il ? Expliquez_<br>
La commande cd fait partie du bash. Il s'agit d'une commande interne au shell. Sudo ne peut pas les utiliser.

7. _Création d'arborescence_

    `mkdir dossier1 && touch dossier1/fichier1 && mkdir dossier2 && mkdir dossier2/dossier2.1 && mkdir dossier2/dossier2.2 && touch dossier2/dossier2.2/fichier2 && touch dossier2/dossier2.2/fichier3`

8. _revenez dans votre dossier personnel ; à l’aide de la commande rm, essayez de supprimer Fichier1, puis Dossier1 ; que se passe-t-il ?_<br>
La commande `rm` permet de supprimer un fichier mais pas un dossier.

9. _quelle commande permet de supprimer un dossier ?_<br>
Pour supprimer un dossier, il faut utiliser la commande`rmdir`.

10. _que se passe-t-il quand on applique cette commande à Dossier2 ?_<br>
La commande nous retourne que le dossier comporte des fichiers.

11. _comment supprimer en une seule commande Dossier2 et son contenu ?_<br>
Il faut utiliser la commande `rm -r`.

## :pushpin: Commandes importantes

1. _Quelle commande permet d’afficher l’heure ? A quoi sert la commande time ?_<br>
Pour voir l'heure, utilisez la commande `date`.

2. _Dans votre dossier personnel, tapez successivement les commandes ls puis la ; que peut-on en déduire
sur les fichiers commençant par un point ?_<br>
La commande `ls` affiche les fichiers du dossier. La commande `la` affiche __tous__ les (même cachés). Les fichiers étant nommés avec un "." au début de leur nom, son cachés. 

3. _Où se situe le programme ls ?_<br>
Grâce à la comamnde `which ls`. Nous savons que la commande se situe : `/usr/bin/ls`.

4. _Que fait la commande ll ? (indice : la commande alias peut vous aider)_<br>
La commande `ll` affiche la totalité des informations des fichiers/dossiers (droits, propriétaire, groupe propriétaire, horodatage, taille, nom)

5. _Quelle commande permet d’afficher les fichiers contenus dans le dossier /bin ?_<br>
`ls /bin`

6. _Que fait la commande ls .. ?_<br>
La commande `ls ..` permet de lister le dossier à l'échelon suppérieur dans l'arborescence.

7. _Quelle commande donne le chemin complet du dossier courant ?_<br>
La commande `pwd` permet de donner le chemin complet du dossier courant.

8. _Que fait la commande echo 'yo' > plop exécutée 2 fois ?_<br>
L'utilisation d'un seul symbole ">" permet de créer un fichier et y inscrir la chaine de caractère entre ''.

9. _Que fait la commande echo 'yo' >> plop exécutée 2 fois ?_<br>
L'utilisation de deux symboles ">>" permet de créer un fichier et y inscrir la chaine de caractère entre ''. Si celle-ci est déjà présente, elle sera inscrite une deuxième fois.

10. _A quoi sert la commande file ? Essayez la sur des fichiers de types différents._<br>
La commande `file` retourne le type de données contenue dans une fichier du système.

11. _Créez un fichier toto qui contient la chaîne Hello Toto ! ; créer ensuite un lien titi vers ce fichier
avec la commande ln toto titi. Modifiez à présent le contenu de toto et affichez le contenu de titi :
qu’observe-t-on ? Supprimez le fichier toto ; quelle conséquence cela a-t-il sur titi ?_<br>
Lorsque le fichier toto est modifié, le fichier titi l'est aussi et inversement. Si l'on supprime un des deux fichiers, le lien est rompu et le fichier restant devient un fichier unique.

12. _Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez le
contenu de titi ; quelle conséquence pour tutu ? Et inversement ? Supprimez le fichier titi ; quelle
conséquence cela a-t-il sur tutu ?_<br>
Lorsque le fichier titi est modifié, le fichier tutu l'est aussi et inversement. Si l'on supprime le fichier titi, le lien est rompu et le fichier tutu est ilisible.

13. _Affichez à l’écran le fichier /var/log/syslog. Quels raccourcis clavier permettent d’interrompre et
reprendre le défilement à l’écran ?_<br>
Pour afficher un fichier, nous utiliserons la commande `cat <chemin>`. Grâce à la commande less, nous pourrons défiler dans le fichier librement.<br>
Exemple:
    `cat /var/log/syslog | less`

14. _Affichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les
lignes 10 à 20._<br>
Pour afficher des plages de lignes spécifique d'un fichier, nous utiliserons la commande head, perl et tail.<br>
Exemple:<br>
    * 5 premières : head -5 /var/log/syslog
    * entre 10-20 : perl -ne'10..20 and print' /var/log/syslog
    * 15 dernières : tail -15 /var/log/syslog

15. _Que fait la commande dmesg | less ?_<br>
La commande `dmesg` ou display message, permet de voir l'historique des messages du noyaux. La commande `less` quant à elle, ne quitte pas la pagination, il est donc possible de revenir en arrière sans relancer la commande, naviguer dans le fichier ouvert à l'aide des flèches de direction du clavier, passer d'une page à l'autre en appuyant sur la barre Espace ou F, revenir sur la page précédente en appuyant sur B (back), aller au début du fichier G, aller à la fin du fichier Shift+G et quitter avec Q.<br>
Une option qui peut être intéressante est -N. Elle sert à numéroter les lignes du fichier affiché à l'écran (le fichier lu n'est aucunement modifié).


16. _Affichez à l’écran le fichier /etc/passwd ; que contient-il ? Quelle commande permet d’afficher la page
de manuel de ce fichier ?_<br>
Le fichier /etc/passwd contient la liste de tous les utilisateurs systèmes ainsi que divers données sur leur compte comme l'id, le chemin d'accès au dossier utilisateur, le shell utilisé (/bin/false pour interdire).<br>
La commande pour accéder au manuel de ce fichier est `man 5 passwd`.

17. _Affichez seulement la première colonne triée par ordre alphabétique inverse_<br>
...

18. _Quelle commande nous donne le nombre d’utilisateurs ?_<br>
Pour trouver le nombre d'utilisateurs du système, il nous suffit en quelque sorte de compter combien de ligne comporte le fichier passwd.<br>
Pour cela nous utiliserons la command `wc -l /etc/passwd`.

19. _Combien de pages de manuel comportent le mot-clé conversion dans leur description ?_<br>
...

20. _A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine_<br>
La commande `find` est très utile pour rechercher un/des fichier(s) à partir d'un chemin d'accès.<br>
Exemple:
Pour chercher tous les fichiers nommés passwd dans la totalité du système : `find / -name 'passwd'`.

21. _Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier
~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null_ <br> Pour stocker le retour d'une commande dans un fichier (comme des logs), il est possible d'ajouter comme vu plus haut le symbole `>` suivi d'un nom de fichier. La mention `2>/dev/null` exclu les erreurs.<br>
Exemple: `find / -name 'passwd' > ~/list_passwd_files.txt 2>/dev/null`.

22. _Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu
précédemment_<br>
...

23. _Utilisez la commande locate pour trouver le fichier history.log._<br>
Pour trouver un fichier plus rapidement, nous pouvons utiliser la commande `locate`.<br>
Exemple: `locate 'history.log'`<br>
La commande nous retourne `/var/log/apt/history.log`.

24. _Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il ? Pourquoi ?_<br>
La commande `locate` utilise une base de données (d'où son côté très très rapide). En revanche cette base de données n'est mise à jour que toutes les 24h (ce qui est suffisant en soit). C'est pour cela que le fichier créé à l'instant ne resortira pas. Il faut taper la commande `updatedb` pour mettre à jour cette base de données.

### :paperclip: NOTA : Travailler avec plusieurs shells
On peut utiliser jusqu’à 6 shells en parallèle. Ils portent les noms ttyX (où X va de 1 à 6) et sont
accessibles via Alt + FX

# Exercice 3. Découverte de l’éditeur de texte nano

1. _Copiez le fichier /var/log/syslog dans votre dossier personnel sous le nom log.txt, puis ouvrez-le avec
nano_<br>
`sudo cp /var/log/syslog ~/log.txt && nano ~/log.txt`

2. _Remplacez toutes les occurrences du mot kernel par le mot noyau_<br>
`CTRL + W` > `CTRL + R` > taper le mot à remplacer > taper le mot qui remplacera

3. _Déplacer les 10 premières lignes à la fin du fichier_<br>
...

4. _Annulez cette action_<br>
`ALT + U`

5. _Enregistrez le fichier avant de quitter nano_<br>
`CTRL + S`


# Exercice 4. Personnalisation du shell

* La syntaxe finale du shell est la suivante<br>
`\[\033[95m\]\A - \[\033[92m\]\u@\h\[\033[00m\]:\[\033[36m\]\w\[\033[00m\]\$`
