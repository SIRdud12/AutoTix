# Cat-gorisation-automatique-des-tickets
Classification automatique des tickets clients Jean-Claude

Ce projet a pour objectif de classer automatiquement les tickets clients afin de faciliter la gestion et le traitement des demandes.

Contenu du projet

tickets_annotes.csv : jeu de données avec les tickets et leurs catégories.

vectorizer_tfidf.pkl : TF-IDF utilisé pour transformer les textes en vecteurs.

model_svm.pkl : modèle SVM entraîné pour la classification.

confusion_matrix_*.png : matrices de confusion pour les différents modèles (Logistic Regression, Random Forest, SVM).

Technologies utilisées

Python

Pandas, NumPy

Scikit-learn (TF-IDF, SVM, Random Forest, Logistic Regression)

Matplotlib / Seaborn pour les matrices de confusion

Comment ça marche

Prétraitement des données : nettoyage et transformation des textes en vecteurs avec TF-IDF.

Entraînement des modèles : SVM, Random Forest, Régression Logistique.

Évaluation : utilisation des matrices de confusion pour comparer les performances.

Modèle final : le SVM a été choisi pour sa meilleure précision.
