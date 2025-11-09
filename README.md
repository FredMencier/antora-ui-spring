
<p align="center">
  <a href="https://github.com/FredMencier/antora-ui-spring">
    <img alt="Spring" src="https://github.com/FredMencier/antora-ui-spring/blob/main/src/img/java.svg" width="250" />
  </a>
</p>


# antora-ui-spring

## Principe

Ce projet est un fork du projet [antora-ui-spring](https://github.com/spring-io/antora-ui-spring). Il fourni une ui customisée pour la génération de documentation basée sur Antora.

Vous trouvez la documentation complète d'Antora sur le site [docs.antora.org](https://docs.antora.org/).

Le système de templating utilisé par Antora est [Handlebars](https://handlebarsjs.com/)

`gulp` permet de réaliser des taches répétitives (lint, minify, zip...). Vous trouvez plus d'info sur [Gulp](https://gulpjs.com/)

Pour builder et tester le site en local vous pouvez utiliser les commandes :

```shell
npm install
gulp preview
```

Le serveur local demarre avec le log :

```log
[12:00:00] Starting server...
[12:00:00] Server started http://localhost:5252
[12:00:00] Running server
```

## Packaging du bundle pour une utilisation avec Antora

Pour packager la UI afin de générer le site vous pouvez utiliser la commande : 

```shell
gulp bundle
```

Fixez les erreurs qui apparaissent lors du processus de lint

Lorsque la commande se termine sans erreurs, la UI est disponible au format zip dans le répertoire `build/ui-bundle.zip`

Vous pouvez alors utiliser votre UI directement avec Antora :
- en passant le zip dans la ligne de commande grace à l'option `--ui-bundle-url`
- en pointant votre zip depuis le fichier `antora-playbook.yml`

```yml
ui:
  bundle:
    url: "https://github.com/FredMencier/antora-ui-spring/releases/download/1.0.0/ui-bundle.zip"
    snapshot: true
```

## Les éléments personnalisés
- Ajout d'un `card.css` permettant l'affichage d'une entrance page sous forme de card

## Demo

La documentation contenu dans le projet `https://github.com/FredMencier/antora-sample` est un example d'utilisation de cette UI custom.
Antora permet de générer le site associé