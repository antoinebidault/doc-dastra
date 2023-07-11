---
description: >-
  Dastra est nativement intégré à Google Tag Manager. Cet article vous
  expliquera comment intégrer le blocage ou le déblocage de tags en fonction des
  consentements de l'utilisateur à l'aide de GTM.
---

# Google Tag Manager

## Introduction

Google Tag Manager est un outil de taggage performant qui centralise l'ensemble des snippets de code que vous souhaitez intégrer dans votre site (Dastra peut d'ailleurs en faire partie !).\
Cette solution de taggage est très efficace pour implémenter le consentement effectif des cookies car elle ne nécessite pas de redéployer l'intégralité du site web lors de chaque modification de tags.

## Evènements envoyés à GTM dans le DataLayer

Les évènements suivants sont automatiquement envoyés au dataLayer de google :

| Nom                               | Signification                                                                              |
| --------------------------------- | ------------------------------------------------------------------------------------------ |
| dastra:consent:{your-vendor-name} | Cet évènement est envoyé quand l'utilisateur a accepté les cookies de ce vendeur           |
| dastra:refused:{your-vendor-name} | Cet évènement est déclenché quand l'utilisateur n'a pas consenti aux cookies de ce vendeur |

Vous pouvez par conséquent déclencher les balises correspondant aux différents vendeurs configurés dans le widget en utilisant ces deux évènements

## Exemple

Dans cet exemple, nous allons déclencher le tag Google Optimize au consentement de l'utilisateur.

Dans votre container GTM, créez un déclencheur sur évènement du dataLayer portant le nom de "dastra:consent:google-optimize"

La balise Google Optimize ne se déclenchera alors que sur cet évènement. Voici ce que ça donne dans l'interface de GTM :

![](<../../../../.gitbook/assets/image (169).png>)

### Cas spécifique des "blocking triggers"

le Widget&#x20;
