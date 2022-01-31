---
description: >-
  Cet article vous présente comment intégrer le widget d'exercice de droit dans
  une page web
---

# Intégration technique

## Objectifs

Le widget d'exercice de droits vous permet de **collecter automatiquement depuis une page de votre site des demandes d'exercice de droit** de différents types (suppressions, modifications, rectifications...)

Le widget est intégré au **SDK javascript** de dastra.

## Prérequis

Afin de mettre en place le widget d'exercice de droit, vous devez disposer d'**une clé publique d'API** : [lire la documentation](../settings/gestion-des-cles-dapi.md) ou[ accéder directement à la page de gestion des clés d'API](https://app.dasta.eu/general-settings/api)

## Mise en place du widget dans l'interface dédiée

Pour commencer, vous devez **mettre en place le widget** dans[ le panel de gestion des widgets](https://app.dasta.eu/workspace/data-subject-request/integrations) d'exercice de droits :&#x20;

![](<../../.gitbook/assets/image (250) (1) (1).png>)

Voici un exemple simple d'intégration du widget (en mode popup avec un bouton d'ouverture) :

```html
<div id="customer-subject-form-custom" ></div>
<button id="customer-request-button">Open the widget</button>
<script src="https://cdn.dastra.eu/sdk/dastra.js?key={YOUR PUBLIC KEY}" async></script>
<script>
  window.dastra = window.dastra || [];
  dastra.debug = true;
  window.dastra.push(function(){
    dastra.loadCustomerSubjectForm({
      selector: '#customer-subject-form-custom',
      widgetId: {your widget id},
      onLoad: function (form) {
        document.getElementById('customer-request-button').addEventListener('click',function () {
          form.open()
        })
      }
    })
  })
</script>
```



## Comment envoyer automatiquement des valeur de formulaire au widget ?

```html
<script>
  dastra.push(['set','dsr:refId','{your custom userId}'])
</script>
```

Vous pouvez remplacer le nom de la colonne **refId** par le nom de propriété suivante :&#x20;

* refId : the unique identifier of the user
* familyName&#x20;
* givenName
* email
* city
* zipCode
* countryCode
* address
* phoneNumber
* message
* additionalDatas**\***

\*For the specific case of custom fields, you must reference the additionalDatas name:

```html
<script>
  var payload = {
    customFieldSlug1: 'test', 
    customFieldSlug2: 'test'
  };
  dastra.push(['set','dsr:additionalDatas', payload])
</script>
```

Les champs additionnels seront automatiquement fusionnés

## Envoi des paramètres en utilisant le mode page

Il est également possible de passer ces paramètres en utilisant les paramètres querystring, il suffit de préfixer le nom du paramètre par dsr\_ :&#x20;

```url
https://api.dastra.eu/v1/client/customer-subject-form?id=<Your widget id>
&key=<your public key>
&dsr_email=test@github.org
&dsr_givenName=Dastonaute
&dsr_refId=123456
&...etc...
```

