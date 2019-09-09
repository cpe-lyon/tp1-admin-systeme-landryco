# Exercice 2. Prise en main de l’interpréteur de commandes

## :closed_book: Manuel

1. La commande which permet de localiser une commande
2. L'option `-k` peut-être utilisé dans la command `man` afin de rechercher un mot clé. Par exemple `man -k option`.
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
3. Pour quitter une page du manuel, il suffit de presser la touche `q`

4. `man 6 intro`
```
    DESCRIPTION
       Section 6 of the manual describes the games and funny little programs available on the system.
```

## :round_pushpin: Navigation dans l’arborescence des fichiers 

1. Pour se rendre dans un dossier de façon absolue, la commande à utiliser est `cd /<chemin d'accès>`. Par exemple `cd /var/log`.


2. Il existe néanmoins des raccourcis pour permettre d'utiliser des chemins relatifs. Par exemple pour remonter d'un échelon dans l'arborescence il est possible d'utiliser la command `cd ..`

3. Afin de retourner dans son dossier rapidement avec la commande `cd`

4. Pour retourner au dossier précédement visité, il existe la commande `cd -`

5. Accès refusé

6. La commande cd fait partie du bash. Il s'agit d'une commande interne au shell. Sudo ne peut pas les utiliser

7. _Création d'arborescence_

    `mkdir dossier1 && touch dossier1/fichier1 && mkdir dossier2 && mkdir dossier2/dossier2.1 && mkdir dossier2/dossier2.2 && touch dossier2/dossier2.2/fichier2 && touch dossier2/dossier2.2/fichier3`

8. La commande `rm` permet de supprimer un fichier mais pas un dossier.

9. Pour supprimer un dossier, il faut utiliser la commande`rmdir`.

10. La commande nous retourne que le dossier comporte des fichiers.

11. Il faut utiliser la commande `rm -r`.

## :pushpin: Commandes importantes
