# Shell - Redirections et filtres / Redirections and Filters !

Projet réalisé dans le cadre de l'école **Holberton School.** Il vise à apprendre à gérer les entrées et les sorties standard et à combiner des commandes et des filtres avec des redirections dans **Shell**.  

## Technologies
* Emacs
* Vim
* Script écrits en Bash
* Tester sur Ubuntu 22.04 LTS

## Fichiers
Voici un tableau des scripts et commande utilisé pour l'ensemble du projet Shell - Redirections and Filtre

| Nom du Fichier | Commande Utiliser | Description du Fichier |
| -------- | ----------- | ----------- |
| [0-hello_world](./0-hello_world) | `echo "Hello, World"` | Script qui affiche `Hello, World`, suivi d'une nouvelle ligne sur la sortie standard |
| [1-confused_smiley](./1-confused_smiley) | `echo "\"(Ôo)'"` | Script qui affiche un smiley confus `(Ôo)`. |
| [2-hellofile](./2-hellofile) | `cat /etc/passwd` | Script qui Affichez le contenu du fichier `/etc/passwd`.
| [3-twofiles](./3-twofiles) | `cat /etc/passwd /etc/hosts` | Script qui Affichez le contenu du fichier `/etc/passwd` et `/etc/hosts`
| [4-lastlines](./4-lastlines) | `tail /cat/passwd` | Script qui Afficher les `10 dernières lignes` de `/cat/passwd`
| [5-firstlines](./5-firstlines) | `head /etc/passwd` | Script qui Afficher les 10 premières lignes de `/etc/passwd`
| [6-third_line](./6-third_line) | `head -n 3 iacta l tail -n 1` | Script qui affiche la troisième ligne du fichier iacta.
