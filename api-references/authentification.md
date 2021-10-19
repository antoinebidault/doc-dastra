---
description: Pour s'authentifier sur l'API Dastra vous devez utiliser
---

# Authentification

### Obtention de la clé secrète d'API

L'API Rest Dastra utilise les clés d'API pour authentifier chaque requête. Vous pouvez gérer vos clés dans l['interface de configuration de votre organisation](https://app.dastra.eu/general-settings/api).&#x20;

Vous pouvez utiliser une clé d'API pour un espace de travail spécifique ou l'organisation complète.

Votre clé d'API permet de faire beaucoup de chose, c'est pourquoi, vous devez la conserver précieusement. Ne partagez pas votre clé secrète dans les parties publiques d'applications comme GitHub, le code client...etc...

### Méthode d'authentification

L'authentification de l'API s'effectue grâce à l'aide du [protocole OAuth2](https://oauth.net/2/) utilisant le flow "Client credential". Ce mode d'authentification doit être utilisé uniquement pour des requêtes de serveur à serveur et ne doit en aucun cas être utilisé côté navigateur (SPA en javascript par exemple).

![](<../.gitbook/assets/API authentication scheam.svg>)

### Récupération du token

{% swagger method="post" path="/connect/token" baseUrl="https://account.dastra.eu" summary="" %}
{% swagger-description %}
Perform a token request using BASIC Headers
{% endswagger-description %}

{% swagger-parameter in="body" type="scope" required="true" %}
api1
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" type="grant_type" %}
client_credentials
{% endswagger-parameter %}

{% swagger-parameter in="header" type="Authorization" required="true" %}
Basic {base64("{PublicKey}:{PrivateKey}")}
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="The access_token necessary to perform operations on the REST API" %}
```javascript
{
  "access_token":"tNQoqsSePv0DnSSNVJv1aDxzSFh9H2z3YBKtuBKqWAU",
  "expires_in":3600,
  "token_type":"Bearer",
  "scope":"api1"
}
```
{% endswagger-response %}
{% endswagger %}

Une fois que vous avez récupéré un access\_token, vous pouvez ensuite appeler n'importe quel endpoint de l'API Rest à l'aide de ce jeton d'accès en le passant en "Bearer token".&#x20;

Par exemple, pour récupérer la liste de vos espaces de travail :

{% swagger method="get" path="" baseUrl="https://api.dastra.eu/v1/workspaces" summary="" %}
{% swagger-description %}
Récupérer la liste des espaces de travail de Dastra
{% endswagger-description %}

{% swagger-parameter in="header" type="Authorization" required="true" %}
Bearer {access_token}
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
  "items": [
    {
      "id": 1,
      "tenantId": 1,
      "label": "My data company",
      "logoUrl": null,
      "state": "Active",
      "permissions": null,
      "dataSubjectArchivedRetentionDays": null,
      "nbEntities": 1
    },
    {
      "id": 2,
      "tenantId": 1,
      "label": "My test workspace",
      "logoUrl": null,
      "state": "Active",
      "permissions": null,
      "dataSubjectArchivedRetentionDays": null,
      "nbEntities": 1
    },
    {
      "id": 3,
      "tenantId": 1,
      "label": "My experimentation workspace",
      "logoUrl": null,
      "state": "Active",
      "permissions": null,
      "dataSubjectArchivedRetentionDays": null,
      "nbEntities": 0
    }
  ],
  "total": 3
}
```
{% endswagger-response %}
{% endswagger %}



{% hint style="info" %}
Pour l'instant, les requêtes cross-orgin ne sont pas autorisées par l'API. Il ne faut donc jamais effectuer de requêtes vers l'API REST côté client !&#x20;

Elles seront de toutes façon bloquées par le navigateur avec CORS.

Si vous avez besoin de cette fonctionnalité, n'hésitez pas à nous envoyer un mail à [contact@dastra.eu](mailto:contact@dastra.eu).
{% endhint %}

Toutes les requêtes doivent s'effectuer en [HTTPS](http://en.wikipedia.org/wiki/HTTP\_Secure) et toujours côté serveur. Les requêtes sans authentification échoueront avec le code d'erreur 401

Consultez les références de l'API ici : [https://api.dastra.eu/swagger/index.html](https://api.dastra.eu/swagger/index.html)\
