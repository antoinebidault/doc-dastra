---
description: >-
  This chapter will teach you how to manage the consents of our cookie widget
  programmatically.
---

# Manage consent programmatically

## Where are the consents stored?

The entire proof of user consent is stored in the browser's localStorage (the storage key is named dastra-consents) in json format. The propagation of consents depends on it, that's why it's not recommended to directly modify the data of this key

{% hint style="info" %}
It's not recommended to directly modify the data in the localStorage. Preferably use the Javascript SDK of dastra.
{% endhint %}

## Access to the consent service

The dastra consent service can be accessed in this way:

```javascript
<script>
dastra = dastra || []
dastra.push(['cookieReady',function(manager){
    console.log(manager.consent)
});
</script>
```

### Liste des méthodes disponibles dans le manageur de consentement

dans manager.consent, vous disposez des méthodes suivantes :

* open() : ouvre le widget de consentement
* close() : ferme le widget de consentement
* getAllConsents() : récupération des tous les consentements
* getPurposeConsent(purposeId:number) : récupère le consentement d'une catégorie de cookies
* setPurposeConsent(purposeId:number, consent:bool): défini le consentement pour une catégorie
* getServiceConsent(serviceShortName:string): Récupère le consentement d'un service particulier.
* setServiceConsent(serviceShortName:string, consent:bool): Définit le consentement d'un élément particulier

### Récupérer la liste des consentements de l'utilisateur (getAllConsents)

Une fois que vous accédez au manager de consentement, il est très aisé de récupérer les consentements de l'utilisateur courant :

```javascript
<script>
dastra = dastra || []
dastra.push(['cookieReady', function(manager){
    // Get the complete consent services list
    var consents = manager.consent.getAllConsents()
});
</script>
```

La méthode ci-dessus renvoie la liste de tous les consentements de l'utilisateur

```javascript
[
  {
    "id":"000000-0000000-000000",
    "name": "Service name",
    "purpose": 1,
    "logoUrl": "https://logo-url/img.jpg",
    "privacyPolicyUrl":"",
    "description": "Short description",
    "defaultConsent": true,
    "requiredConsent":true
  },
  ...
]
```

### Interroger les consentements par catégorie (getPurposeConsent/setPurposeConsent)

Les catégories de cookies sont représentés par les ids suivants :

| Type        | Id |
| ----------- | -- |
| Nécessaires | 0  |
| Préférences | 1  |
| Analytique  | 2  |
| Marketing   | 3  |
| Autre       | 4  |

```javascript
<script>
dastra = dastra || []
dastra.push(['cookieReady',function(manager){
    // Get the complete consent services list
    let cookiePurpose = 2; // 2 = Analytic
    let consents = manager.consent.getPurposeConsent(cookiePurpose);
    manager.consent.setPurposeConsent(cookiePurpose, false)
});
</script>
```

### Manipuler les consentements par service

Pour manipuler les consentements par service, vous aurez besoin du nom simplifié du service disponible dans l'interface de gestion des services de votre widget.

{% hint style="info" %}
**Comment trouver le nom simplifié du service ?**\
Rendez-vous dans l'interface de gestion des services, en éditant un service, le nom simplifié (slug) du service apparaît en dessous du nom du cookie.
{% endhint %}

![Emplacement du nom du cookies simplifié](<../../../.gitbook/assets/image (79).png>)

```javascript
<script> 
dastra = dastra || []
dastra.push(['cookieReady',function(manager){
    // Get the complete consent services list
    let cookiePurpose = 'google-analytics'; // 2 = Analytic
    let consents = manager.consent.getServiceConsent(cookiePurpose );
    manager.consent.setServicePurpose(cookiePurpose, false)
});
</script>
```

### Exemple d'utilisation

Pour illustrer la chose, voici un exemple complet qui permet de manipuler les consentements dans le navigateur sans utiliser le widget :



```javascript
todo
```

