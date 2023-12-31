Le projet fil-rouge a pour but de mettre en pratique les différences compétences et outils que nous avons pu découvrir au cours de notre formation chez Datascientest (formation sur 3 mois - 38h/semaines - Certifiée RNCP36129 (Niveau 7))

Ainsi, notre mission était d'extraire et traiter l'ensemble des offres d'emploi disponibles en France métropolitaine afin de pouvoir les exploiter au travers de DashBoard et de machine learning.
Nous avons donc mis en place l'architecture suivante :
- une partie ETL (Extraction, Transform, Load) :
    - Via des scripts PYTHON, nous avons récupéré toutes les données possibles de l'API de Pôle Emploi.
    - Elles ont ensuite été traitées (suppression des doublons, remplacement des Nan et valeurs manquantes, extraction de données de libellés...)
    - Pour être enrichi via du MACHINE LEARNING avec une simulation du salaire moyen de chacune de ces offres en fonction des 8 critères distincts (Code ROME, localisation, nombre d'année d'expérience...)
    ==> Ces données ont finalement été chargées dans des tables NOSQL du type MONGODB
- Une partie DATAVIZ :
    -  Une fraction de ces données a été utilisée pour alimenter un Dashboard DASH contenant divers graphs :
	- La localisation de chaque offre sur une carte de France ainsi qu'avec un code couleur en fonction de son salaire
    	- Un classement des secteurs d'activité en fonction des salaires proposés
    	- Un classement des secteurs d'activité en fonction de l'expérience demandée
    	- Un récapitulatif des offres affichées en fonction des filtres choisis
- Une partie conteneurisées :
   - Les parties ETL et DATAVIZ ont toutes deux été conteneurisées via DOCKER.

Support de Présentation : [JobMarket.pptx](https://github.com/JYM1987/projet_fil_rouge/files/13677202/JobMarket.pptx)

