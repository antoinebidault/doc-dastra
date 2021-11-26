---
description: >-
  Cette page vous explique comment envoyer directement une demande d'exercice de
  droit sans intégrer le SDK javascript en passant par l'API Rest
---

# Intégration de l'API

Si vous souhaitez intégrer les demandes d'exercices de droits au sein d'une application qui n'utilise pas Javascript (ex: application mobile, système embarqués, application desktop...). Dastra ne s'intègre pas nativement à toutes les plateformes de développement mobile et ne supporte que la version Javascript. Il est cependant possible de poster directement une demande en intégrant votre propre formulaire en utilisant le endpoint suivant :

{% swagger method="post" path="" baseUrl="https://api.dastra/eu/v1/client/save-request/{id}" summary="Create a data subject request" %}
{% swagger-description %}
On success, an email is sent to the user using identity validation
{% endswagger-description %}

{% swagger-parameter in="body" name="email" required="true" %}
Data subject request
{% endswagger-parameter %}

{% swagger-parameter in="body" name="message" %}
Subject's message (html is not authorized)
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" %}
ApiKey <your public key>
{% endswagger-parameter %}

{% swagger-parameter in="body" name="refId" %}
A specific identifier provided by the customer (Reservation number, Social security number, identity card number....)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="givenName" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="familyName" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="userId" %}
A userId provided by the js SDK if he is in an authorized environment (intranet)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="additionalDatas" %}
A dynamic object containing specific key value pairs (for custom fields for example)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="purpose" %}
Unknown, Information, Access, Rectification, Erasure, Restriction, Opposition, Portability, AdvanceDirectives
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="An email is sent automatically to the provided email" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}
