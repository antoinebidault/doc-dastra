---
description: Pour s'authentifier sur l'API Dastra vous devez utiliser
---

# Authentification

L'API Rest Dastra utilise les clés d'API pour authentifiée chaque requête. Vous pouvez gérer vos clés dans l['interface de configuration de votre organisation](https://app.dastra.eu/general-settings/api).

Vous pouvez utiliser une clé d'API pour une entité ou l'organisation complète.

Votre clé d'API permet de faire beaucoup de chose, c'est pourquoi, vous devez la conserver précieusement. Ne partagez pas votre clé secrète dans les parties publiques d'applications comme GitHub, le code client...etc...

L'authentification de l'API s'effectue grâce à l'aide du protocole [HTTP Basic Auth](http://en.wikipedia.org/wiki/Basic_access_authentication). Fournissez votre clé d'API en temps que nom d'utilisateur. Le mot de passe n'est pas nécessaire \(Vous pouvez en mettre un aléatoire comme 123\).

```text
curl https://api.dastra.eu/v1/actors\
  -u asdskdskgfdkghfdkhg:
# The colon prevents curl from asking for a password.
```

{% hint style="info" %}
Les requêtes cross-orgin ne sont pas autorisées par l'API. Il ne faut donc jamais effectuer de requêtes vers l'API REST en passant la clé secrète en clair côté client ! 

Elles seront de toutes façon bloquées par le navigateur avec CORS
{% endhint %}

Toutes les requêtes doivent s'effectuer en [HTTPS](http://en.wikipedia.org/wiki/HTTP_Secure) et toujours côté serveur. Les requêtes sans authentification échoueront avec le code d'erreur 401

Consultez les références de l'API ici : [https://api.dastra.eu/swagger/index.html](https://api.dastra.eu/swagger/index.html)  


