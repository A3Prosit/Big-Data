
# Prosit 8 : Big Data

- Team :
- Animateur : John
- Secrétaire : Nico
- Scribe : Flo
- Gestionnaire : Max C

##  Mot clés (rien à définir) :

-	Simultanément
-	POC
-	Algorithme
-	Architecture
-	Big Data
-	NoSQL
-	Volume
-	Variété des données


## Contexte :

Quoi ?
-	Intégrer les serveurs en simultané
-	Gérer des gros volumes de données
Comment ?
-	Etude de différentes architectures dans le Big Data
Pourquoi ?
-	Prendre conscience des enjeux du Big Data

## Contraintes :
-	Simultanéité
-	Gros volume de données
-	Données variées

## Problématique :
-	Comment prendre conscience des enjeux du Big Data en pour gérer de gros volumes de données ?
-	Comment mettre en place une architecture de Big Data avec des clusters ?
-	Quels sont les enjeux du big data et comment y répondre ?
Généralisation :

-	Logistique sur gros volumes
-	Organisation de données
-	Conception

## Hypothèses :

-	NoSQL est mieux pour le Big Data
-	Les algorithmes de la th des graphes s’adaptent bien pour le NoSQL
-	On peut faire des clusters en local, ou en cloud selon le volume de données
-	L’exploitation des données récoltées pourrait augmenter l’efficacité le traitement des données obtenues
-	Le Big Data engrange les données
-	Une application Big Data peut utiliser plusieurs archi

## Plan d’action
Études
-	Big Data
  -	Définition
  -	Lexique
  -	Map Reduce
  -	Architecture
  -	Enjeux
-	Techno & Sociétés (Spark & Hadoop)
-	Archi logicielle et matérielle
-	5V

Réalisation
-	Corbeille 2

## Big data 
- Mégadonnées / donées massives
- Aucun outil de BDD ne peuvent travailler.
- Procréation de 2.5 trillions octets de donnéestous les jours
- Concept permettant de stocker un nombre indicible d'informations sur une base numérique.
- Permet aux spéculateurs sur le marché financier de se prononcer (stats)

## Lexique 
- Analyse : Etudier des données pour en dégager des infos et prendre des décisions
- Analyse descriptive : prédiction
- Analyse prescriptive : prédire les décisions à prendre pour un impact maximal (optimiser)
- Batch processing : traiter de larges volumes de données
- Cassandra : SGBD open source géré par Apache. Prend en charge de larges données sur serveurs distribués
- Cloud computing : Logiciels / données hébergées ou lancées sur des serveurs distants,accessibles depuis n'importe où sur internet
- Cluster  computing :ressources provenant sur multiples serverus rassemblées en clusters
- Darkdata : Données rassemblées et traitées par les entreprises qui ne sont pas utilisées dans un but précis. (60 à 90%)
- Data Lake : répertoire où sont stockées de nombreuses données au format brut. Permet de faciliter l'accès au données
- DataWarehouse : Stoackage de données conventionnelles, structurées et formatées.
- DataMining : Trouver des patterns et extraite des infos pertinentes. On utilise des stats, des algos et du marchine learning, de l'IA.
- Data Scientist : Donne un sens au big data, extrait les données bruts du Data Lake, les traite.
- Données structurées ou non structurées : structurées = tableau //  Non structurées = messages, mail, publications, discours, vidéos...
- Système de fichier distribué : stocker de larges volumes sur plusieurs appareils, en réduisant coûts, complexité stockage.
- ETL : Extraire, Transform, Load : Fait réf au processus d'extraction, de transformation par le nettoyage et l'enrichisssement des données pour les rendres utilisables.
- Hadoop : Framework open source Haddop est inextricablement lié au Big Data. Repose sur le système de fichiers distribués Hadoop (HDFS) qui permet le stockage et l'analyse de larges ensembles de données.
- In memory Computing : Technique pour transférer des ensembles de données complets vers la mémoire collective d'un cluster et d'éviter d'écrire descalculs intermédiaires sur le disque
- IoT : Internet Of Things : Connexion entre les appareils électroniques...
- Machine learning : Techno permettant au S.I d'apprendre, de s'ajuster et de s'améliorer grâce aux données
- MapReduce : Modèle de programmation constitué de Map et Reduce
- NoSQL : Not Only SQL : SGB prendre en charge les données de largesvoumes
- R : Langage très utilisé pour le computing statistique
- Spark : Moteur de traitementde données capable d'effectuer des tâches de streaming, Machine learning, requêtes SQL
- Stream processing : Agir en temps réel sur les données à l'aide  de requêtes continues. 
## Map Reduce 
- Décrit en 2004 par Google
- Pattern implémenté dans le projet Nutch de Yahoo
- Algorithme qui dispose d'une grande capacité en matière de stockage
- Assez lent
- Remplacé en 2014 par Google Cloud DataFlow
- MAP: Modèle sépare les ensemble de données en plusieurs partiesafin qu'ils puissent être distribués à différents PC
- Reduce : Collecte less résultats et les réduit en un rapport. Lié au système de fichiers distribués d'Hadoop

ll y a aussi **Spark**
- Bibliothèques de traitement classique
- Performances remarquables
- Sur données de disques ou données en RAM
- S'avère être le successeur de MapREDUCE
- 
## Lambda Architecture
Pour avoir une bonne architecture :
- Gestion de la tolérance aux pannes (loi  de murphy : tout ce qui est suceptible d'aller mal ira mal)
- Maintenabilité : Arhitecture facile à maintenir et à modifier pour les successeurs
- Un coût faible : composants simples, ajustés aux besoins pour minimiser les coûts

## Acteurs  du big data
- Secteurde l'IT :
	- Oracle
	- HP
	- SAP
	- IBM
- Web :
	- Google
	- Facebook
	- Twitter
- Data et Big Data
	- MapR
	- Teradata
	- ECM
	- Hortonworks
	- CapGemini
	- Sopra
	- Accenture
	- Atos
- Analytique (éditeurs, BI)
	- SAS
	- Microstrategy
	- Qlikech
- France : (pionniers)
	- Hurence
	- Dataiku
## Archi materielle / logicielle

## 5V

![](https://www.lebigdata.fr/wp-content/uploads/2015/08/Les5vdubigdata-1024x757.jpg)**- Volume :** Masse d'information produite chaque seconde. 
**- Vélocité :** Rapidité d'élaboration et du déploiement des nouvelles données. Ex : répdnre les infos diffusés sur fb à tous
**- Variété :** Structuration des données (il faut reconnaître et les classer, vidéos, images...)
- **Véracité :** Fiabilité et crédibilité des informations collectées.
- **Valeur**: Profit qu'on puisse tirer de l'usage du Big Data. Selon les gestionnaires et les économistes, ceuxqui ne s'y intéressent pas risquent d'être pénalisés et écartés.

## Enjeux 
- Commercial privilégié
- Capacité à impacter le commerce en profondeur dans l'économie modiale
- Prendre des décision plus véloces et plus crédibles

## Techno & Sociétés (Spark & Hadoop)

## Archi logicielle et matérielle
