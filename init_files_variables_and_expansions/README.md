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
| [0-alias](./0-alias) | `alias ls="rm *"` | Script qui crée un `alias`. |
| [1-hello_you](./1-hello_you) | `echo hello $USER` | Script qui imprime `hello user`, où `user` est l'utilisateur Linux actuel..
| [2-path ](./2-path) | `2-path` | Script qui Ajoutez `/action` au `PATH`. `/action` doit être le dernier répertoire dans lequel le *shell* se penche lorsqu'il recherche un programme..
| [3-paths](./3-paths) | `echo $PATH l tr -s ':' '\n' l wc -l ` | Script qui compte le nombre de répertoires dans le `PATH`.
| [4-global_variables](./4-global_variables) | `printenv` | Script qui répertorie les variables d'environnement.
| [5-local_variables](./5-local_variables) | `set` | Script qui répertorie toutes les variables locales et les variables d'environnement, ainsi que les fonctions.
| [6-create_local_variable](./6-create_local_variable) | `BEST="School"` | Script qui crée une nouvelle variable locale.
| [7-create_global_variable](./7-create_global_variable) | `export BEST="School"` | Script qui crée une nouvelle variable globale.
| [8-true_knowledge](./8-true_knowledge) | `echo $(($TRUEKNOWLEDGE+128))` | Script qui imprime le résultat de l'addition de 128 avec la valeur stockée dans la variable d'environnement `TRUEKNOWLEDGE`, suivi d'une nouvelle ligne.
| [9-divide_and_rule](./9-divide_and_rule) | `echo $(( $POWER / $DIVIDE ))` | Script qui imprime le résultat de `POWER` divisé par `DIVIDE`, suivi d'une nouvelle ligne.
| [10-love_exponent_breath](./10-love_exponent_breath) | `echo "$((BREATH**LOVE))"` | Script qui affiche le résultat de `BREATH` au pouvoir `LOVE`
| [11-binary_to_decimal](./11-binary_to_decimal) | `echo $((2#$BINARY))` | Script qui convertit un nombre de base 2 en base 10.
| [12-combinations](./12-combinations) | `echo {a..z}{a..z} l tr ' ' '\n' l grep -v "oo"` | Script qui imprime toutes les combinaisons possibles de deux lettres, sauf `oo`.
| [13-print_float](./13-print_float) | `printf "%.2f\n" $NUM` | Script qui imprime un nombre avec deux décimales, suivi d'une nouvelle ligne. Le numéro sera stocké dans la variable d'environnement `NUM`.
| [14-decimal_to_hexadecimal](./14-decimal_to_hexadecimal) | `printf "%x\n" $DECIMAL` | Script qui convertit un nombre de base 10 en base 16. Le nombre en base 10 est stocké dans la variable d'environnement `DECIMAL`.
| [15-rot13](./15-rot13) | `tr 'A-Za-z' 'N-ZA-Mn-za-m'` | Script qui encode et décode le texte en utilisant le cryptage rot13. Supposons ASCII.
| [16-odd](./16-odd) | `paste - - | cut -f1` | Script qui imprime une ligne sur deux à partir de l'entrée, en commençant par la première ligne.
| [17-water_and_stir](./17-water_and_stir) | `printf "%o\n" $(( $((5#$(echo $WATER l tr water 01234))) + $((5#$(echo $STIR l tr stir. 01234))) )) l tr 01234567 bestchol ` | Script *shell* qui additionne les deux nombres stockés dans les variables d'environnement `WATER` et `STIR` et imprime le résultat.
