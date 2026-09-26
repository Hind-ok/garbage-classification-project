# Classification d'images de déchets recyclables

Projet de fin de module TDMM — classification automatique de déchets en 6 catégories à partir d'images, par apprentissage profond.

## Auteurs
- Amraoui Hind
- Khadely Zaineb

## Description
Ce projet met en place un pipeline complet de deep learning pour classer des images de déchets en 6 catégories : carton, verre, métal, papier, plastique, et déchets divers.

## Jeu de données
Le dataset **Garbage Classification** (2527 images RGB) est disponible sur Kaggle :
https://www.kaggle.com/datasets/asdasdasasdas/garbage-classification

Pour le télécharger :
```bash
kaggle datasets download -d asdasdasasdas/garbage-classification
```

## Pipeline suivi
1. Data Collection
2. Data Exploration
3. Data Preprocessing / Cleaning (redimensionnement, normalisation, seuillage d'Otsu)
4. Data Augmentation (rotation, translation, luminosité)
5. Split des données (70/15/15, stratifié)
6. Choix / conception du modèle (CNN-Transformer hybride EfficientNet-B0, ResNet, MobileNet, CNN from scratch)
7. Entraînement (AdamW, recuit cosinus)
8. Optimisation des hyperparamètres (Optuna, TPE)
9. Évaluation (précision, rappel, F1-score, matrice de confusion)
10. Déploiement (benchmarking CPU vs GPU)

## Résultats
- Meilleure précision de validation : **95,25 %**
- Précision sur le jeu de test indépendant : **93,9 %**

## Structure du dépôt
garbage-classification-project/
├── ProjetTraitmentImage.ipynb 
├── presentation/ Presentation_Tri_de_déchets_recyclables.pdf
└── README.md

## Technologies utilisées
- Python, TensorFlow/Keras, PyTorch
- OpenCV, scikit-image (traitement d'image)
- Optuna (optimisation bayésienne)
- Google Colab (GPU NVIDIA T4)