# holbertonschool-shell

[0-current_working_directory](./0-current_working_directory) "pwd" - Script qui indique le nom de chemin absolu du répertoire de travail actuel.

[1-listit](./1-listit) "ls" - Script qui permet de Lister le contenu de votre répertoire actuel.

[2-bring_me_home](./2-bring_me_home) "cd" - Script qui permet de Naviguer à travers les répertoir et/ou de revenir à la racine de root.

[3-listfiles](./3-listfiles) "ls -l" - Script qui liste le contenu du répertoire actuel de façon plus complète.

[4-listmorefiles](./4-listmorefiles) "ls -a" - Script qui liste le contenu du répertoire actuel, y compris les fichiers cachés.

[5-listfilesdigitonly](./5-listfilesdigitonly) "ls -lna" - Script qui liste le contenu du répertoire actuel, y compris les fichiers cahcés. Avec ID utilisateur et groupe affichés numériquement.

[6-firstdirectory](./6-firstdirectory) "mkdir /tmp/my_first_directory/" Script qui crée un répertoire nommé my_first_directory dans le répertoire /tmp/. mkdir = Make Directory

[7-movethatfile](./7-movethatfile) "mv /tmp/betty /tmp/my_first_directory" - Script qui permet de déplacer le fichier betty de /tmp/ vers /tmp/my_first_directory. mv = Move/Rename

[8-firstdelete](./8-firstdelete) "rm /tmp/my_first_directory/betty" - Script qui permet de supprimer le fichier betty. rm = Remove

[9-firstdirdeletion](./9-firstdirdeletion) "rm -r /tmp/my_first_directory" - Script qui permet de supprimer le répertoire my_first_directory.

[10-back](./10-back) "cd -" - Script qui permet de retourner au repertoir précédent. Avec cd on retour à la racine "root". Avec "cd -" On retourne au répértour précedent. 

[11-lists](./11-lists) "ls -la . .. /boot" - Script qui permet de répertorier tous les fichiers (même ceux qui sont normalement cachés) dans le répertoire courant et le parent du répertoire de travail et du répertoire /boot (dans cet ordre), de façon complète.

[12-file_type](./12-file_type) "file /tmp/iamafile" - Script qui crée un fichier nommé iamfile. Le fichier iamafile sera dans le répertoire /tmp lorsque nous exécuterons le script.

[13-symbolic_link](./13-symbolic_link) "ln -s /bin/ls __ls__" - Scripte qui Crée un lien symbolique vers /bin/ls, nommé ls. Le lien symbolique doit être créé dans le répertoire de travail courant.

[14-copy_html](./14-copy_html) "cp -u *.html .." - Scripte qui copie tous les fichiers HTML du répertoire de travail actuel vers le parent du répertoire de travail, mais copie uniquement les fichiers qui n'existaient pas dans le parent du répertoire de travail ou qui étaient plus récents que les versions du parent du répertoire de travail.

[15-lets_move](./15-lets_move) "mv [[:upper:]]* /tmp/u" OU "mv [[:A-Z:]]* /tmp/u" - Script qui déplace tous les fichiers commençant par une lettre majuscule vers le répertoire /tmp/u.

[16-clean_emacs](./16-clean_emacs) "rm *~" - Script qui supprime tous les fichiers du répertoire de travail actuel qui se terminent par le caractère ~.

[17-tree](./17-tree) "mkdir -p welcome/to/school" - Script qui crée les répertoires welcome/, welcome/to/ et welcome/to/school dans le répertoire courant.