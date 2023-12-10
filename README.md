# Projet_Data354_GUINDO_HUSSEN_HUGUES_JUNIOR
 Microsoft Rice Disease Classification Challenge

# Classification des Images de riz - Projet 

## Introduction
Ce projet vise à développer un modèle de classification des maladies du riz en utilisant des réseaux de neurones profonds. Le jeu de données provient d'un concours Microsoft et contient des images de feuilles de riz présentant pour certaines une maladie  maladie.

## Structure du Projet


### Notebooks : 
   Vous trouverez ici un notebooks Jupyter utilisé pour le développement, l'entraînement et l'évaluation de modèles.


1. **Notebooks**
   - `projet-guindo-hussen-hugues-junior`

2. **Données**
   - `Train.csv`: Fichier CSV contenant les données d'entraînement.
   - `Test.csv`: Fichier CSV contenant les données de test.
   - `Images/`: Répertoire contenant les images.

3. **Modèles**
   Définition des architectures de modèle utilisés: 

### EfficientNet :
   Caractéristique principale : Conçu pour optimiser la performance et l'efficacité en ajustant simultanément la largeur, la profondeur, et la résolution des couches du réseau.

   Évolutivité : Les modèles EfficientNet sont évolués en utilisant un paramètre de mise à l'échelle (compound scaling) qui garantit un équilibre entre la largeur, la profondeur et la résolution du réseau.

### ResNet (Residual Networks) :
   Caractéristique principale : Introduit des connexions résiduelles qui permettent un flux direct d'informations à travers les couches du réseau, facilitant l'apprentissage profond en évitant les problèmes de disparition du gradient.

   Architecture résiduelle : Les blocs résiduels, ou "residual blocks", contiennent des connexions skip (shortcuts) qui bypassent une ou plusieurs couches, facilitant l'apprentissage profond.

### DenseNet (Densely Connected Convolutional Networks) :
   Caractéristique principale : Propose une architecture dense dans laquelle chaque couche reçoit des informations de toutes les couches précédentes dans un bloc.

   Connectivité dense : Les blocs dans DenseNet sont reliés de manière dense, ce qui signifie que chaque couche reçoit des entrées non seulement de la couche précédente mais aussi de toutes les couches précédentes dans le bloc.

On choisira le modele qui minimisera le critère suivant 'Average Validation Loss Across Folds' qui se réfère à la moyenne des pertes de validation sur plusieurs plis (folds) lors de l'évaluation d'un modèle d'apprentissage automatique.


4. **Entraînement des Modèles** 
 Les modèles sont entraînés sur plusieurs plis en utilisant la validation croisée. L'arrêt anticipé est mis en place pour éviter un surapprentissage.


5. **Résultats**
   - `predictions.csv`: Fichier CSV contenant les prédictions sur le jeu de données de test.

6. **Entraînement du Modèle**
- Les fonctions utilisées sont : 
   * **verifier_correspondances** : Vérifie si les images dans dont les Id sont dans le jeu de donnees Test et Train sont bien dans le repertoire image 

   * **get_loaders** : Fonction pour obtenir les loaders d'entraînement et de validation.

   * **Net,ResNetModel,DenseNetModel** : Initialise des modèles et une couche linéaire de classification.

   * **check_acc** :  Fonction pour calculer la perte moyenne sur un ensemble de données (loader)

   * **save_checkpoint** : Fonction pour sauvegarder un checkpoint du modèle et de l'optimiseur.

   * **train_fn** : Fonction d'entraînement utilisant la précision mixte (AMP)
 

7. **Prédictions sur le Jeu de Données de Test**
- Exécutez les lignes de codes defini dans le fichier Projet_GUINDO_HUSSEN_HUGUES_JUNIOR pour faire des prédictions.


8. **Exploration des Résultats**
- Consultez le fichier `predictions2.csv` pour les résultats de la prédiction.

**La capture de la soumission sur Zindi réprésente plusieurs modèles que nous avons eu à soumettre sur la plateforme pour evaluer les performances en fonction des modèles. Il en ressort que le modèle DenseNet et EfficientNet nous fournissent des résultats plus ou moins satisfaisants comparativement aux trois modèles** 

## Environnement et Dépendances
- Python 3.x
- Bibliothèques Python nécessaires : numpy, pandas, matplotlib, scikit-learn, torch, torchvision, albumentations, efficientnet_pytorch, PIL.

## Ressources Supplémentaires
- [PyTorch](https://pytorch.org/tutorials/)
- [PyTorch2](https://towardsdatascience.comunderstanding-pytorch-with-an-example-a-step-by-)
- [Albumentations](https://albumentations.ai/)

## Auteur
Guindo Hussen Hugues Junior
