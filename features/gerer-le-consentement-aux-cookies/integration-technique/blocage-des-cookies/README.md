---
description: Ce guide vous expliquera comment bloquer réellement les cookies.
---

# Blocage des cookies

Pour réaliser un blocage effectif des cookies, il existe plusieurs méthodes possibles : la suppression des cookies, le blocage d'un snippet, le javascript personnalisé ou Google Tag Manager.

## Suppression des cookies

Cette méthode est la plus rapide à mettre en place, mais aussi la moins fiable. Dans le panel de configuration du widget Dastra, si vous renseignez le nom des cookies associés à chaque service, cela supprimera automatiquement les cookies concernés à chaque affichage de page.&#x20;

![](<../../../../.gitbook/assets/image (85).png>)

Ce fonctionnement peut-être effectif dans certain cas, mais risque de perturber de manière importante la fiabilité des outils tiers utilisés (Outils de web analytique notamment). Il est très souvent préférable d'utiliser en complément une autre des méthodes ci-dessous.

## Bloquer un snippet de code dans la page

Cette méthode permet de désactiver totalement un snippet de code de suivi de la page.

Pour cela, remplacez dans le code html de votre page le snippet de code suivant :

```markup
<script >
  alert("hello, I'm a tracking javascript tag");
</script>
```

Par :

```markup
<script data-consent="{your-service-slug}" type="dastra/script">
   alert("hello, I'm a tracking javascript tag");
</script>
```

Remplacez le "{your-service-slug}" par l'identifiant de votre service saisi lors de la config de votre widget :

![](<../../../../.gitbook/assets/image (86).png>)

Si le client a accepté les cookie, le contenu du script sera automatiquement exécuté.

{% hint style="info" %}
Ce fonctionnement peut avoir plusieurs effets de bord : notamment des problèmes de highlight de la synthaxe dans la plupart des IDEs.&#x20;

Le bout de script ne sera pas du tout exécuté dans le cas d'une erreur d'implémentation du widget de Dastra.
{% endhint %}

### Blocage en pur javascript

En pur javascript, vous pouvez utiliser les évènements déclenchés sur le window pour collecter le consentement et gérer un comportement particulier selon l'acceptation et le refus des cookies. Ce fonctionnement vous donnera une plus grande souplesse :

```javascript
<script>
  (function(){

      /* 
      * Trigger  a custom servicve tag with expected cookies
      */
      function customTagsTrigger () {
        /* If the vendor provide a specific function for making the service work cookie-less, pull it here.
        * Else copy the default code snippet provided by the tag vendors*/
      }

      /*
      * Handle the global scope consent event
      * If the user has consented to custom vendor's tag cookies, this event will be fired on each page load where the cookie consent widget is installed
      */
      window.addEventListener('dastra:consent:{your-service-slug}', function () {
        /* The client is optin to the custom vendor's cookies here */
        customTagsTrigger();
        console.log('{your-service-slug} accepted')
      });

      /* Uncomment this if you want to handle the refused event
      *  Handle global scope refused event event (Optional) 
      */
        window.addEventListener('dastra:refused:{your-service-slug}', function () {
         // The custom's services cookies are refused 
         console.log('{your-service-slug} cookies refused')
       });
      
  });
  </script>
```

### Google Tag Manager

Voir page suivante:

{% content-ref url="google-tag-manager.md" %}
[google-tag-manager.md](google-tag-manager.md)
{% endcontent-ref %}

### Rappel sur le cycle de vie du consentement :&#x20;

<figure><img src="../../../../.gitbook/assets/cookies-lifecycle.drawio.png" alt=""><figcaption><p>Cookie widget lifecycle</p></figcaption></figure>
