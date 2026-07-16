# 🛒 Analyse de l'Inflation & Évolution du Panier de la Ménagère à Abidjan (2021-2026)

[![Dashboard](https://img.shields.io/badge/Dashboard-Power%20BI-orange?style=flat-square&logo=microsoftpowerbi)](https://votre-lien-dashboard.com)
[![Python](https://img.shields.io/badge/Language-Python%203.9-blue?style=flat-square&logo=python)](./notebooks/)
[![Données](https://img.shields.io/badge/Data-INS%20%2F%20BCEAO-green?style=flat-square)](./data/)

## 🎯 Problématique Métier & Contexte Économique

L'inflation et la cherté de la vie sont au cœur des préoccupations économiques en Côte d'Ivoire. Pour les acteurs de la grande distribution (Prosuma, Carrefour, CDCI Playce, Chic shop), les entreprises agroalimentaires et les décideurs publics, comprendre comment la hausse des prix affecte le pouvoir d'achat des ménages ivoirien est un enjeu stratégique majeur.

**L'objectif de ce projet** est d'analyser la dynamique de l'Indice des Prix à la Consommation (IPC) et de modéliser l'évolution du "panier de la ménagère" à Abidjan afin de :
1. **Identifier les postes de dépenses les plus inflationnistes** (produits alimentaires, transport, logement).
2. **Mesurer l'impact de l'inflation sur le budget des ménages** selon leur niveau de revenu (effet de substitution).
3. **Prédire l'évolution des prix à court terme** pour aider les entreprises à ajuster leurs stratégies de tarification (pricing).

---

## 💡 Approche Économique & Concepts Clés

Ce projet applique des théories micro et macroéconomiques fondamentales pour donner du sens aux données :
* **Théorie du Consommateur & Effet de Substitution :** Analyse de la manière dont les ménages ivoiriens réallouent leur budget vers des biens inférieurs (ex: substitution de produits importés par des produits locaux) lorsque l'inflation globale augmente.
* **Indice de Laspeyres :** Compréhension de la méthodologie de calcul de l'IPC national utilisée par l'Institut National de la Statistique (INS) de Côte d'Ivoire.
* **Analyse de Séries Temporelles :** Modélisation de la saisonnalité des prix agricoles (périodes de soudure, saisons des pluies impactant l'approvisionnement des marchés comme le marché Gouro à Adjamé).

---

## 🛠️ Stack Technique

* **Collecte & Intégration :** Python / Pandas (Extraction et fusion de données historiques de l'INS Côte d'Ivoire, de la BCEAO et de la Banque Mondiale).
* **Analyse Quantitative & Forecasting :** 
  * Python (Statsmodels, Scikit-Learn) pour l'analyse de saisonnalité.
  * Modèle **ARIMA / SARIMAX** pour la prévision de l'indice des prix alimentaires à 6 mois.
* **Visualisation (Data Storytelling) :** Microsoft Power BI (ou Streamlit) pour concevoir un simulateur d'impact budgétaire.

---

## 📈 Résultats & Insights Clés (Exemples)

* **Le Moteur de l'Inflation :** Les produits alimentaires (principalement l'huile de palme, le riz importé et le poisson congelé) représentent plus de 60% de la contribution à l'inflation globale constatée en Côte d'Ivoire sur la période étudiée.
* **Saisonnalité Marquée :** On observe un pic systématique des prix des produits vivriers locaux (banane de table, manioc, piment) entre mai et juillet, coïncidant avec la grande saison des pluies qui perturbe le transport depuis l'intérieur du pays (Daloa, Gagnoa) vers Abidjan.
* **Performances de Prévision :** Le modèle SARIMAX a permis de prédire l'évolution de l'indice des produits alimentaires avec un taux d'erreur moyen (MAPE) inférieur à 3.2% sur un horizon de 3 mois.

---

## 🖥️ Structure du Dashboard interactif

Le rapport Power BI se structure autour de trois axes :

1. **Observatoire de l'Inflation :** Suivi de l'inflation globale vs inflation sous-jacente en Côte d'Ivoire (normes de convergence de l'UEMOA à 3%).
2. **Simulateur du "Panier de la Ménagère" :** Un outil interactif permettant à l'utilisateur de configurer la composition de son panier mensuel (logement, transport, alimentation) et de visualiser l'évolution réelle de son reste à vivre sur les 3 dernières années.
3. **Section "Prévisions Business" :** Courbes de tendances prévisionnelles par catégorie de produits pour aider les directions d'achats à anticiper les hausses de coûts de leurs matières premières.

---

## 📂 Organisation du Répertoire

```text
├── data/                  # Données INS / BCEAO nettoyées
├── notebooks/             # Notebooks Jupyter (Analyse exploratoire, modèle SARIMAX)
├── src/                   # Scripts Python de traitement automatique des données
├── dashboard/             # Fichier de conception du dashboard (.pbix)
└── README.md              # Présentation du projet
