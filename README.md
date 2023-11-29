<!-- omit in toc -->
# Atelier Web en RedemArts

<!-- omit in toc -->
## Table des matières

- [Introduction](#introduction)
  - [Installer votre éditeur de code](#installer-votre-éditeur-de-code)
- [HTML](#html)
    - [Ton code :](#ton-code-)
  - [Les balises](#les-balises)
    - [Ton code :](#ton-code--1)
  - [Astuce : Les commentaires en HTML](#astuce--les-commentaires-en-html)

# Introduction

Dans ce cours, nous explorerons les bases du développement web, en commençant par la création d'une page web simple à l'aide du langage HTML. Nous découvrirons les principaux éléments nécessaires pour structurer et organiser le contenu d'une page web, ainsi que des astuces pour bien démarrer votre projet.
<!-- MAIS ENCORE LE CSS -->

## Installer votre éditeur de code

1. **Téléchargement** :
   Rends-toi sur le site officiel de Visual Studio Code : [Visual Studio Code](https://code.visualstudio.com/Download). Télécharge la version en fonction de ton système d'exploitation.

2. **Lancement de l'installation** :
   Une fois le téléchargement terminé, ouvre le fichier téléchargé (généralement nommé `VSCodeSetup.exe`) en double-cliquant dessus.

3. **Suivre les instructions** :
   Une fenêtre d'installation s'ouvrira. Il suffira de suivre les instructions à l'écran. Tu auras probablement à accepter des conditions d'utilisation et à choisir l'emplacement d'installation..

4. **Terminer l'installation** :
   Une fois que l'installation est terminée, tu pourras ouvrir Visual Studio Code en le cherchant dans le menu Démarrer ou en double-cliquant sur l'icône sur le bureau si tu en as créé une.

5. **Accéder à la vue des extensions** :
   Ouvre VSCode et dans la barre latérale, clique sur l'icône en forme de carré.<br>
   ![](./Resources/images/plugins.png)<br>
   Cela ouvrira la vue des extensions.

6. **Rechercher Live Server** :
   Dans la barre de recherche en haut de cette vue, tape "Live Server" et appuie sur Entrée. Tu devrais voir l'extension "Live Server" proposée dans les résultats de recherche.<br>
   ![](./Resources/images/liveServer.png)

7. **Installer l'extension** :
   Lorsque tu trouves l'extension "Live Server" dans la liste, clique sur le bouton "Installer".

8. **Redémarrer si nécessaire** :
   Il est possible que VSCode te demande de redémarrer pour activer complètement l'extension. Si c'est le cas, suis simplement les instructions.

# HTML

HTML qui signifie HyperText Markup Language, est le langage de balisage utilisé pour créer la structure et le contenu des pages web. Il utilise des balises pour décrire les différents éléments d'une page, comme les titres, les paragraphes, les images, les liens, etc. Ces balises permettent de définir la manière dont le contenu doit être affiché dans un navigateur web. HTML agit comme l'ossature de base d'une page web, déterminant la disposition et l'organisation du contenu, tout en permettant l'intégration d'autres langages comme CSS pour le style et JavaScript pour l'interactivité.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <!-- Contenu -->
</body>
</html>
```

Je précise que cette structure HTML est par défaut et nécessite peu de changements. Donc ne supprime aucune ligne de ce bout de code, chaque élément est important.

### Ton code :
1. Crée un dossier sur ta machine que tu nommeras "WebDev", tu devras le retrouver après si tu ne veux pas le perdre je te conseille de le mettre sur le "Bureau".
2. Dans VSCode, ouvre le dossier qu'on vient de créer. Ajoute un fichier `index.html`.
3. Dans ce fichier tu vas taper un simple point d'exclamation `!` et validé avec `Enter` ou `Tab`.
4. En bas à droite trouve le bouton `Go Live` et clique dessus. Cela devrait ouvrir une page/onglet sur ton navigateur (tu peux aussi cliquer droit sur le fichier `index.html` et cliquer sur ouvrir avec Live Server).

> :exclamation: Lors d'une mise à jour de VScode il est possible que la fonctionnalité `!` ai changée. Il faut désormais activer `Emmet: Use Inline Completions` qui est un paramètre dans VSCode. Ainsi, lorsque tu écriras du code Emmet, VScode te montrera directement le résultat et il faudra valider avec `Tab`.

[:arrow_up: Revenir au top](#table-des-matières)

## Les balises

Ce sont tous ces mots étranges entre `< >`. Sans les balises HTML, une page ne serait qu'un simple bloc texte. Ce sont les balises qui structurent le contenu de la page. Elles seront interprétées par le navigateur pour lui permettre d'afficher correctement votre page à l'utilisateur.

Elles peuvent être imbriquées l'une dans l'autre.

La balise `<body>` contient le **contenu** de la page. On y met **toutes** les balises de textes, d'images, de liens,...

```html
<body>
   Je suis tout le contenu affiché sur une page web.
</body>
```

On commence toujours par la balise entrante, puis le contenu, ensuite on referme la balise.

```html
<p>Salut</p>
```

Certaines balises peuvent se voir attribuer des attributs. Ils permettent de préciser certains paramètres (par exemple : l'adresse d'un lien, la source d'une image, le style d'une div, ...)

```html
<img src="mon lien"/>
```

> Ici `src` est l'attribut et `mon lien` la valeur.

La balise `<title>` est contenue dans la balise `<head>` et permet de donner un titre à votre page.

```html
<title>Le titre de ma super page HTML</title>
```

### Ton code :
1. Dans ton fichier HTML que tu as créé précédemment change le `<title>` car "Document" est le contenu par défaut, tu peux par exemple écrire ton nom et prénom ou un pseudo.
2. Entre l'ouverture de ta balise `<body>` et sa fermeture `</body>`, écris `p` et appuyes sur `Tab` ou `Enter` (auto-complétion super pratique). Ajoute du contenu entre l'ouverture de ta balise `<p>` et sa fermeture, "Mes débuts dans le développement Web" sera très bien pour le moment.
3. Télécharge cette <a href="./Resources/images/learnWebDev.jpg" target="_blank">image</a> et enregistre-la à la racine du dossier.
4. Ajoute la balise `img` à la suite de ton code (après la balise `p` mais toujours dans la balise `body`). Pour ajouter une image il faut faire appel à la balise `<img>`. Fais confiance à ton éditeur de code dès que tu tapes "img" dans ton code, VSCode te proposera la balise img, il suffit de faire `Tab` ou `Enter` 😊
5. Il faut maintenant changer la source qui n'est autre que l'image que tu as téléchargé. Dans ta balise `img` se trouve l'attribut `src=""` tapes `./` une liste apparaitra et tu n'as plus qu'à choisir ton image.
6. Va voir le résultat de ta page sur ton navigateur 😁
7. Tu devrais avoir obtenu ce résultat de code :
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Changement du titre -->
    <title>Ton prénom & ton nom</title>
</head>
<body>
   <!-- Création d'une balise paragraphe -->
    <p>Mes débuts dans le développement Web</p>
    <!-- Ajout d'une balise img avec sa source en racine -->
    <img src="./learnWebDev.jpg">
</body>
</html>
```

[:arrow_up: Revenir au top](#table-des-matières)

## Astuce : Les commentaires en HTML

Les commentaires dans le code sont une bonne pratique à avoir. Ils permettent de donner des informations complémentaires à ceux qui retravaillerons dans votre code. Généralement pour l'HTML, vu que c'est la base, il y a peu d'intérêt de commenter. Mais cela peut-être une bonne manière de vous organiser, surtout au début.

```html
<p> Je suis un texte visible <!-- je suis un commentaire invisible --></p>
```

[:arrow_up: Revenir au top](#table-des-matières)