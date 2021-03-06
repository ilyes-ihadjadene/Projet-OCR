PROJET FDP OCR
==============

Le FDP OCR est un programme sur lequel les intervenants de Platypus
pourront déposer les feuilles de présence (un scan ou une photo de bonne
qualité) des cours où ils interviennent. Plutôt que de saisir manuellement les
informations contenues sur la feuille, qui est en soit une tâche extrêmement
chronophage à l’échelle de la société Platypus en plus d’être propice aux
erreurs et aux oublis, le FDP OCR scannera directement le contenu de la
feuille et en extirpera toutes les données grâce aux dernières technologies de
reconnaissance de Google dans le cadre de l’analyse et de l’extraction de
données imprimées et manuscrites. Ces informations seront ensuite traitées puis
intégrées à la plateforme de dépôt des PV de l’entreprise et permettront le
suivi administratif (absences, retards, ajout ou retrait d’un étudiant dans un
groupe de travail pour permettre la mise à jour des listes...), mais aussi
pédagogique (suivi de l’assiduité, recensement des points de participation...)
des nombreux élèves qui suivent un enseignement made in Platypus !


Interface du projet
-------------------

L'envoi des fichiers se fera via une plateforme Web

![Screen plateforme](pages/screen.png)

Sorti du programme
------------------

Le projet sortira un fichier JSON qui suivra cette syntaxe :

```
[
	{
metadata : {
	id : 0B7mNn544KuPGaE9CbDNINFJWUlU,
	title :’2017 09 19 - ESIEA 2A SDD - TD 6_30 2B1 - FRANCK’,
},
header : {
	activity : ‘TI102-TD/…’,
	session :  ‘Mercredi 20 … E36’,
	assignments : {
		teacher : ‘LEPOIVRE, Franck’,
		students_group : // laisser vide en première approche }
		signature : true
	},
students : [
	{
		name : ABITTAN David,
		status : P,
		bonus : 1
	},
	...
],
free_part : tout ce qui ne rentre pas dans les champs précédents.		
}]
```

TODO LIST
---------

* [x]  Ecriture du 'header'
	* [x] lesson
	* [x] teacher
	* [x] date
	* [x]  school
* [x]  Ecriture de la liste des 'students'
	* [x] liste des etudiants
	* [x] suppresion du professeur s'il est inclus
* [ ] Ecriture des 'metadata'
	* [ ] id
	* [ ] title
* [ ] Ecriture des informations non utilsées
