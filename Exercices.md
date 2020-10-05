## Exercices

## 1 

​	$ mkdir exo

​	$ cd exo

​	$ pwd

​	/home/collignon/exo

## 2

​	$ cd exo

​	$ touch es1

​	$ mkdir essai2

## 3

​	$ cp es1 essai2

​	$ mv essaie2/es1 essai2/es1-copie

*Nous pouvons obtenir ce résultat en ne faisant qu'une seule opération*

​	$ cp es1 essai2/es1-copie

## 4

La commande a utiliser afin de créer ces répertoires est la commande mkdir, qui permet de créer des répertoires.

## 5

*La commande ls *  va afficher l'ensemble des fichiers contenus dans le répertoire courant ('exo') ainsi que l'ensemble de tout les fichiers contenus dans ses sous répertoires.*

​	$ ls *                                                                                                                                                                         	    	es1

​	essai2                                                                                                                                                               	  	 	        	es1-copie



Pour voir les fichiers dont le nom commence par 'es', il faut utiliser '''' qui représente n'importe quelle suite de caractères. La commande ls es *, va afficher l'ensemble des fichiers qui commencent par 'es'.

## 6

La commande 'rm -i <fichier>' permet de supprimer un fichier avec demande de confirmation. L'option '-r' permet de supprimer les répertoires et sous-répertoires récursivement.

## 7

La commande 'head -n 51' permet de récupérer les 51 premières lignes du fichier.

Nous utilisons ensuite la commande 'tail - n 1', pour n'afficher que la dernière ligne.

​	$ head -n 51 <fichier> | tail -n 1

## 8

La terminaison '-s' permet de supprimer les messages d'erreur.

​	$ grep passwd /etc/* -s

## 9

La commande à utiliser pour trouver un fichier stdio.h est la suivante :

​	$ sudo find / -name "stdio.h"

## 10

Pour trouver tous les fichiers dont le nom commence par a ou A, nous pouvons utiliser : 

​	$ find -name "[Aa]*" -print

## 11

Pour répondre à l'exercice, nous pouvons utiliser : 

​	$ find - newer <fichier> -print

## 12

Pour supprimer les fichiers.o nous pouvons utiliser : 

​	$ find -name "*.o" -delete

## 13

Nous savons que drwxr-xr-x indique que 4 stouch staff est un répertoire.  Les droits d’accès y sont    divisés en 3 groupes: rwx r-x r-x correspondent respectivement aux droits de propriétaire, des groupes et des autres.

r étant read

w étant write

x étant exécution

Pour modifier les droits d'accès nous pouvons utiliser la commande chmod.

​	$ chmod og -r fichier ==> interdit aux groupes et aux autres de lire les fichiers

​	$ chmod og-x fichier ==> interdit aux groupes et aux autres d'exécuter

## 14

Pour créer un fichier, nous pouvons utiliser la commande touch :

​	$ touch Hello.txt 

Pour vérifier que le fichier ait bien été crée nous pouvons utiliser la commande :

​	$ ls -l Hello.txt

Ensuite, pour écrire dans le fichier nous pouvons faire :

​	echo "Hello World" >> Hello.txt

	## 15

La commande Cat va permettre de lire dans le fichier Hello 

La commande grep -v va afficher toutes les lignes du fichier ne contenant pas la chaîne de caractère

La commande wc -l va afficher le nombre de lignes 

## 16

1. Placer-vous dans votre répertoire de connexion. Il faut utiliser la commande : cd

2. Créer des répertoires ./tp/system. Nous pouvons utiliser la commande :

   mkdir ./tp/system

3. Placer-vous dans le répertoire système qui vient d'être crée. Nous pouvons utiliser la commande :

   ​	cd /tmp/system

4. Créer un fichier vide nommé Makefile. Pour ce faire nous pouvons utiliser la commande :

   ​	touch Makefile.txt

5. Copier un répertoire /usr/share/vim.  D'abord il faut que je me place dans ce répertoire, soit ;

   ​	cd /usr/share/vim 

   Ensuite, pour le copier je peux utiliser la commande : 

   ​	cp -pr * ../

6. Supprimer le fichier makefile. On peut utiliser la commande :

   ​	rm Makefile

## 17

La commande ps permet de visualiser les processus machines en cours d'exécution.

La commande ps -ef. L'option -e, qui signifie every permet d'afficher tous les processus, tandis que l'option -f permet d'afficher l'ensemble des informations disponibles par ps.

## 18

Pour trouver le nombre de programme qui sont en cours d'exécution, nous pouvons utiliser :

​	ps -ef (ou ps- aux) qui répertorie les processus en cours d'exécution

Nous pourrions également (si on veut plus de détails) utiliser la commande :

​	ps -e -o pid,comm,etime qui affiche le temps depuis lequel les différents processus actifs ont démarés.



Le nombre trouvé ne correspond pas à la sortie de la commande ps, car la commande ps affiche les processus machine qui seront plus détaillés par ps -ef