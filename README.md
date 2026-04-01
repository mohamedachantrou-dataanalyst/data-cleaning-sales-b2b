# Nettoyage et préparation des données d'une base de ventes B2B

**Secteur :** Sales  

**Outils :** Python · Pandas

**Compétences :** Data Cleaning · Exploratory Data Analysis (EDA) · Data Quality Management · Data Validation · Math & statistics

---

## Contexte

Dans les environnements réels d’entreprise, les données brutes sont rarement directement exploitables.
Les jeux de données de ventes contiennent souvent des incohérences, des problèmes de formatage, des valeurs manquantes ou encore des enregistrements dupliqués qui peuvent impacter la qualité des analyses et la prise de décision.

Ce projet vise à nettoyer et préparer un **jeu de données de ventes B2B** afin d'améliorer la **qualité des données (Data Quality)** avant les étapes suivantes du cycle de la donnée, telles que l'analyse, la visualisation ou la modélisation.

Assurer une bonne qualité des données est une étape essentielles, car des données incorrectes ou incohérentes peuvent conduire à des analyses erronées et à de mauvaises décisions métier.

Le dataset utilisé dans ce projet contient plus de **10 000 commandes B2B**.

**Colonnes :**

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

```
├── README.md
├── SalesB2B_DataCleaning.ipynb                         ← Projet complet détaillé avec toutes les étapes
├── Input/
│   └── DirtySalesB2BDataset.csv
├── Output/
    └── CleanedSalesB2BDataset.xlsx
  
```
---

# Étapes du projet

## 1. Exploratory Data Analysis (EDA)

Exploration du dataset afin d’identifier :

- incohérences
- problèmes de standardisation
- valeurs aberrantes
- valeurs manquantes
- doublons

---

## 2. Data Cleaning

### 2.1 Suppression des doublons

Identification et suppression des lignes dupliquées.

### 2.2 Standardisation des données

- suppression des espaces blancs
- suppression des caractères non désirés
- standardisation des variants de valeurs
- conversion vers le bon type de données

### 2.3 Gestion des valeurs aberrantes

Correction ou remplacement des valeurs impossibles (dates, quantités négatives, etc.) en respectant la logique métier.

### 2.4 Gestion des valeurs manquantes (NaN)

- remplacement par valeurs cohérentes en se basant sur la logique métier
- "Unknown" pour des champs catégoriels
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

| Indicateur | Avant nettoyage | Après nettoyage |
|---|---|---|
| Nombre de lignes | 10 200 | ~ 9 000 **(12% de réduction)** |
| Types de données | Toutes les colonnes en `object` | Conversion vers les types appropriés |
| Valeurs manquantes | > 11 % du dataset | 0 |
| Valeurs manquantes par colonne | entre 10 % et 15 % du dataset | 0 |
| Formatage des données | Incohérences et problèmes de standardisation | Données standardisées |
| Valeurs aberrantes | Présentes | Aucune |

Dataset prêt pour les étapes d’analyse.
