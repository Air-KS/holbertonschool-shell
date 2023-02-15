# Shell - Init, File, Variables and expansions

>Projet réalisé dans le cadre de l'école **[Holberton School](https://www.holbertonschool.fr/?utm_source=googleads&utm_medium=cta&gclid=CjwKCAiA_6yfBhBNEiwAkmXy50eX6Dq5EZ7N9KvwnQ9og_Xm7dYtCC2PkdKXvP-tK75zN7BWrIze2BoC1zgQAvD_BwE/).** Il vise à apprendre à gérer les entrées et les sorties standard et à combiner des commandes et des filtres avec des redirections dans **[Shell](http://hautrive.free.fr/linux/page-shell-linux.html)**.  

## Read or watch:
* [Expansions](http://linuxcommand.org/lc3_lts0080.php)  
* [Shell Arithmetic](https://www.gnu.org/software/bash/manual/html_node/Shell-Arithmetic.html)  
* [Variables](https://tldp.org/LDP/Bash-Beginners-Guide/html/sect_03_02.html)  
* [Shell initialization files](https://tldp.org/LDP/Bash-Beginners-Guide/html/sect_03_01.html)  
* [The alias Command](http://www.linfo.org/alias.html)  
* [Technical Writing](https://s3.eu-west-3.amazonaws.com/hbtn.intranet/uploads/misc/2021/6/9112669886fd446a2aa3113c31319d1f468dc160.pdf?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4MYA5JM5DUTZGMZG%2F20230215%2Feu-west-3%2Fs3%2Faws4_request&X-Amz-Date=20230215T185212Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=9f0cd9ecfc4cdf70a91e5a7540b0e39377005beb3d173815713bd57474e7b71d)  


## Man or Help in terminal
 > printenv | set | unset | export | alias | unalias | . | source | printf
 
## Technologies
* [Vim](https://doc.ubuntu-fr.org/vim/)
* Script écrits en [Bash](https://datascientest.com/bash-tout-savoir/)
* Tester sur Ubuntu [22.04 LTS](https://ubuntu.com/download/desktop/)

## Fichiers
Tous les script de ce projets utilise l'interpreteur [Bash](https://datascientest.com/bash-tout-savoir/).
- `#!/bin/bash`  
  
Voici un tableau des scripts et commande utilisé pour l'ensemble du projet Shell - Redirections and Filtre

| Nom du Fichier | Commande Utiliser | Description du Fichier |
| :--------: | :-----------: | :-----------: |
| [0-alias](./0-alias) | `echo "Hello, World"` | Script qui affiche `Hello, World`, suivi d'une nouvelle ligne sur la sortie standard |
| [1-hello_you](./1-hello_you) | `echo "\"(Ôo)'"` | Script qui affiche un smiley confus `(Ôo)`. |
| [2-path ](./2-path) | `cat /etc/passwd` | Script qui Affichez le contenu du fichier `/etc/passwd`.
| [3-paths](./3-paths) | `cat /etc/passwd /etc/hosts` | Script qui Affichez le contenu du fichier `/etc/passwd` et `/etc/hosts`
| [4-global_variables](./4-global_variables) | `tail /cat/passwd` | Script qui Afficher les `10 dernières lignes` de `/cat/passwd`
| [5-local_variables](./5-local_variables) | `head /etc/passwd` | Script qui Afficher les 10 premières lignes de `/etc/passwd`
| [6-create_local_variable](./6-create_local_variable) | `head -n 3 iacta l tail -n 1` | Script qui Afficher les 10 premières lignes de `/etc/passwd`
| [7-create_global_variable](./7-create_global_variable) | `echo -e "Best School"  >> "\\*\\\\'\"Best School\"\\'\\\\*$\\?\\*\\*\\*\\*\\*:)"` | Écrivez un script shell qui crée un fichier nommé exactement `\*\\'"Best School"\'\\*$\?\*\*\*\*\*:)` contenant le texte Best School se terminant par une nouvelle ligne.
| [8-true_knowledge](./8-true_knowledge) | `ls -la >> ls_cwd_content` | Script qui écrit dans le fichier ls_cwd_content le résultat de la commande `ls -la`. Si le fichier `ls_cwd_content` existe déjà, il doit être écrasé. Si le fichier `ls_cwd_content` n'existe pas, Il le crée.
| [9-divide_and_rule](./9-divide_and_rule) | `tail -1 iacta >> iacta` | Script qui duplique `La dernière ligne` du fichier `iacta`
| [10-love_exponent_breath](./10-love_exponent_breath) | `find . -type f -name "*.js" -delete` | Script qui supprime tous les fichiers normaux *Pas les Répertoires* avec une extension `.js` présents dans le répertoire actuel et tous ses sous-dossiers.
| [11-binary_to_decimal](./11-binary_to_decimal) | `find -mindepth 1 -type d l wc -l` | Script qui compte le nombre de répertoires et de sous-répertoires dans le répertoire courant.
| [12-combinations](./12-combinations) | `ls -t . l head` | Script qui affiche les `10 fichiers` les plus récents du répertoire actuel.
| [13-print_float](./13-print_float) | `sort l uniq -u` | Script qui prend une liste de mots en entrée et imprime que les mots qui apparaissent exactement une fois.
| [14-decimal_to_hexadecimal](./14-decimal_to_hexadecimal) | `egrep "root" /etc/passwd` | Script qui Afficher les lignes contenant le motif `root` du fichier `/etc/passwd`
| [15-rot13](./15-rot13) | `egrep -c 'bin' /etc/passwd` | Script qui Afficher le nombre de lignes contenant le motif `bin` dans le fichier `/etc/passwd`
| [16-odd](./16-odd) | `grep -A 3 'root' /etc/passwd` | Script qui Afficher les lignes contenant le motif `root` et `3 lignes` après celles-ci dans le fichier `/etc/passwd`
| [17-water_and_stir](./17-water_and_stir) | `grep -v "bin" /etc/passwd` | Script qui Affiche toutes les lignes du fichier `/etc/passwd` qui ne contiennent pas le motif `bin`.
