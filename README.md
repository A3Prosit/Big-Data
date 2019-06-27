# Prosit 8 : Big Data

Team :
Animateur : John
Secrétaire : Nico
Scribe : Flo
Gestionnaire : Max C

##  Mot clés (rien à définir) :

●	Simultanément
●	POC
●	Algorithme
●	Architecture
●	Big Data
●	NoSQL
●	Volume
●	Variété des données


## Contexte :

Quoi ?
●	Intégrer les serveurs en simultané
●	Gérer des gros volumes de données
Comment ?
●	Etude de différentes architectures dans le Big Data
Pourquoi ?
●	Prendre conscience des enjeux du Big Data

## Contraintes :
●	Simultanéité
●	Gros volume de données
●	Données variées

## Problématique :

●	Comment prendre conscience des enjeux du Big Data en pour gérer de gros volumes de données ?
●	Comment mettre en place une architecture de Big Data avec des clusters ?
●	Quels sont les enjeux du big data et comment y répondre ?
Généralisation :

●	Logistique sur gros volumes
●	Organisation de données
●	Conception

## Hypothèses :

●	NoSQL est mieux pour le Big Data
●	Les algorithmes de la th des graphes s’adaptent bien pour le NoSQL
●	On peut faire des clusters en local, ou en cloud selon le volume de données
●	L’exploitation des données récoltées pourrait augmenter l’efficacité le traitement des données obtenues
●	Le Big Data engrange les données
●	Une application Big Data peut utiliser plusieurs archi

## Plan d’action
Études
## Big Data
### Définition

pas de définition propre encore une fois mais : quand on gère de gros volumes de données.
Inventé par les géants du web le big data se présente comme solution permettant à tt le monde d'accéder en temps réel à des BDD

Il vise à proposer une solution au pb classiques de bdd et d'analyse (la phrase dit proposer un choix aux solutions)

il réponds au 5v (ou 3v) vélocité, volume, variété (et valeur, varacité)

La croissance du big data a été facilité par la croissance de 2 familles de technos: les technos de stockage en particulié le **cloud computing** et les technos de traitement ajustées, en particulié le dvp de **bdd adaptée aux données nn structurées** (Hadoop) et la mise au point de **modes de calcul à haute performance** (MapReduce)

Il y a plusieurs façons d'opti le temps de traitement sur les bases géante : NoSQL, le clustering (traitement parallèle comme Hadoop qui distibue les fichiers avec HDFS, une base NoSQL et l'algo MapReduce)

On s'en sert par exemple pour la spéculation financière autonome 

### Lexique

- analyse descriptive: 
décrire le contenu d'un ensemble de données. Spéarer les données. Par exemple sur un relevé bnaquaire dire que 25% bouffe, 35% loyer, 40% école

- analyse prédictive: 
prédire avec une certaine proba ce qu'il va se passer. Ex: on analyse un relevé de carte sur 5 ans et on peut prédire d'a la fin du mois le loyer va être déduit

- analyse prescriptive:
prédire les décision à prendre pour un impact maximal. Ex: donner les catégorie à viser pour faire des économies

- batch processing : traiter de larges volume. hadoop est focalisé sur le batch processing de données

- cassandra: système de gestion de bdd opensource d'apache

- cloud computing: logiciels ou données sur des serv distants accessibles via le net

- cluster computing: on regroupe les données de plusieurs serv en cluster et on ravail avec

- dark data: données rassembléeset traitées par les entreprises qui ne sont pas utilisées par la suite dans un but précis

- data lake: répertoire de données brutes

- data warehouse : stockage de données structurées et formatées

- data mining : permet de trouver des patterns et extraire des infos pertinentes vennant de large sources de données à l'aide de parttern matching

- data scientist: donne un sens au big data en extrayant les data du data lake et les traitant

- ETL: extract, transform, load. processus d'extraction de données brutes, transfo par nettoyage et enrichissement des données pour les rendre utilisables et chargement de ces données au sein du répertoire aproprié pour l'utilisation du système. De base on en parlait pour les data warehouses mais mtn on s'en sert pour toutes les sources

- Hadoop: framework opensourfe se basant sur le système de fichier distribué Hadoop (HDFS) et permettant le stockage et l'analyse de larges ensembles de data par le biais d'hardware distribué

- In-memory computing : technique permettant de tranférer des ensembles de données complets vers la mémoire collective d'un cluster et évite les calcules intermédiaires sur le disque.

- machine learning: techno permettant aux systèmes info d'apprendre, s'ajuster et s'améliorer grâce aux données

- mapreduce: modèle de prog utilisant Map et Reduce (y). Map sépare le modèle pour les distribuer et après processing, reduce récup les résultats et les réduit en un rapport

- Spark : moteur de traitement de données pouvant effectuer les tâches en streaming, faire du machine learning ou faire des requpete SQL nécessitant un accès itératif rapide

- stream processing: permet d'agir en temps réel sur les données à l'aide de requêtes continues quand combiné avec les streaming analytics

### Map Reduce

en 2014 google a annoncé que MapReduce sera succédé par Google Cloud DataFlow

le job à faire doit pouvoir être mapé 

on coupe les data en groupes, on traite en // et on regroupe

ex: word count. on coupe la liste et on la map, on compte séparément, et on reduce: on fait la somme 

note: on move vraiment la data on la map juste pas puis on envoie le mapping, on envoie sur chaque node (c'est auto)

on compute là où la data est stockée (pour gagner du temps)

pas très flexible, on doit pouvoir map et reduce, on doit pouvoir pairer clé:valeur

on peut pas vraiment réutilser la donées donc itérer, donc bof pour par exemple kmeans

dans ce genre de cas on utilise spark

### Spark

plus flexible que mapreduce

quand utiliser : process des donées quine rentrent pas sur une sele node ou besoin d itérer

resilient distributed dataset : rdd: collection des objets spread sur le cluster mais quand on prog cest abstrait donc on a l'illusion que c'est sur 1 seul node

on a 1 driver node et des workers : driver run le main program avec les transfo et on envoie ax workers
spark fait aussi du map reduce
on a filter

RDD: resilient distributed dataset
rdd sont immutalbe: cannot be changed
spark est donc une chaine de tranfo qui créé de nouvelles rdd et se les passe
l'avantage est qu'on les garde et on peut donc les réutiliser contrairement à map reduce qui le stock sur le disque

### Architecture

### Enjeux

### Technologies et sociétés

apache, projets hadoop et spark
classiques : Oracle, HP, SAP, IBM, 
web : Google, Facebook, Twitter
spécialistes du big data : MapR, Teradata, EMC ou Hortonworks
companies aux: capgemini, sopra, accenture, Atos
BI: SAS, Micro-strategy, Qliktech

## Techno & Sociétés (Spark & Hadoop)

Hadoop distibue les fichiers avec HDFS, une base NoSQL et l'algo MapReduce

spark : 
solution permettant d'écrire simplement des app distribuées et proposant des lib de traitement classiqe. Il peut travailler sur des données sur disque ou en RAM


## Archi logicielle et matérielle

## 5V

2001 y en avait 3

- **Volume:** quantité de donnée
- **Vélocité:** vitesse à laquelle on créé de la data
- **Variété:** à quel point la data est variée (like, vue, image, audio, valeur d'un capteur)
- **Valeur:** patern dans la data?
- **Veracité:** a quelle point le donnée est "vraie" : data biaisée? erreur sur des capteurs? 

Réalisation
●	Corbeille 2
