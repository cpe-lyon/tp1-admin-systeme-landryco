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
