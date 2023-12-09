# Projet_Data354_GUINDO_HUSSEN_HUGUES_JUNIOR
 Microsoft Rice Disease Classification Challenge

# Classification des maladies du riz - Projet 

## Introduction
Ce projet vise à développer un modèle de classification des maladies du riz en utilisant des réseaux de neurones profonds. Le jeu de données provient d'un concours Microsoft et contient des images de feuilles de riz présentant pour certaines une maladie  maladie.

## Structure du Projet

1. **Notebooks**
   - `projet-guindo-hussen-hugues-junior`


3. **Modèles**
   Définition des architectures de modèle utilisés: 
EfficientNet :
   Caractéristique principale : Conçu pour optimiser la performance et l'efficacité en ajustant simultanément la largeur, la profondeur, et la résolution des couches du réseau.

   Évolutivité : Les modèles EfficientNet sont évolués en utilisant un paramètre de mise à l'échelle (compound scaling) qui garantit un équilibre entre la largeur, la profondeur et la résolution du réseau.

ResNet (Residual Networks) :
   Caractéristique principale : Introduit des connexions résiduelles qui permettent un flux direct d'informations à travers les couches du réseau, facilitant l'apprentissage profond en évitant les problèmes de disparition du gradient.

   Architecture résiduelle : Les blocs résiduels, ou "residual blocks", contiennent des connexions skip (shortcuts) qui bypassent une ou plusieurs couches, facilitant l'apprentissage profond.

DenseNet (Densely Connected Convolutional Networks) :
   Caractéristique principale : Propose une architecture dense dans laquelle chaque couche reçoit des informations de toutes les couches précédentes dans un bloc.

   Connectivité dense : Les blocs dans DenseNet sont reliés de manière dense, ce qui signifie que chaque couche reçoit des entrées non seulement de la couche précédente mais aussi de toutes les couches précédentes dans le bloc.

   On choisira le modele qui minimisera le critère suivant 'Average Validation Loss Across Folds' qui se réfère à la moyenne des pertes de validation sur plusieurs plis (folds) lors de l'évaluation d'un modèle d'apprentissage automatique.

4. **Données**
   - `Train.csv`: Fichier CSV contenant les données d'entraînement.
   - `Test.csv`: Fichier CSV contenant les données de test.
   - `Images/`: Répertoire contenant les images.

5. **Résultats**
   - `predictions.csv`: Fichier CSV contenant les prédictions sur le jeu de données de test.

## Environnement et Dépendances
- Python 3.x
- Bibliothèques Python nécessaires : numpy, pandas, matplotlib, scikit-learn, torch, torchvision, albumentations, efficientnet_pytorch, PIL.

## Comment Utiliser
1. **Installation des Dépendances**
