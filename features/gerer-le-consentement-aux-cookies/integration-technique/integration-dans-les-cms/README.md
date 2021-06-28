---
description: >-
  Apprenez à intégrer le widget de cookie Dastra dans une page web en utilisant
  le SDK javascript.
---

# Démarrage rapide

## Prérequis : récupération d'une clé publique d'API

pour récupérer une clé publique du SDK Dastra, rendez-vous sur cette page : [https://app.dastra.eu/general-settings/api](https://app.dastra.eu/general-settings/api) 

![](../../../../.gitbook/assets/image%20%2824%29.png)

## Configurez votre widget

Configurez votre widget en suivant le guide ci-dessous

{% page-ref page="../../configuration-du-widget/" %}

## Insérez le code d'intégration html

Insérez le code HTML disponible dans la section "Code" du module de consentement Cookie Dastra **avant la fin de la balise &lt;BODY&gt;** de votre site internet, sur l'ensemble des pages. Vous pouvez utiliser le Google tag manager pour insérer dynamiquement ce code sur chaque page.

{% hint style="info" %}
Pour que le code fonctionne correctement, assurez-vous de la bonne configuration au préalable de la clef publique de votre API.
{% endhint %}

Voici comment se présente le code d'intégration du widget

```markup
<div id="dastra-cookie-consent" data-widgetid="{your_widget_id}"></div>
<script src="https://app.dastra.eu/sdk/dastra.js?key={your_public_key}" async>
</script>
```

La div avec l'id "dastra-cookie-consent" sera l'emplacement du rendu de votre widget de consentement. L'attribut "data-widgetid" permet d'identifier le widget invoqué, c'est souvent un nombre \(int32\). {your\_public\_key} correspond à votre clé publique [d'API récupérable ici](https://app.dastra.eu/general-settings/api)

Une fois le code inséré dans la balise &lt;body&gt; de votre site, le widget s'affichera sur votre site.

{% hint style="warning" %}
Pour des performances optimales, le widget est mis en cache automatiquement par la navigateur dans le sessionStorage
{% endhint %}

## Wordpress

Si vous utilisez Wordpress, vous trouverez dans le lien ci-dessous plus d'informations sur la manière dont le code généré peut être inséré à la fin de la balise html de votre site internet.

{% page-ref page="wordpress.md" %}



Une fois le widget intégré, passez à la phase de test.

{% page-ref page="../comment-tester-lintegration-dun-widget.md" %}



