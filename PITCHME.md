# SouthPigalle

Thèse professionnelle de François Lecerf

Présentation du 21/01/2019

---
@snap[north-west]
## Présentation
@snapend

@snap[center]
@ul
- La société SouthPigalle
- Labellisation semi-supervisée
- Reconnaissance d'entités nommées
- Semantic Slot Filling et reconnaissance d'intents
@ulend
@snapend

---
## Labellisation semi-supervisée
---
@snap[north-west]
### Principe
@snapend

@snap[center]
@ul
- 400 données annotées
- Labelliser automatiquement les observations très similaires
- Labelliser manuellement les observations ambigües
- Effectuer ces opérations de façon contrôlée
- Deux datasets clients pur lesquels on cherche à prédire l'intent: My Little Box, GameLoft
@ulend
@snapend
---
@snap[north-west]
### Méthode
@snapend

@snap[center]
@ul
- **Metric learning**: trouver un embedding séparant bien les classes des données annotées
- **Clustering spectral**: identifier des clusters homogène
- Identifier les paramètres séparant bien les clusters sur le jeu de train d'un point de vue précision
- Utiliser le jeu de test pour vérifier que le modèle se généralisera bien
- Propager les labels sur les clusters dont la précision sur une classe est supérieure à un seuil
@ulend
@snapend
---
@snap[north-west]
### Metric learning
@snapend
---
@snap[north-west]
### Clustering spectral
@snapend
---
## Reconnaissance d'entités nommées
---
@snap[north-west]
### Architecture
@snapend

@snap[west span-50]
@ul
- Tokenization
- Embedding layer
- Bi-LSTM
- Fully connected
- Cross-entropy
@ulend
@snapend

@snap[east span-50]
![](assets/img/RNN_NER.png)
@snapend
---
@snap[north-west]
### La cellule LSTM
@snapend

@snap[west span-50]
@ul
- Contexte partagé
- Forget Gate
- Update Gate
- Output Gate
@ulend
@snapend

@snap[east span-50]
![](assets/img/LSTM.png)
@snapend

---
## Semantic Slot Filling et reconnaissance d'intents
---
@snap[north-west]
### Architecture
@snapend

@snap[west span-50]
@ul
- Similaire au NER
- Features pour l'intent: concatenation des dernières hidden state
- Une loss pour les slots
- Une loss pour les intents
- A mitiger !
@ulend
@snapend

@snap[east span-50]
![](assets/img/RNN_SSF.png)
@snapend
---
## Add Some Slide Candy

![](assets/img/presentation.png)

---
@title[Customize Slide Layout]

@snap[west span-50]
## Customize Slide Content Layout
@snapend

@snap[east span-50]
![](assets/img/presentation.png)
@snapend

---?color=#E58537
@title[Add A Little Imagination]

@snap[north-west]
#### Add a splash of @color[cyan](**color**) and you are ready to start presenting...
@snapend

@snap[west span-55]
@ul[spaced text-white]
- You will be amazed
- What you can achieve
- *With a little imagination...*
- And **GitPitch Markdown**
@ulend
@snapend

@snap[east span-45]
@img[shadow](assets/img/conference.png)
@snapend

---?image=assets/img/presenter.jpg

@snap[north span-100 headline]
## Now It's Your Turn
@snapend

@snap[south span-100 text-06]
[Click here to jump straight into the interactive feature guides in the GitPitch Docs @fa[external-link]](https://gitpitch.com/docs/getting-started/tutorial/)
@snapend
