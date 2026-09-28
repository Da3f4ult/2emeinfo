## Introduction

Le langage HTML (HyperText Markup Language) est un langage de description dit "à balises". D'une manière très simplifiée, les balises permettent de mettre en forme le texte (titres, liens, tableaux,...) ou d'y placer des objets (images, sons, vidéos).

Depuis les débuts du langage (dans les années 1990) il y a eu de nombreuses évolutions et améliorations. La dernière version du langage est le HTML 5. Les pages WEB actuelles, en plus du HTML, intègrent du CSS, du javascript,...

Le but de ce document est de découvrir à travers des exemples simples les balises les plus courantes que l'on peut rencontrer dans un document HTML.

## À propos du CSS

À l'origine les pages étaient codées en HTML uniquement (pas de CSS ni de JavaScript,...). Il existe donc des balises pour mettre en forme le texte : couleur, gras, italique,... Ces balises sont obsolètes et ne seront pas décrites ici.

En effet, depuis l'introduction du CSS, la partie HTML contient uniquement le contenu (le fond) et le CSS permet de mettre en forme la page.

Un autre TP sur le CSS est à venir mais il est préférable d'avoir quelques connaissances en HTML avant de se lancer dans le CSS....

Place maintenant à la pratique. Copier le répertoire « html-css » du TP.

## 1 - Code minimum d'une page HTML 5

Voici ci-dessous le code minimum d'une page HTML 5.

```html
<!DOCTYPE html>
<html>
 <head>
 <meta charset="utf-8" />
 <title>Titre de votre page WEB</title>
 </head>
 <body> <!-- Commentaire : Corps de la page -->
 Contenu de votre page WEB.
 </body>
</html>
