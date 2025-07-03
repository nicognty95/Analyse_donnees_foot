# Football Data Science – Analyse et Modélisation avec StatsBomb

## Objectif du projet  
Ce projet a pour but d’explorer et de modéliser des données de match issues d’un format similaire à StatsBomb, afin de réaliser une data science appliquée au football :  
- Analyse exploratoire  
- Visualisations avancées  
- Modélisation prédictive (xG)

## 📂 Structure du projet  
Le notebook Jupyter (compatible Colab) est organisé en quatre grandes parties :

1. **Chargement des données**  
   - Lecture des fichiers JSON (ex. `3788745.json`)  
2. **Nettoyage & préparation**  
   - Extraction des coordonnées, types d’actions, métadonnées (minute, joueur, pression…)  
   - Normalisation & encodage  
3. **Visualisations interactives et analytiques**  
   - **Shot Map** : carte des tirs (taille ∝ xG)  
   - **Timeline xG** : accumulation d’xG au fil du temps  
   - **Réseaux de passes** : flux de passes (> 5 passes) et position moyenne  
   - **Heatmap des réceptions** : zones de réception de balle  
4. **Modélisation prédictive**  
   - **Objectif** : prédire la probabilité qu’un tir devienne but  
   - **Modèle** : `LogisticRegression` dans un pipeline scikit-learn  
   - **Features clés** : coordonnées (x, y), minute, pression, partie du corps  
   - **Évaluation** : `roc_auc_score`

## Données utilisées  
- Données brutes OpenSource (format JSON) similaires à StatsBomb  
- Match anonymisé : `3788745.json`  
- Enrichissements : coordonnées, types d’actions, métadonnées  

## Outils et librairies  
- **Python** (Google Colab)  
- **Pandas** / **NumPy**  
- **Plotly** & **mplsoccer**  
- **scikit-learn** :  
  - `Pipeline`, `ColumnTransformer`, `OneHotEncoder`, `StandardScaler`  
  - `LogisticRegression`  
  - `roc_auc_score`

## Visualisations clés  
- **Shot Map** : représentations des tirs avec xG  
- **Timeline xG** : comparaison des dynamiques offensives  
- **Réseau de passes** : visualisation des connexions  
- **Heatmap des réceptions** : zones d’influence des joueurs  

## Modélisation : Prédiction de but  
1. **Préparation** : sélection et encodage des features  
2. **Entraînement** : régression logistique  
3. **Évaluation** : AUC-ROC, courbes ROC  
4. **Interprétation** : poids des variables, importance des features  

## Conclusion  
- Analyse complète d’un match à partir de données événementielles  
- Visualisations actionnables pour les performances  
- Modèle xG simple, interprétable et extensible  
