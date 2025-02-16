# README : Computer Vision

## Table des matières
- [Description](#description)
- [Fonctionnalités principales](#fonctionnalités-principales)
- [Structure du projet](#structure-du-projet)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Auteurs](#auteurs)

## Description

Ce projet explore l'application des techniques de Computer Vision et de Deep Learning à la reconnaissance et la classification de produits en supermarché. Nous avons développé un modèle de détection basé sur YOLOv11, une architecture avancée intégrant un backbone performant, un neck optimisé et un head multi-échelle renforcé par un mécanisme d’attention.

Le modèle a été entraîné sur un jeu de données composé d’images issues de supermarchés internationaux, incluant des variations de packaging et de conditions d’éclairage, afin d’assurer une détection robuste et adaptable. Nous avons mis en place des techniques d’augmentation de données et optimisé les hyperparamètres du modèle pour améliorer sa capacité de généralisation.

L’évaluation du modèle repose sur des métriques telles que la précision, le rappel, le mAP@50 et le mAP@50-95, permettant d’analyser sa performance en conditions réelles. Nous avons également comparé ses résultats sur différents contextes afin d'identifier ses forces et limites.

Ce projet a été développé principalement sur Google Colab, avec une architecture adaptable permettant une utilisation efficace sur GPU. Il peut être utilisé à des fins de recherche, d’optimisation ou de déploiement pour des applications commerciales liées à la reconnaissance visuelle en grande distribution.

## Structure du projet

```bash
├── data
│   ├── test
│   │    ├── images
│   │    │   └── ...
│   │    ├── labels
│   │    │   └── ...
│   │    └── labels.cache
│   ├── train
│   │    ├── images
│   │    │   └── ...
│   │    ├── labels
│   │    │   └── ...
│   │    └── labels.cache
│   ├── valid
│   │    ├── images
│   │    │   └── ...
│   │    ├── labels
│   │    │   └── ...
│   │    └── labels.cache
│   └── data.yaml
├── docs
│   ├── rapport.pdf
│   └── README.md 
├── images
│   └── ...
├── images_pred
│   └── ...
├── model
│   └── model_v2.onnx
├── test_model.ipynb
└── train_model.ipynb
```

## Installation

Ce projet a été développé et optimisé pour une utilisation sur Google Colab. Pour l'utiliser, il suffit de télécharger le projet et de l'importer sur Google Drive afin de l'ouvrir avec Google Colab.

## Utilisation

 - Ouvrez et exécutez `train_model.ipynb` pour entraîner le modèle YOLOv11 sur les données disponibles. Les paramètres d’entraînement peuvent être ajustés selon les besoins.
 - Ouvrez `test_model.ipynb` pour tester le modèle sur de nouvelles images et obtenir une génération des prédictions avec affichage des bounding boxes et évaluation des performances via mAP, précision et rappel.
 - Le fichier `model_v2.onnx` contient une version optimisée du modèle entraîné. Ce modèle peut être utilisé pour l’inférence en temps réel ou intégré dans une application externe.

## Auteurs

Cette application a été développée par [KOCAB Cyril](https://github.com/Cyr-CK) et [COLLIN Hugo](https://github.com/hugocollin), dans le cadre du Master 2 SISE.