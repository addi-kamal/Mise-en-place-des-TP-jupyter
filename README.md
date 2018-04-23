# Mise-en-place-des-TP-jupyter

## Installation

Pour pouvoir créer des TPs sous Jupyter et herberger ces TP sur Github, il faut

* Un compte github: www.github.com
* le logiciel Jupyter Notebook (ou mieux Anaconda: https://www.anaconda.com/download/)

## Création d'un notebook Jupyter

1. Dans un terminal, lancer la commande: `jupyter notebook`. Jupyter doit alors lancer automatiquement votre navigateur web (Firefox, Chrome, Safari, ...)
2. Dans votre navigateur, editez le contenu de votre fichier notebook.
  * texte: cellule Markdown (documentation: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
  * code: cellule Python
3. Sauvegardez votre résultat (File > Save and Checkpoint)

## Hebergement sur Github via l'interface web (Solution 1)

1. Sur Github, créez un nouveau repository (new repository)
2. Dans la partie Quick Setup (fond bleu), ajoutez un fichier README.md et décrivez votre répertoire (objectif du cours, etc). Pour sauvegarder, ajoutez un "commit" (bouton avec un fond vert en fin de page)
3. Ajoutez votre fichier Jupyter en appuyant sur le bouton Upload files (bouton situé à proximité du bouton Clone or Download)
4. Sauvegardez votre modification en appuyant sur le bouton commit (bouton avec un fond vert en fin de page)

## Hebergement sur Github en ligne de commande (Solution 2)

> Pour utiliser les lignes de commande, il faudra au préalable installer git sur votre machine.

1. Sur Github, créez un nouveau repository (new repository)
2. Sur votre machine, ouvrez un terminal dans le repertoire contenant fichier notebook
3. Dans votre terminal, initialisez git:

```
git init
git add .
git commit -m "premier depot"
```

4. Synchronisez votre repertoire avec votre repo github (l'adresse https correspond à l'url de votre repo sur github + ".git")

```
git remote add origin https://github.com/XXX/XXX.git
```

5. Deposez votre premier "commit" sur github

```
git push -u origin master
```

Ensuite, lorsque vous souhaitez envoyer une nouvelle version de votre notebook sur gitbook, il faudra taper les 3 commandes suivantes:

```
git add .
git commit -m "premiere modification"
git push -u origin master
```

