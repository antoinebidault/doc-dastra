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

## Cas spécifique des "blocking triggers"

Dans certains cas, vous avez besoin de désactiver certaines balises si le consentement n'a pas été donné. Dans ce cas il est nécessaire d'effectuer certains paramétrages afin de lire directement la valeur du consentement stocké dans le cookie de consentement.

### 1. Créer une variable "DastraConsents"

#### Définir la variable

**Connectez vous** à votre compte Google Tag Manager et allez dans "Variables", puis créez une nouvelle "Variable définie par l'utilisateur".

<figure><img src="../../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

#### Sélectionnez "1st party cookies"

![](<../../../../.gitbook/assets/image (1).png>)

Nommez votre tag "DastraConsents" par exemple. Dans le champ nom du cookie (Cookie name), entrez le nom du cookie de consentement (par défaut : **consent-eu**).\
Pensez à **sélectionner l'option "URI-decode cookie"**

<figure><img src="../../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

#### Configurez ensuite votre trigger de cette façon :&#x20;

Dans ce cas, notre balise se déclenche si la profondeur de scroll dans la page est > 20%. Nous voulons que cette balise ne se déclenche que si le service google analytics a été autorisé par l'utilisateur. Voici comment configurer le déclencheur de la balise.

<figure><img src="../../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Dans la partie "Some Pages", si vous souhaitez activer la balise uniquement quand l'utilisation d'un service a été consenti, saisissez la formule **DastraConsents contains "{serviceName}":true** (exemple "crisp":true) sans espace

Si vous souhaitez déclencher la balise dans le cas d'un refus, mettez la formule :

**DastraConsents contains "{serviceName}":false** (exemple "google-analytics":false)

#### Cas de plusieurs déclencheurs du même type avec une exception

Si vous avez de nombreux déclencheurs différents pour une même balise, il est également tout à fait possible de créer une exception de cette manière.\
Exemple d'une balise avec plusieurs déclencheurs :&#x20;

<figure><img src="../../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Dans ce cas nous souhaitons ajouter une exception, si la balise google ads (google-ads) n'est pas accepté, nous ne voulons pas que la balise se déclenche .

Cliquez sur "Ajouter une exception" (Add Exception)

{% hint style="info" %}
Attention les exceptions ne fonctionnent bien que quand elles sont du même type. Si vos triggers sont du type "Page view", l'exception doit être également de type page view
{% endhint %}

Créez un déclencheur du même type avec pour nom par exemple "Pages vues avec le service Google Ads refusé"

<figure><img src="../../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Cliquez sur "Sauvegarder". Vous devriez avoir ceci :

<figure><img src="../../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

Enregistrez vos changements et vous devriez constater que vos balises sont bien désactivées sur les pages en question si le consentement n'est pas donné.
