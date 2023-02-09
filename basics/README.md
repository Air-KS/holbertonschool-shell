# holbertonschool-shell

0-current_working_directory "pwd" - Écrivez un script qui imprime le nom de chemin absolu du répertoire de travail actuel.

[1-listit](./1-listit) 1-listit "ls" - Affiche la liste du contenu de votre répertoire actuel.

2-bring_me_home "cd" - Écrivez un script qui remplace le répertoire de travail par le répertoire personnel de l'utilisateur. Vous n'êtes pas autorisé à utiliser des variables shell

3-listfiles "ls -l" - Affiche le contenu du répertoire actuel dans un format long

4-listmorefiles "ls -a" - Affiche le contenu du répertoire actuel, y compris les fichiers cachés (commençant par .). Utilisez le format long.

5-listfilesdigitonly " ls -lna" - Afficher le contenu du répertoire actuel. Format long avec ID utilisateur et groupe affichés numériquement Et fichiers cachés (commençant par .)

6-firstdirectory "mkdir /tmp/my_first_directory/" Créez un script qui crée un répertoire nommé holberton dans le répertoire /tmp/.

7-movethatfile "mv /tmp/betty /tmp/my_first_directory" - Déplacez le fichier betty de /tmp/ vers /tmp/holberton

8-firstdelete "rm /tmp/my_first_directory/betty" - Supprimez le fichier betty.

9-firstdirection "rm -r /tmp/my_first_directory" - Supprimez le répertoire my_first_directory

10-back "cd -" - Retourner au repertoir précédent. Avec cd on retour à la racine "root". Avec "cd -" On retourne au répértour précedfent. 

11-lists "ls -la . .. /boot" - Écrivez un script qui répertorie tous les fichiers (même ceux dont le nom commence par un point, qui sont normalement cachés) dans le répertoire courant et le parent du répertoire de travail et du répertoire /boot (dans cet ordre), au format long.

12-file_type "file /tmp/iamafile" - Script qui ecrit le type du fichier nommé iamfile. Le fichier iamafile sera dans le répertoire /tmp lorsque nous exécuterons le script.

13-symbolic_link "ln -s /bin/ls __ls__" - Créez un lien symbolique vers /bin/ls, nommé ls. Le lien symbolique doit être créé dans le répertoire de travail courant.

14-copy_html "cp -u *.html .." - Créez un script qui copie tous les fichiers HTML du répertoire de travail actuel vers le parent du répertoire de travail, mais copiez uniquement les fichiers qui n'existaient pas dans le parent du répertoire de travail ou qui étaient plus récents que les versions du parent du répertoire de travail . Vous pouvez considérer que tous les fichiers HTML ont l'extension .html

15-lets_move "mv [[:upper:]]* /tmp/u" OU "mv [[:A-Z:]]* /tmp/u" - Créez un script qui déplace tous les fichiers commençant par une lettre majuscule vers le répertoire /tmp/u. Vous pouvez supposer que le répertoire /tmp/u existera lorsque nous exécuterons votre script

16-clean_emacs "rm *~" - Créez un script qui supprime tous les fichiers du répertoire de travail actuel qui se terminent par le caractère ~.

17-treee "mkdir -p welcome/to/school" - Créez un script qui crée les répertoires welcome/, welcome/to/ et welcome/to/school dans le répertoire courant. Vous n'êtes autorisé à utiliser que deux espaces dans votre script, pas plus.

curl http://www.star.bris.ac.uk/bjm/superman_cluster.gif -o superman_cluster.gif