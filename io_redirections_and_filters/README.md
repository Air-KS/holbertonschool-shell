# Shell - Redirections et filtres / Redirections and Filters

![](https://www.seeyar.fr/wp-content/uploads/2014/02/linux-shell.webp)

Projet réalisé dans le cadre de l'école **[Holberton School](https://www.holbertonschool.fr/?utm_source=googleads&utm_medium=cta&gclid=CjwKCAiA_6yfBhBNEiwAkmXy50eX6Dq5EZ7N9KvwnQ9og_Xm7dYtCC2PkdKXvP-tK75zN7BWrIze2BoC1zgQAvD_BwE/).** Il vise à apprendre à gérer les entrées et les sorties standard et à combiner des commandes et des filtres avec des redirections dans **[Shell](http://hautrive.free.fr/linux/page-shell-linux.html)**.  

## Technologies
* [Emacs](https://www.gnu.org/software/emacs/)
* [Vim](https://doc.ubuntu-fr.org/vim/)
* Script écrits en [Bash](https://datascientest.com/bash-tout-savoir/)
* Tester sur Ubuntu [22.04 LTS](https://ubuntu.com/download/desktop/)

## Fichiers
Tous les script de ce projets utilise l'interpreteur [Bash](https://datascientest.com/bash-tout-savoir/).
- `#!/bin/bash`  
  
Voici un tableau des scripts et commande utilisé pour l'ensemble du projet Shell - Redirections and Filtre

| Nom du Fichier | Commande Utiliser | Description du Fichier |
| -------- | ----------- | ----------- |
| [0-hello_world](./0-hello_world) | `echo "Hello, World"` | Script qui affiche `Hello, World`, suivi d'une nouvelle ligne sur la sortie standard |
| [1-confused_smiley](./1-confused_smiley) | `echo "\"(Ôo)'"` | Script qui affiche un smiley confus `(Ôo)`. |
| [2-hellofile](./2-hellofile) | `cat /etc/passwd` | Script qui Affichez le contenu du fichier `/etc/passwd`.
| [3-twofiles](./3-twofiles) | `cat /etc/passwd /etc/hosts` | Script qui Affichez le contenu du fichier `/etc/passwd` et `/etc/hosts`
| [4-lastlines](./4-lastlines) | `tail /cat/passwd` | Script qui Afficher les `10 dernières lignes` de `/cat/passwd`
| [5-firstlines](./5-firstlines) | `head /etc/passwd` | Script qui Afficher les 10 premières lignes de `/etc/passwd`
| [6-third_line](./6-third_line) | `head -n 3 iacta l tail -n 1` | Script qui Afficher les 10 premières lignes de `/etc/passwd`
| [7-file](./7-file) | `echo -e "Best School"  >> "\\*\\\\'\"Best School\"\\'\\\\*$\\?\\*\\*\\*\\*\\*:)"` | Écrivez un script shell qui crée un fichier nommé exactement `\*\\'"Best School"\'\\*$\?\*\*\*\*\*:)` contenant le texte Best School se terminant par une nouvelle ligne.
| [8-cwd_state](./8-cwd_state) | `ls -la >> ls_cwd_content` | Script qui écrit dans le fichier ls_cwd_content le résultat de la commande `ls -la`. Si le fichier `ls_cwd_content` existe déjà, il doit être écrasé. Si le fichier `ls_cwd_content` n'existe pas, Il le crée.
| [9-duplicate_last_line](./9-duplicate_last_line) | `tail -1 iacta >> iacta` | Script qui duplique `La dernière ligne` du fichier `iacta`
| [10-no_more_js](./10-no_more_js) | `find . -type f -name "*.js" -delete` | Script qui supprime tous les fichiers normaux *Pas les Répertoires* avec une extension `.js` présents dans le répertoire actuel et tous ses sous-dossiers.
| [11-directories](./11-directories) | `find -mindepth 1 -type d l wc -l` | Script qui compte le nombre de répertoires et de sous-répertoires dans le répertoire courant.
| [12-newest_files](./12-newest_files) | `ls -t . l head` | Script qui affiche les `10 fichiers` les plus récents du répertoire actuel.
| [13-unique](./13-unique) | `sort l uniq -u` | Script qui prend une liste de mots en entrée et imprime que les mots qui apparaissent exactement une fois.
| [14-findthatword](./14-findthatword) | `egrep "root" /etc/passwd` | Script qui Afficher les lignes contenant le motif `root` du fichier `/etc/passwd`
| [15-countthatword](./15-countthatword) | `egrep -c 'bin' /etc/passwd` | Script qui Afficher le nombre de lignes contenant le motif `bin` dans le fichier `/etc/passwd`
| [16-whatsnext](./16-whatsnext) | `grep -A 3 'root' /etc/passwd` | Script qui Afficher les lignes contenant le motif `root` et `3 lignes` après celles-ci dans le fichier `/etc/passwd`
| [17-hidethisword](./17-hidethisword) | `grep -v "bin" /etc/passwd` | Script qui Affiche toutes les lignes du fichier `/etc/passwd` qui ne contiennent pas le motif `bin`.
| [18-letteronly](./18-letteronly) | `grep '^[[:alpha:]]' /etc/ssh/sshd_config` | Script qui Affiche toutes les lignes du fichier `/etc/ssh/sshd_config` commençant par une lettre.
| [19-AZ](./19-AZ) | `tr Ac Ze` | Script qui Remplacez tous les caractères `A` et `c` de l'entrée par `Z` et `e` respectivement.
| [20-hiago](./20-hiago) | `tr -d Cc` | Script qui supprime toutes les lettres `c` et `C` de l'entrée.
| [21-reverse](./21-reverse) | `rev` | Script qui `Inverse` son entrée.
| [22-users_and_homes](./22-users_and_homes) | `cut -f 1,6 -d ':' /etc/passwd l sort` | Script qui affiche tous les `Utilisateurs` et leurs répertoires personnels, triés par `Utilisateurs`.
| [23-empty_casks](./23-empty_casks) | `23-empty_casks` | Script qui trouve tous les fichiers et répertoires vides dans le répertoire courant et tous les sous-répertoires.
| [24-gifs](./24-gifs) | `find . -type f -name "*.gif" l rev l cut -d "/" -f1 l cut -d "." -f2,3 l rev l sort -Vf` | Script qui liste tous les fichiers avec une extension `.gif` dans le répertoire courant et tous ses sous-répertoires.
| [25-acrostic](./25-acrostic) | `cut -c 1 l paste -s -d ''` | Script qui décode les [Acrostic](https://en.wikipedia.org/wiki/Acrostic/) utilisant la première lettre de chaque ligne.
