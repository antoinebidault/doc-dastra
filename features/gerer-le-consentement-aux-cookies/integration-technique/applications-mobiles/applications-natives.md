---
description: >-
  Cette page vous détaille le fonctionnement de l'api de gestion du
  consentement. Cette API peut-être intégrée facilement dans les applications
  mobiles natives.
---

# Applications natives

{% api-method method="get" host="https://api.dastra.eu" path="/v1/client/cookie-widget-settings/:id?key=:key" %}
{% api-method-summary %}
Récupérer la configuration du widget
{% endapi-method-summary %}

{% api-method-description %}
Cet endpoint permet de récupérer l'intégralité de la configuration du widget
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="number" required=true %}
ID of the widget configuration
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="culture" type="string" required=false %}
The locale of the widget configuration \(en, fr...\)
{% endapi-method-parameter %}

{% api-method-parameter name="key" type="string" required=true %}
The public api key provided
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "translation": {
    "id": "35dddc1a-3ceb-49a8-a8d2-fc343fdb56a3",
    "lang": "fr",
    "order": 0,
    "buttonBackLabel": "Retour",
    "buttonAcceptLabel": "Accepter tout",
    "buttonSettingsLabel": "Personnaliser",
    "buttonViewPurposeLabel": "Sélectionner les finalités",
    "buttonConfirmLabel": "Enregistrer sélection",
    "buttonAcceptAllLabel": "Tout accepter",
    "buttonLaterLabel": "Tout refuser",
    "buttonViewMoreLabel": "Voir la liste",
    "noticeUrlButtonLabel": "Lire notre politique des cookies",
    "startupTitle": "Nous utilisons les cookies",
    "startupDisclaimer": "Les cookies nous permettent de personnaliser le contenu et les annonces, d'offrir des fonctionnalités relatives aux médias sociaux et d'analyser notre trafic. Nous partageons également des informations sur l'utilisation de notre site avec nos partenaires de médias sociaux, de publicité et d'analyse, qui peuvent combiner celles-ci avec d'autres informations que vous leur avez fournies ou qu'ils ont collectées lors de votre utilisation de leurs services",
    "innerTitle": "Voici nos services qui utilisent les cookies",
    "innerDisclaimer": "Dans cet écran de configuration, vous pouvez choisir les cookies que vous autorisez lors de votre navigation",
    "categoryNecessaryLabel": "Cookies nécessaires",
    "categoryNecessaryExcerpt": "Les cookies nécessaires contribuent à rendre un site Web utilisable en activant des fonctions de base comme la navigation de page et l'accès aux zones sécurisées du site Web. Le site Web ne peut pas fonctionner correctement sans ces cookies.",
    "categoryNecessaryDescription": "Les cookies nécessaires contribuent à rendre un site Web utilisable en activant des fonctions de base comme la navigation de page et l'accès aux zones sécurisées du site Web. Le site Web ne peut pas fonctionner correctement sans ces cookies.",
    "categoryPreferenceLabel": "Préférences",
    "categoryPreferenceExcerpt": "Les cookies de préférences permettent à un site Web de retenir des informations qui modifient la manière dont le site se comporte ou s’affiche, comme votre langue préférée ou la région dans laquelle vous vous situez.",
    "categoryPreferenceDescription": "Les cookies de préférences permettent à un site Web de retenir des informations qui modifient la manière dont le site se comporte ou s’affiche, comme votre langue préférée ou la région dans laquelle vous vous situez.",
    "categoryAnalyticalLabel": "Statistiques",
    "categoryAnalyticalExcerpt": "Les cookies statistiques aident les propriétaires du site Web, par la collecte et la communication d'informations de manière anonyme, à comprendre comment les visiteurs interagissent avec les sites Web.",
    "categoryAnalyticalDescription": "Les cookies statistiques aident les propriétaires du site Web, par la collecte et la communication d'informations de manière anonyme, à comprendre comment les visiteurs interagissent avec les sites Web.",
    "categoryMarketingLabel": "Marketing",
    "categoryMarketingExcerpt": "Les cookies marketing sont utilisés pour effectuer le suivi des visiteurs au travers des sites Web. Le but est d'afficher des publicités qui sont pertinentes et intéressantes pour l'utilisateur individuel et donc plus précieuses pour les éditeurs et annonceurs tiers.",
    "categoryMarketingDescription": "Les cookies marketing sont utilisés pour effectuer le suivi des visiteurs au travers des sites Web. Le but est d'afficher des publicités qui sont pertinentes et intéressantes pour l'utilisateur individuel et donc plus précieuses pour les éditeurs et annonceurs tiers.",
    "categoryOtherLabel": "Autres cookies",
    "categoryOtherExcerpt": "Ecrire une description courte ici",
    "categoryOtherDescription": "Ecrire une description longue ici",
    "categoryIABLabel": "Services publicitaires de l'IAB",
    "categoryIABExcerpt": "Ces services utilisent les cookies principalement à des fin d'amélioration de la qualité des messages publicitaires.",
    "categoryIABDescription": "Ces services utilisent les cookies principalement à des fin d'amélioration de la qualité des messages publicitaires.",
    "cookieDeclaration": null,
    "buttonYes": "Oui",
    "buttonNo": "Non",
    "viewProof": "Afficher la preuve du consentement",
    "successMessage": "Vos préférences ont été sauvegardées ! Merci ! "
  },
  "groups": [
    {
      "label": "Marketing",
      "excerpt": "Les cookies marketing sont utilisés pour effectuer le suivi des visiteurs au travers des sites Web. Le but est d'afficher des publicités qui sont pertinentes et intéressantes pour l'utilisateur individuel et donc plus précieuses pour les éditeurs et annonceurs tiers.",
      "purpose": 3,
      "services": [
        {
          "id": "e213aca4-79b7-4b93-2bad-08d897969898",
          "name": "yrdy",
          "slug": "yrdy",
          "domain": "www.dastra.eu",
          "logoUrl": "https://api.dastra.eu/v1/favicon/www.dastra.eu",
          "privacyPolicyUrl": null,
          "defaultConsent": false,
          "requiredConsent": true,
          "purpose": 3,
          "description": null,
          "cookies": [
            {
              "id": "de529978-3ae0-496d-bf25-daac9d7230c7",
              "serviceId": null,
              "name": "yrdy",
              "description": null,
              "value": null,
              "path": null,
              "domain": null,
              "expiryDays": null
            }
          ],
          "lang": "fr"
        }
      ],
      "description": "Les cookies marketing sont utilisés pour effectuer le suivi des visiteurs au travers des sites Web. Le but est d'afficher des publicités qui sont pertinentes et intéressantes pour l'utilisateur individuel et donc plus précieuses pour les éditeurs et annonceurs tiers.",
      "requiredConsent": true,
      "defaultConsent": false
    }
  ],
  "lang": "fr",
  "versionKey": "36df80ee-235c-4485-b9e2-f28f5568f572",
  "lastVersionGeneration": "2020-12-03T14:28:55.5450603",
  "buttonLogoUrl": null,
  "enabled": true,
  "label": "www.dastra.eu",
  "displayLogo": true,
  "hideCopyright": false,
  "showFixedButton": true,
  "developerMode": true,
  "saveConsentProof": true,
  "isValid": false,
  "position": "BottomLeft",
  "timerTrigger": 0,
  "scrollTrigger": 0,
  "autoGeneratedCookieNotice": false,
  "cookieNoticeUrl": "",
  "bgColor": "#FFFFFF",
  "colorTitle": "#2E4058",
  "colorBtn": "#686868",
  "colorText": "#2E4058",
  "colorPrimary": "#E7630A",
  "colorSecondary": "#48ba61",
  "customCSS": "",
  "enableIAB": false,
  "tcfVersion": 1,
  "fontFamily": "'Segoe UI', Tahoma, Geneva, Verdana, sans-serif",
  "dateCreation": "2020-12-03T14:20:19.3703522",
  "dateUpdate": "2021-03-15T12:32:09.848664",
  "consentCookieExpiryTime": 180,
  "consentCookieName": null,
  "id": 1,
  "tenant": null,
  "tenantId": 1
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.dastra.eu" path="/v1/client/collect/:id?key=:key" %}
{% api-method-summary %}
Enregistrement des consentements
{% endapi-method-summary %}

{% api-method-description %}
Cette méthode permet de collecter les consentements aux cookies
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
ID of the widget configuration
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="key" type="string" required=true %}
The public api key
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="consents" type="object" required=false %}
 La liste des consentements de l'utilisateur  
  
`{  
"cookieConsents":  
[  
  {  
    "consent":true, // True if consented, false if refused  
    "id":"e213aca4-79b7-4b93-2bad-08d897969898", // Cookies id  
    "date":"2021-03-15T14:00:04.133Z",  
    "name":"yrdy",  
    "slug":"yrdy",  
    "purpose":3  
  }  
],  
"lang":"fr-FR",  
"consentId":"6f47576e-5a0c-4219-8efe-331e72bab73a",  
"date":1615809009744  
}`  
  
  
  
  
  
  
  
  
  
 
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
CookieEventType Visit,Quit,Consents
{% endapi-method-parameter %}

{% api-method-parameter name="consentId" type="string" required=false %}
The current consent Id \(If any collected before\)
{% endapi-method-parameter %}

{% api-method-parameter name="userId" type="string" required=false %}
Custom user id \(
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Return the id of the consent collected
{% endapi-method-response-example-description %}

```
140f213b-de17-4572-99a7-5075ccbcbbec
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}
