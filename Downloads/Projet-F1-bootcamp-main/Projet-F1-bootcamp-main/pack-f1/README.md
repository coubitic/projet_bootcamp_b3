# Projet transversal F1 — Python → Java → JavaScript

Explication du projet, du raisonnement pour chaque fonctions, etc.

## 01 - Python

La première fonction permet de convertir un chronomètre de format minute:secondes à un nombre de secondes en float. Le processus est simple: on utilise un split pour obtenir 2 variables différentes représentant respectivement le nombre de minutes (int) et le nombre de secondes (float), nous permettant de faire le calcul et d'obtenir un résultat final en float.

La deuxième fonction a pour but d'ouvrir le fichier csv brut et d'en faire une liste de dictionnaires. On importe donc le module csv qui est directement built in dans python et qui permet en l'occurence avec csv.reader de transformer chaque ligne du fichier csv en tableau. Ainsi pour créer le dictionnaire on fait une boucle qui parcourt chaque tableau représentant chacun une ligne du csv, et qui les envoie à leur bonne place dans le dictionnaire.

Pour la troisième option qui a pour but de ré-écrire un nouveau fichier csv au propre, on réutilise une fonction du module csv, ici csv.writer . Dans chaque ligne du nouveau fichier csv créé, on parcourt le dictionnaire créé lors de la fonction précédente pour y ranger les informations dans la ligne correspondante du fichier csv, grace à la clé ligne.



## 02 - Java

La première fonction permet d'accorder le bon nombre de points aux pilotes en fonctions de leur position. On sait qu'un abandon équivaut à la position 0, et que les pilotes terminant en dehors du top 10 ne recoivent aucun point. On crée donc une condition pour vérifier que la position du pilote se trouve entre 1 et 10 inclus, et dans le cas échéant il reçoit 0 point. Pour les pilotes ayant fini entre la 1ère et la 10ème place, on utilise simplement le tableau qui liste les points, en utilisant la position du pilote comme index (sans oublier de faire -1 sur la position étant donné que l'index dans un tableau commence à 0).

Pour la 2ème fonction qui permettait d'établir un classement des pilotes, je suis resté bloqué pendant 30 minutes à me torturer l'esprit dessus alors pour ne pas rester bloqué et faire la suite j'ai demandé à Timothée de me donner sa fonction.

En partant de cette fonction j'ai réussi à aboutir à la 3ème qui repose essentiellement sur les mêmes principes et qui permet cette fois ci d'établir un classement des écuries.

Enfin, la dernière fonction permettant de calculer la moyenne des résultats des pilotes parcourt la liste vérifie que le pilote a bien terminé la course (position supérieure à 0), et dans ce cas ajoute la position à un compteur total, compteur qui sera par la suite divisé par le nombre de courses terminées par le pilote pour obtenir la moyenne de ses positions. (le compteur courses ne prend également pas en compte les courses abandonnées).



## 03 - JavaScript

La première fonction commence par créer une copie de la liste pour ne pas modifier l'originale. Ensuite, le tri est fait en 2 temps: grâce à une condition, on vérifie que 2 pilotes comparés ne sont pas égaux en nombre de points. Tant qu'ils ne le sont pas, ils sont donc triés en fonction de leur nombre de points, mais dans le cas échéant, ils sont départagés par le nombre de victoires.

La deuxième fonction fait une boucle qui remplit le classement des pilotes ligne par ligne. Le classement sera d'office dans le bon ordre étant donné qu'il utilise la liste triée créée dans la fonction précédente.
 
Enfin, la dernière fonction parcourt simplement le tableau qui était déjà utilisé dans la 2ème fonction, et applique le style css podium aux 3 premiers éléments du tableau, synonyme de podium.
