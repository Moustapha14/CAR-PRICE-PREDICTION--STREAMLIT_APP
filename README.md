# Estimation du Prix de Voiture - Projet Streamlit

## Aperçu

Ce projet est une application web interactive conçue pour estimer le prix des voitures d'occasion en se basant sur diverses caractéristiques telles que la marque, le modèle, l'année, le kilométrage, le type de transmission, et le type de carburant. L'application est construite avec Streamlit, une bibliothèque open-source pour créer des applications web de data science en Python, et utilise un modèle de forêt aléatoire (RandomForestRegressor) pour les prédictions.

## Caractéristiques Principales

- **Interface utilisateur intuitive**: Streamlit fournit une interface utilisateur conviviale, permettant aux utilisateurs de saisir les détails de la voiture à travers des widgets interactifs.

- **Intégration de MongoDB**: L'application se connecte à une base de données MongoDB pour récupérer les données utilisées pour entraîner le modèle de machine learning. Cela permet une gestion efficace et flexible des données.

- **Machine Learning**: Utilise un modèle de forêt aléatoire pour prédire le prix en se basant sur l'apprentissage à partir des données historiques. Le modèle est connu pour sa précision et sa capacité à fonctionner sur des données non linéaires.

## Comment ça marche

1. **Connexion à MongoDB**: L'application commence par établir une connexion à la base de données MongoDB, où elle récupère les données nécessaires.

2. **Prétraitement des données**: Les caractéristiques pertinentes sont sélectionnées et encodées (via one-hot encoding) pour être utilisées par le modèle de machine learning. Les données sont ensuite divisées en ensembles d'entraînement et de test.

3. **Entraînement du modèle**: Un modèle de forêt aléatoire est entraîné sur l'ensemble d'entraînement.

4. **Interface utilisateur Streamlit**: L'utilisateur interagit avec l'application via divers widgets pour entrer les détails de la voiture. Ces entrées sont récupérées et transformées pour correspondre au format attendu par le modèle.

5. **Prédiction et affichage**: Le modèle utilise les informations fournies pour estimer le prix de la voiture. Ce prix estimé est ensuite affiché à l'utilisateur.

## Utilisation

Pour utiliser cette application, l'utilisateur doit disposer d'une installation fonctionnelle de Python et des bibliothèques nécessaires, ainsi que d'un accès à une base de données MongoDB. Les détails de la configuration de la base de données (URI, nom de la base de données, nom de la collection) doivent être correctement renseignés dans le script.

Une fois que tout est configuré, l'application peut être lancée en utilisant la commande suivante dans le terminal :

```bash
streamlit run <nom_du_fichier.py>
```

## Conclusion

Cette application est un outil pratique qui utilise la puissance de la science des données et du machine learning pour fournir des estimations de prix de voitures d'occasion. Elle démontre comment des technologies diverses peuvent être intégrées pour résoudre des problèmes concrets de manière efficace et conviviale.
