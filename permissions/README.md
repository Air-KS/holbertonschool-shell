# Shell Permission

[0-iam_betty](./0-iam_betty) - "su betty "  
Script qui bascule l'utilisateur actuel vers l'utilisateur betty.

[1-who_am_i](./1-who_am_i) - "whoami"  
Script qui imprime le nom d'utilisateur effectif de l'utilisateur actuel.

[2-groups](./2-groups) - "groups"  
Script qui imprime tous les groupes dont l'utilisateur actuel fait partie.

[3-new_owner](./3-new_owner) - "chown betty hello"  
Script qui change le propriétaire du fichier hello en utilisateur betty.

[4-empty](./4-empty) - "touch hello"  
Script qui crée un fichier vide appelé hello.

[5-execute](./5-execute) - "chmod u+x hello" ou "+100"  
Script qui crée un fichier vide appelé hello.

[6-multiple_permission](./6-multiple_permission) - "u+x,g+x,o+r"  
Script qui ajoute l'autorisation d'exécution au propriétaire et au propriétaire du groupe, et l'autorisation de lecture aux autres utilisateurs, au fichier hello. 

[7-Everybody](./7-Everybody) - "chmod a+x hello"  
Script qui ajoute une autorisation d'exécution au propriétaire, au propriétaire du groupe et aux autres utilisateurs, dans le fichier hello

[8-Jamers_Bond](./8-Jamers_Bond) - "chmod 007 hello"  
Script qui définit l'autorisation sur le fichier hello

[9-John_Doe](./9-John_Doe) - "chmod 753 hello"  
Script qui définit le mode du fichier hello

[10-mirror_permissions](./10-mirror_permissions) -"chmod 354 olleh hello"  
Script qui définit le mode du fichier hello de la même manière que le mode d'olleh.

[11-directories_permissions](./11-directories_permissions) - "chmod -R a+x (asterisque)/"  
Script qui ajoute une autorisation d'exécution à tous les sous-répertoires du répertoire actuel pour le propriétaire, le propriétaire du groupe et tous les autres utilisateurs. Les fichiers normaux ne doivent pas être modifiés.

[12-directory_permissions](./12-directory_permissions) - "mkdir -m 751 my_dir"  
Script qui crée un répertoire appelé my_dir avec les autorisations 751 dans le répertoire de travail.

[13-change_group](./13-change_group ) - "chgrp school hello"  
Script qui change le propriétaire du groupe en école pour le fichier bonjour

[14-change_owner_and_group](./14-change_owner_and_group) - "chown -R vincent:staff (asterisque)"  
Script qui change le propriétaire en vincent et le propriétaire du groupe en staff pour tous les fichiers et répertoires du répertoire de travail. 

[15-symbolic_link_permissions](./15-symbolic_link_permissions) - "chown -h vincent:staff (Underscor)hello"  
Script qui change le propriétaire et le propriétaire du groupe de hello en vincent et staff respectivement.

[16-if_only](./16-if_only) - "Chmod --from=guillaume vincent hello"  
Script qui change le propriétaire du fichier hello en vincent uniquement s'il appartient à l'utilisateur guillaume.
