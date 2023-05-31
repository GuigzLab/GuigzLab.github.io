---
layout: distill
title: Image Captioning
description: A project in which I implemented a Neural Image Caption (NIC) network to generate image captions
img: assets/img/12.jpg
importance: 1
category: school

authors:
  - name: Guillaume Dufau
    url: "https://guigzlab.github.io/"
    affiliations:
      name: Université Paris Cité

toc:
  - name: Motivation
  - name: Methodology
    subsections:
      - name: Dataset
      - name: Model
      - name: Training
  - name: Évaluation

bibliography: nic-project.bib
# bibliography: 2018-12-22-distill.bib

---

# Motivation

Automatically describing the content of an image, or "Image Captioning," is a major task in computer vision and natural language processing. It involves generating a textual description that reflects the content of a given image. As part of my second year of Master's degree, I developed a project where I implemented a NIC (Neural Image Captioning) neural network, leveraging the model proposed in the influential "Show and Tell" paper proposed by Vinyals, Oriol et al. <d-cite key="Vinyals2014ShowAT"></d-cite>

<d-footnote>this is a footnote</d-footnote>

# Illustration

Le modèle NIC est un réseau de neurones profond qui utilise une architecture encodeur-décodeur. L'encodeur est un réseau de neurones convolutionnel (CNN) qui transforme l'image en une représentation vectorielle. Le décodeur, un réseau de neurones récurrent (RNN), utilise cette représentation pour générer une séquence de mots décrivant l'image.

Illustration

# Methodology

## Dataset

## Model

<img src="/assets/img/nic-model.png" style="width:100%;">

## Training


Pour entraîner et tester mon modèle, j'ai utilisé le jeu de données Flickr 8K, qui contient 8 000 images annotées chacune par 5 descriptions textuelles différentes.

Exemple de batch

# Résultats

Avant de présenter les résultats, il est important de comprendre les différentes métriques utilisées pour évaluer la qualité des descriptions générées :

- **Bleu (Bilingual Evaluation Understudy)** : Cette métrique compare la séquence de mots prédite avec les séquences de référence en calculant le rapport de n-grammes qui se chevauchent. Elle est généralement utilisée avec n allant de 1 à 4.

- **Rouge (Recall-Oriented Understudy for Gisting Evaluation)** : Elle évalue la qualité d'un résumé en comparant le nombre de n-grammes qui se chevauchent entre le résumé généré et les résumés de référence.

- **METEOR (Metric for Evaluation of Translation with Explicit ORdering)** : Cette métrique est une combinaison de plusieurs métriques, y compris la précision, le rappel et la similarité syntaxique. Elle a été conçue pour améliorer les faiblesses de la métrique BLEU.

Présentation des résultats et comparaison 