# Administration Systèmes


# Exercice 2

## Manuel

 ***1.*** Commande which :
	 Permet de localiser une commande. Exemple : which ls
	 
***2.*** Recherche dans le manuel : /mot_a_rechercher

***3.*** On quitte le manuel en cliquant sur la touche 'q'

***4.*** Affichage de la première page de la section 6 :
	man 6 intro : Cette section décrit les jeux disponibles.
	


## Navigation dans l'arborescence des fichiers

***1.***  Naviguer dans l'arborescence à partir du root  : cd /
	Exemple : cd /var/log

***2.*** Remonter dans le dossier parent :  cd ../

***3.*** Retourner dans le dossier personnel : cd

***4.*** Revenir au dossier précédent :  cd -

***5.*** Acces au dossier root : cd /root -> Permission non accordée

***6.*** La commande sudo cd /root ne fonctionne pas car sudo ne peut être appliqué uniquement sur des programmes et non pas sur des commandes

***8.*** Supprimer un fichier : rm
	Cette commande a bien supprimé le fichier 1

***9.*** Supprimer un dossier : rm -r
	Cette commande a bien supprimé le dossier 1

***10.*** Si on applique cette commande à un dossier non vide, cela supprime tous les dossiers et fichiers enfants.

***11.***  Supprimer un dossier non vide : rm -fr
	

## Commandes importantes

***1.*** Pour afficher l'heure, on execute la commande: ***date +%R*** on peut aussi combiner l'affichage des heure et des minutes en changeant le separateur, par exemple : ***date +%Hh%M***
La commande ***time*** permet de calculer le temps necessaire a l'execution d'une commande.

***2.*** ***ls*** permet d'afficher le contenu du dossier en cours alors que ***la*** permet d'afficher les dossier précédés d'un point qui sont les fichiers cachés.

***3.*** La commande ***ls*** se situe dans le fichier ***/bin/ls*** (commande: ***which ls***)

***4.*** La commande ***ll*** n'a pas d'entrée dans le manuel. On trouve son nom complet ***ls -alF*** via la commande ***alias***. C'est donc une combinaison d'options de la commande ***ls***. Elle sert a : 
-> ***-a*** afficher tous les fichiers, y compris ceux commencant par un point.
-> ***-l*** utiliser un format de listage long (type, permission d'acces, lien physique, nom du proprietaire, taille en octet, horodatage).
-> ***-F*** ajouter un caractere pour preciser le type de fichier.

***5.*** La commande ***ls /bin***

***6.*** La commande ***ls ..*** permet de lister les fichiers du dossier mère.

***7.*** Pour afficher le chemin complet du dossier courant : pwd

***8.*** La commande echo 'yo' > plop exécutée 2 fois permet de créer le dossier plop et d'écrire dedans yo une seule fois.

***9.*** La commande echo 'yo' >> plop exécutée 2 fois permet d'ajouter deux fois 'plop' à la fin du fichier plop crée précédemment.

***10.*** La commande file permet de déterminer le type d'un fichier.

***11.*** Création du fichier tott et insertion de "Hello toto" : "touch" puis on va insérer la chaine avec : echo "Hello toto" > toto.

	Creation du lien "titi" vers "toto" : "ln toto titi".

	Si on modifie le fichier toto, le fichier titi est aussi modifié.

	Si on supprime toto, le fichier titi n'est pas supprimé.

***12.*** Création d'un lien symbolique : "ln - s titi tutu".

	Si on modifie titi, le fichier tutu est aussi modifié. De même, si on modifie tutu alors titi est modifié.

	Si on supprimme titi alors le fichier tutu n'est pas supprimé mais son contenu est vide


***13.*** ctrl+s permet d'arreter le defilement et ctrl+q permet de le reprendre

***14.*** Affichier 5 premières lignes d'un fichier : "head -5 nomDuFichier"
	  Afficher les 15 dernières :"tail -15 nomDuFichier"
	  Afficher les lignes 10 à 20:"sed -n '10,20p' nomDuFichier".

***15.*** "dmesg | less" affiche la mémoire tampon de message du noyau accoupler à | less qui permet d'afficher un fichier page par page.

***16.*** Le fichier /etc/passwd contient toutes les informations relatives aux utilisateurs.Passwd permet aussi de modifier le mot de passe d'un utilisateur. La page de manuel correspondante : "man passwd."

***17.*** La commande "sort -k 1 -d -r passwd" permet de trier la premiere colonne dans l'ordre inverse de l'alphabet.

***18.*** La commande "w" permet d'afficher les différents utilisateurs.

***19.*** "man -k conversion" affiche le nombre de page contenant le mot conversion dans le résumé. Il y en a 4.

***20.*** La commande " find / -name passwd " permet de rechercher tous les fichiers se nommant passwd présent sur la machine.

***21.*** La commande : "find / -name passwd > ~/list_passwd_files.txt 2>> /dev/null" permet d'afficher la liste des fichiers trouvés puis l'enregistre dans le fichier ~/list_passwd_files.txt. Enfin, les erreurs sont affichées dans le fichier spécial /dev/null.

***22.*** La commande : "grep "ll" -r" permet de trouver tous les endroits ou le caractère ll apparait. 
	  On trouve l'alias ll dans : " .bashrc:alias ll='ls -alF' ".

***23.*** La commande locate a permet de trouver un fichier. 
	  Pour trouver le fichier history.log : history.log : locate history.log 
	  Réponse : /var/log/apt/history.log.

***24.*** Création du fichier question : " touch question "
	  Avec la commande " locate fichier " on ne trouve pas le fichier car la base de donnée n'a pas été mis à jour.
	  Pour mettre à jour la base de donnée : "updatedb".





