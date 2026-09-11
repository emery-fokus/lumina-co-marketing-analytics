# Lumina & Co — Data Marketing (DIA2)

Analyse du CRM de Lumina & Co (cosmétiques) : nettoyage, EDA, segmentation client et attribution multicanal, sur trois journées de travail — en vue d'une restitution de 10 minutes au CMO.

## Contexte

Le CMO de Lumina & Co veut savoir *"qui sont nos clients ?"* — pas en termes démographiques vagues, mais en segments actionnables avec des recommandations concrètes. Deux fichiers CRM bruts (`customers.csv`, `transactions.csv`) servent de point de départ, avec leurs imperfections habituelles (valeurs manquantes, doublons, anomalies).

## Contenu

### [TP1 - EDA & Nettoyage du dataset Lumina & Co.ipynb](<TP1 - EDA & Nettoyage du dataset Lumina & Co.ipynb>)
- Diagnostic complet des deux fichiers (volumétrie, valeurs manquantes, types, doublons) et data quality report.
- Détection et traitement documenté de chaque anomalie (customer_id manquants, quantités négatives, prix à zéro, codes produits non-produits...).
- EDA orientée marketing : distribution des paniers, loi de Pareto, saisonnalité, biais géographique, corrélations, catégories produit, données zero-party.
- 5 hypothèses marketing formulées pour être testées par la segmentation.

Consigne d'origine : [TP1 - EDA & Nettoyage du dataset Lumina & Co.md](<TP1 - EDA & Nettoyage du dataset Lumina & Co.md>)

### [TP2 - Segmentation RFM & Lumina & Co.ipynb](<TP2 - Segmentation RFM & Lumina & Co.ipynb>)
- Construction des features RFM (Récence, Fréquence, Montant) à partir des transactions nettoyées, avec une snapshot date fixe.
- Scoring par quintiles et segmentation complète en 8 segments nommés, couvrant 100 % de la base, avec seuils justifiés.
- Visualisations : distribution des scores, matrice RFM, scatter récence × montant par segment.
- Fiches de recommandation par segment (qui, potentiel, risque, action) et priorisation avec budget différencié.
- Bonus : adaptation de la méthode à une petite base, croisement RFM × données zero-party.

Consigne d'origine : [TP2 - Segmentation RFM & Lumina & Co.pdf](<TP2 - Segmentation RFM & Lumina & Co.pdf>)

### [TP3 - KPIs par canal - Lumina & Co.ipynb](<TP3 - KPIs par canal - Lumina & Co.ipynb>)
- CAC, CPA, ROAS et taux de conversion par canal marketing, à partir de `campaigns.csv` et `touchpoints.csv`.
- Réconciliation des deux fichiers, détection des primo-achats (méthode : date de facture vs `first_purchase`) pour isoler le CAC du CPA.
- Discussion des vanity metrics, et du fait que `display`/`social` totalisent 58 % du volume de contacts mais 0 conversion mesurée en dernier-clic.
- Bonus : estimation de la CLTV par canal et ratio LTV:CAC.

### [TP3 - Attribution Multicanal - Lumina & Co.ipynb](<TP3 - Attribution Multicanal - Lumina & Co.ipynb>)
- Comparaison des modèles d'attribution *first touch* et *last touch*, avec répartition du crédit de conversion par canal (% et valeur).
- Mise en évidence d'une séparation quasi parfaite entre canaux de découverte (`display`, `social`) et canaux de closing (`affiliate`, `retargeting`, `direct`, `email`, `search_paid`).
- Limite de données documentée : troncature des parcours convertis (effet de fenêtre d'observation), avec impact chiffré sur la fiabilité du *first touch*.
- Recommandation argumentée : modèle multi-touch plutôt qu'un modèle à un seul point de contact.

Consigne d'origine : [TP3 - Attribution Multicanal Lumina & Co - v2.pdf](<TP3 - Attribution Multicanal Lumina & Co - v2.pdf>)

## Présentation finale

Restitution de 10 minutes au CMO (+ 10 minutes de questions), couvrant : contexte et problématique, segmentation client, KPIs de campagne et attribution, synthèse et plan d'action, limites et confiance dans la data — avec la logique WHAT? → SO WHAT? → NOW WHAT? comme fil conducteur (méthode détaillée dans [DATA STORYTELLING - DIA2 - septembre 2026 (V2).pdf](<DATA STORYTELLING -  DIA2 - septembre 2026 (V2).pdf>)).

## Données

Les fichiers CRM bruts (`customers.csv`, `transactions.csv`, `touchpoints.csv`, `campaigns.csv`) ne sont pas inclus dans ce repo (taille > limite GitHub pour certains). Les notebooks contiennent toutes les sorties déjà calculées.
