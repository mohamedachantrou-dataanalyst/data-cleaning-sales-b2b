# Nettoyage et préparation des données d'un base de ventes B2B

## Contexte

Dans les environnements réels d’entreprise, les données brutes sont rarement directement exploitables.
Les jeux de données de ventes contiennent souvent des incohérences, des problèmes de formatage, des valeurs manquantes ou encore des enregistrements dupliqués qui peuvent impacter la qualité des analyses et la prise de décision.

Ce projet vise à nettoyer et préparer un **jeu de données de ventes B2B** afin d'améliorer la **qualité des données (Data Quality)** avant les étapes suivantes du cycle de la donnée, telles que l'analyse, la visualisation ou la modélisation.

Assurer une bonne qualité des données est une étape essentielles, car des données incorrectes ou incohérentes peuvent conduire à des analyses erronées et à de mauvaises décisions métier.

Le dataset utilisé dans ce projet contient plus de **10 000 commandes B2B**.

Colonnes :

``order_id``
``customer_name``
``region``
``product``
``order_date``
``quantity``
``unit_price``
``currency``
``status``

---

## Objectif

Nettoyer et préparer les données afin de les rendre exploitables pour les étapes futures (analyse, reporting, etc.).

---

## Structure du Repository

*(à compléter)*

---

# Étapes du projet

## 1. Exploratory Data Analysis (EDA)

Exploration du dataset afin d’identifier :

- incohérences
- problèmes de standardisation
- valeurs aberrantes
- valeurs manquantes

---

## 2. Data Cleaning

### 2.1 Suppression des doublons

Identification et suppression des lignes dupliquées.

### 2.2 Standardisation des données

- suppression des espaces
- suppression des caractères non désirés
- standardisation des valeurs
- conversion vers le bon type de données

### 2.3 Gestion des valeurs aberrantes

Correction ou remplacement des valeurs impossibles (dates, quantités négatives, etc.) en respectant la logique métier.

### 2.4 Gestion des valeurs manquantes (NaN)

- remplacement par valeurs cohérentes
- "Unknown" pour certaines catégories
- médiane pour limiter l’impact statistique

### 2.5 Post-cleaning validation

Vérification :

- doublons
- NaN
- types de données
- formatage
- valeurs aberrantes

---

# Résultats

- Dataset initial : **10 200 lignes**, dont **200 doublons**
- Réduction d’environ **12 %**
- Colonnes initialement de type **object**
- Conversion vers les **bons types de données**
- Plus de **11 % de valeurs manquantes** initialement
- Après nettoyage : **0 NaN**
- Données **standardisées et sans valeurs aberrantes**

Dataset prêt pour les étapes d’analyse.
