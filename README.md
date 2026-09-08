# Lumina & Co — Data Marketing (DIA2)

Analyse du CRM de Lumina & Co (cosmétiques) : nettoyage, EDA et segmentation client, sur deux journées de travail.

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

## Données

Les fichiers CRM bruts (`customers.csv`, `transactions.csv`, `touchpoints.csv`, `campaigns.csv`) ne sont pas inclus dans ce repo (taille > limite GitHub pour certains). Les notebooks contiennent toutes les sorties déjà calculées.
