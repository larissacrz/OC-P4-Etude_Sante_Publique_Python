# P4 - Réaliser une étude de Santé Publique avec Python

Projet réalisé dans le cadre de la formation Data Analyst (OpenClassrooms)

## Sommaire

- [Introduction](#introduction)
- [Jeux de données](#jeux-de-données)
- [Analyse](#analyse)
- [Analyse complémentaire](#analyse-complémentaire)
- [Conclusion](#conclusion)
- [Compétences mobilisées](#compétences-mobilisées)
- [Stack technique](#stack-technique)

## Introduction

### Mission 

Contribution à une étude portant sur l’alimentation mondiale, et plus particulièrement sur la problématique de la sous-nutrition.

### Organisme

Organisation des Nations Unies pour l’alimentation et l’agriculture (FAO), dont l’objectif est de contribuer à un monde libéré de la faim.

### Contexte

Le projet s’appuie sur quatre jeux de données couvrant la disponibilité alimentaire, la population, la sous-nutrition et l’aide alimentaire.

### Objectif

Réaliser différentes analyses sur la période 2013–2017 à partir des données disponibles.

### Méthodologie

Le travail est structuré en deux notebooks :

[Notebook 1 : Préparation des données](/notebooks/OC_P4_N1_nettoyage&preparation.ipynb)
>
Nettoyage, standardisation, traitement des valeurs manquantes, harmonisation des unités et création de variables dérivées.  

[Notebook 2 : Analyse](/notebooks/OC_P4_N2_analyse.ipynb)

Analyse des données afin de répondre aux problématiques liées à la faim dans le monde.

<hr/>

## Jeux de données

### Fichier Aide Alimentaire

**Description** : Ce dataset présente les quantités d’aide alimentaire reçues par 76 pays bénéficiaires entre 2013 et 2016. Les quantités sont exprimées en kg.

Après traitement, ce dataframe conserve 1475 enregistrements et 4 colonnes.

### Fichier Disponibilité Alimentaire

**Description** : Ce dataset présente la disponibilité alimentaire en 2017 pour 174 pays et 98 produits d'origine végétale et animale. Les quantités sont exprimées en kg ou en kcal.

Initialement : 15605 enregistrements et 18 colonnes. 
Après traitement: 15605 enregistrements et 19 colonnes.

### Fichier Population

**Description** : Ce dataset présente la population totale de 174 pays pour une année donnée, entre 2013 et 2018. 

Après traitement, ce dataframe conserve 1416 enregistrements et 3 colonnes.

### Fichier Sous-Nutrition

Description : Ce dataset présente nombre moyen de personnes en sous-alimentation sur trois années, en millions d’habitants. 

Initialement : 1218 enregistrements et 3 colonnes. 
Après traitement : 1218 enregistrements et 6 colonnes.

## Remarque

Les traitements appliqués incluent principalement :
* standardisation des variables textuelles ;  
* harmonisation des unités ;  
* gestion des valeurs manquantes ;  
* création de variables dérivées.

<hr/>

## Analyse

### 1. Proportion de personnes en sous nutrition en 2017

**Résultats** :
* Période : année 2017
* Population totale : 7,5 Milliards de personnes
* Population sous-nutrition : 535,7 Millions de personnes
* Indicateur clé : **Taux de sous-nutrition mondial en 2017 de ~7,1 %**
<hr/>

### 2. Nombre de personnes qui en théorie pourraient être nourries

**Résultat** :
* Avec la disponibilité alimentaire mondiale en 2017, il serait théoriquement possible de nourrir environ **9,1 milliards de personnes**, soit, 121% de la population mondiale, sur la base de 2300 kcal par personne et par jour. 
<hr/>

### 3. Nombre de personnes qui en théorie pourraient être nourries avec les produits végétaux

**Résultat** :
* La disponibilité alimentaire mondiale de produits végétaux en 2017 permettait théoriquement de nourrir environ **7,5 milliards de personnes**, sur la base d'un besoin de 2300 kcal par jour, soit 100% de la population mondiale de cette année.
<hr/>

### 4. Utilisation de la disponibilité intérieure

<img src='/charts/3.4_proportion_utilisation_dispo_interieure.png'></img>

**Résultats** :
* 50% de la disponibilité alimentaire intérieure totale est utilisée dans la nourriture ; 
* 22% dans le traitement ;
* 13% dans l'alimentation animale ;
* les 16% restant se distribuent entre pertes, semences et autres utilisations.
<hr/>

### 5. Utilisation des céréales

<img src='/charts/3.5_utilisation_cereales.png'></img>

**Résultat** :
* Le riz est majoritairement consommé par les humains.
* À l’inverse, l'avoine est principalement destinée à l'alimentation animale.
<hr/>

### 6. Pays avec la proportion de personnes sous-alimentées la plus forte en 2017

<img src='/charts/3.6_top_10_pays_pct_sous_nutrition_eleve_2017.png'></img>

**Résultat** : 
* Près de 48% de la population d'Haïti en état de sous-nutrition en 2017, l’un des taux les plus élevés au monde.
<hr/>

## 7. Pays qui ont le plus bénéficié d'aide alimentaire depuis 2013

<img src='/charts/3.7_top_10_pays_plus_aide_alimentaire_depuis_2013.png'></img>

**Résultat** :

* L’aide alimentaire est très concentrée sur un petit nombre de pays (distribution très asymétrique).
* La Syrie est le pays ayant reçu le plus d’aide alimentaire cumulée entre 2013 et 2016.
<hr/>

### 8. Evolution des 5 pays qui ont le plus bénéficié de l'aide alimentaire entre 2013 et 2016

<img src='/charts/3.8_evolution_5_pays_aide_alimentaire.png'></img>

**Résultat** :
Le graphique montre une forte variation de l’aide alimentaire entre 2013 et 2016 pour les cinq principaux bénéficiaires :
* L'Ethiopie est le principal bénéficiaire en 2013, mais son aide diminue fortement dès 2014 jusqu'à disparaître en 2015.
* À partir de 2014, la Syrie devient le premier bénéficiaire avant d'être dépassée par le Yémen en 2016, qui connaît la progression la plus marquée sur la période.
* Le Soudan du Sud présente une hausse importante en 2014. 
* Seuls la Syrie et le Yémen continuent de bénéficier d'une aide alimentaire jusqu'en 2016.
<hr/>

### 9. Distribution des pays selon la disponibilité par habitant : top et bottom 10

Visualisation de la disponibilité des extrêmes dans le monde
<img src='/charts/carte_disponibilite_alim_calories.png'></img>

Pays avec le moins de disponibilité par habitant
<img src='/charts/3.9_10_pays_faible_disponibilite_alimentaire_2017.png'></img>

**Résultat** :
La République Centrafricaine et la Zambie disposent de moins de 2000 kcal par personne par jour.
<hr/>

Pays avec le plus de disponibilité par habitant
<img src='/charts/3.10_10_pays_forte_disponibilite_alimentaire_2017.png'></img>

**Résultat** :
* L’Autriche dispose du nombre de calories le
plus élevé en 2017 (3700 kcal journalière par personne).
<hr/>

### 10. Exemple de la Thaïlande pour le manioc

* Zone : Thaïlande
* Population : 69,2 millions d'habitants
* Sous nutrition : 6,2 millions d'habitants
* Taux sous-nutrition	: 8.96%
* Exportation manioc : 25,2 milliards de kg
* Production manioc : 30,2 milliards de kg
* Taux d'exportation : 83%					

<img src='/charts/3.11_repartition_usages_interieur_manioc.png'></img>

**Résultat** :

En 2017, la Thaïlande présente un taux de sous-alimentation d'environ 9%, malgré une disponibilité alimentaire intérieure moyenne de 2785 kcal par personne et par jour.

Bien que la production nationale du manioc soit importante, elle est majoritairement orientée vers l'exportation (83%) et d'autres usages (alimentation animale et transformation), tandis que l'alimentation humaine directe reste minoritaire (14%).

La Thaïlande importe également une faible part de manioc (4 % de la production).

<hr/>

## Analyse complémentaire

### Relation entre disponibilité calorique et taux de sous-nutrition

Comparaison de la distribution des disponibilités alimentaires mondiale et des pays sans sous-nutrition

<img src='/charts/4.1.2_Comparaison de la distribution des disponibilités alimentaires.png'></img>

**Résultat** :
* Les pays sans sous-nutrition présentent une disponibilité alimentaire globalement plus élevée que la population mondiale.
* Cependant, les deux distributions restent fortement chevauchantes, ce qui indique qu’il n’existe pas de séparation nette entre les deux groupes.
* La sous-nutrition ne correspond donc pas à un seuil strict de disponibilité alimentaire, mais dépend d’un ensemble de facteurs.

## Conclusion

* La disponibilité calorique mondiale semble suffisante pour couvrir les besoins théoriques de la population, mais 7,1 % de la population mondiale reste en situation de sous-nutrition.
* D’importantes disparités existent entre pays, ce qui montre que la disponibilité alimentaire seule n’explique pas les situations de faim.
* D'autres facteurs non présents dans le jeu de données comme l'accès économique, les inégalités, les conflits, les infrastructures ou la qualité nutritionnelle des aliments pourraient également jouer un rôle non négligeable.

<hr/>

## Compétences mobilisées

* Nettoyage et préparation de données
* Contrôle de la qualité des données
* Transformation et standardisation des données
* Analyse exploratoire de données
* Création d'indicateurs statistiques
* Visualisation de données
* Interprétation et communication des résultats

## Stack technique

Environnement : VS Code, Jupyter Notebook
Langage : Python 3.11.9
Bibliothèques : pandas, numpy, matplotlib, seaborn

**Règlement général sur la protection des données** :
Le RGPD n’est pas directement applicable dans ce projet, car les données de la FAO sont agrégées au niveau des pays et ne permettent pas d’identifier des individus. Le RGPD concerne principalement les données personnelles à caractère individuel.