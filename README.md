Football Data Science – Analyse et Modélisation avec StatsBomb

Objectif du projet :
Ce projet a pour but d'explorer et de modéliser des données de match issues de la plateforme StatsBomb, dans une optique de data science appliquée au football. Il mêle analyse exploratoire, visualisations avancées, et modélisation prédictive pour mieux comprendre les dynamiques de match, les performances des joueurs, et la qualité des tirs (xG).

📂 Structure du projet
Le projet est codé dans un notebook Jupyter, compatible Colab, et comprend les sections suivantes :

- Chargement des données StatsBomb (.json)

- Nettoyage et préparation des données

- Visualisations interactives et analytiques :

- Cartes de tirs (Shot Maps)

- Timelines xG

- Réseaux de passes

- Heatmaps des réceptions de balle

Modélisation prédictive :

- Modèle de prédiction de but à partir d’un tir (xG model simple)

- Pipeline de machine learning scikit-learn

- Analyse des performances du modèle

Données utilisées
- Données brutes issues de la base StatsBomb, en format JSON.

- Match anonymisé contenu dans le fichier 3788745.json.

- Données enrichies en extrayant notamment :

- Les coordonnées des événements (location)

- Les types d’action (tir, passe, réception, etc.)

- Les métadonnées associées (minute, joueur, pression, etc.)
Outils et librairies
- Python (via Google Colab)

- Pandas / NumPy pour la manipulation des données

- Plotly et mplsoccer pour les visualisations sportives (terrains, réseaux, heatmaps)

- scikit-learn pour la modélisation :

- LogisticRegression (prédiction de but)

- Pipeline, ColumnTransformer, OneHotEncoder, StandardScaler

- roc_auc_score pour évaluer la qualité du modèle

📊 Visualisations clés
- Shot Map (Carte des tirs)
Représente tous les tirs effectués, avec la taille des points proportionnelle à leur xG (expected goals).

Affichable par équipe.

- Timeline xG
Évolution de l’accumulation d’xG au fil du match.

Permet de comparer les dynamiques offensives des deux équipes.

- Réseau de passes
Montre les connexions fréquentes entre les joueurs d’une même équipe.

Représentation positionnelle moyenne et flux de passes (>5 passes).

- Heatmap des réceptions
Carte de chaleur des ballons reçus sur le terrain.

Permet d’identifier les zones d’activité principales.

- Modélisation : Prédiction de but
Un modèle de régression logistique est entraîné pour prédire la probabilité qu’un tir se transforme en but. Les variables explicatives incluent :

- Coordonnées du tir (x, y)

- Minute de jeu

- Pression adverse

- Partie du corps utilisée

Choix méthodologiques :
- Utilisation de features simples mais pertinentes pour le modèle de tir (pas de deep learning, modèle interprétable).

- Visualisations faites avec mplsoccer, spécialisé dans le football.

- Normalisation et encodage via pipelines pour reproductibilité.

- Filtrage des passes ou tirs par équipe pour analyses ciblées.

Conclusion :

Ce projet a permis :

- Une analyse complète d’un match à partir de données événementielles brutes.

- La création de visualisations claires et actionnables pour la performance d’équipe et individuelle.

- L’entraînement d’un modèle de xG simple mais robuste, facilement interprétable et extensible.

