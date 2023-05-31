---
layout: distill
title: Image Captioning
description: A project in which I implemented a Neural Image Caption (NIC) network to generate image captions
img: assets/img/12.jpg
importance: 1
category: school

authors:
  - name: Guillaume Dufau
    url: "https://en.wikipedia.org/wiki/Albert_Einstein"
    affiliations:
      name: Université Paris Cité
---

# Motivation

La description automatique d'images, ou "Image Captioning", est une tâche majeure en vision par ordinateur et en traitement du langage naturel. Elle consiste à produire une description textuelle qui reflète le contenu d'une image donnée. Dans le cadre de mon projet de Master 2, j'ai implémenté un réseau de neurones NIC (Neural Image Captioning) basé sur le modèle proposé dans l'article de référence "Show and Tell". Cette technologie a de vastes applications, notamment dans les domaines de l'accessibilité, de l'intelligence artificielle et de la recherche d'images.

# Illustration

Le modèle NIC est un réseau de neurones profond qui utilise une architecture encodeur-décodeur. L'encodeur est un réseau de neurones convolutionnel (CNN) qui transforme l'image en une représentation vectorielle. Le décodeur, un réseau de neurones récurrent (RNN), utilise cette représentation pour générer une séquence de mots décrivant l'image.

Illustration

# Méthodologie

Pour entraîner et tester mon modèle, j'ai utilisé le jeu de données Flickr 8K, qui contient 8 000 images annotées chacune par 5 descriptions textuelles différentes.

Exemple de batch

# Résultats

Avant de présenter les résultats, il est important de comprendre les différentes métriques utilisées pour évaluer la qualité des descriptions générées :

- **Bleu (Bilingual Evaluation Understudy)** : Cette métrique compare la séquence de mots prédite avec les séquences de référence en calculant le rapport de n-grammes qui se chevauchent. Elle est généralement utilisée avec n allant de 1 à 4.

- **Rouge (Recall-Oriented Understudy for Gisting Evaluation)** : Elle évalue la qualité d'un résumé en comparant le nombre de n-grammes qui se chevauchent entre le résumé généré et les résumés de référence.

- **METEOR (Metric for Evaluation of Translation with Explicit ORdering)** : Cette métrique est une combinaison de plusieurs métriques, y compris la précision, le rappel et la similarité syntaxique. Elle a été conçue pour améliorer les faiblesses de la métrique BLEU.

Présentation des résultats et comparaison