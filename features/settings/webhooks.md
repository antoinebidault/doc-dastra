---
description: Vous saurez tout sur l'intégration de webhooks dans Dastra
---

# Webhooks

## Concept

Pour faire simple, les webhooks permettent de **déclencher une action** suite à un événement. Ils sont généralement utilisés pour faire communiquer des systèmes. C’est la façon la plus simple de recevoir une alerte lorsque quelque chose se produit dans un autre système. L'objectif est de notifier les systèmes en temps réel



## Configuration 🛠️

Pour configurer vos webhooks, rendez-vous sur la page : [https://app.dastra.eu/general-settings/webhooks](https://app.dastra.eu/general-settings/webhooks)

![](<../../.gitbook/assets/image (252).png>)

* Cliquez sur créer une "url de webhook"
* Renseignez l'url
* Renseignez l'espace de travail concerné
* Sélectionnez le ou les évènements auxquels vous souhaitez vous abonner. Le type de données renvoyés sera différent selon le type d'évènement.
* Enregistrez le webhook

Vous arrivez sur l'**écran de détail du webhook.**

![](<../../.gitbook/assets/image (254).png>)



## Test

Vous allez pouvoir tester votre webhook en condition réelle **en cliquant sur le bouton "Tester"**



## Comment sécuriser le webhook ? 🛡️

{% hint style="info" %}
Même si ce n'est pas une obligation, il est **recommandé de valider la requête entrante** du webhook pour éviter les attaques potentielles d'un hackeur qui aurait sniffé le réseau et serait ainsi en capacité de poster n'importe quoi sur votre url de webhook.
{% endhint %}

Chaque fois qu'une requête de modification, suppression d'un élément de Dastra est effectuée, nous allons poster un objet sur toutes les urls que vous avez configurés sur l'évènement voulu. Dans chaque requête POST figurera une entête **Dastra-Signature**, cette entête peut être récupérée côté serveur.&#x20;

Cette entête correspond à l'intégralité du JSON posté encrypté en HMAC256 à l'aide de la clé de validation du webhook.

> DastraSignature = HMAC256(\<JSON sérialisé du POST>,\<clé de validation du webhook>)

Quelques exemples de code de validation :

{% tabs %}
{% tab title="PHP" %}
```php
error_reporting(E_ALL);
ini_set('display_errors', 1); 
c
$secret = "your dastra validation key";// your secret key
$payload = "";// equest body
$headers = "";// request message headers array

$signature = "";// the HMAC hash key in the HTTP header x-docusign-signature-1
$result = false;// verification result

if (isset($_POST)) {
    try {
        $payload = file_get_contents('php://input');
        $headers = get_ds_headers();
        if (array_key_exists("Dastra-Signature", $headers)) {
            $signature = $headers["Dastra-Signature"];
            $result = hash_is_valid($secret, $payload, $signature);
            log_result($signature, $payload, $result);
        }
     } catch (Exception $e) {
        logger("\nException: " . $e->getMessage() . "\n");
    }
    header("HTTP/1.1 200 OK");
}

function get_ds_headers()
{
    $headers = array();
    foreach ($_SERVER as $key => $value) {
        if (strpos($key, 'HTTP_') === 0) {
            $headers[str_replace(' ', '', ucwords(str_replace('_', ' ', strtolower(substr($key, 5)))))] = $value;
        }
    }
    return $headers;
}
 
function compute_hash($secret, $payload)
{
    $hexHash = hash_hmac('sha256', $payload, utf8_encode($secret));
    $base64Hash = base64_encode(hex2bin($hexHash));
    return $base64Hash;
}
 
function hash_is_valid($secret, $payload, $verify)
{
    $computed_hash = compute_hash($secret, $payload);
     return hash_equals($verify,$computed_hash);
 }
```
{% endtab %}

{% tab title="C#" %}
```csharp

public IActionResult Handle(){
    string dastraSignature = Request.Headers["Dastra-Signature"];
    string key = "Your validation key";
    string payload = GetRequestBody();
    
}

public static bool ValidateSignature(string signature, string payload, string secret)
{
    using (var hmacsha256 = new HMACSHA256(Encoding.UTF8.GetBytes(secret)))
    {
        var hash = hmacsha256.ComputeHash(Encoding.UTF8.GetBytes(payload));
        var result = Convert.ToBase64String(hash);
    }
    
    return result.Equals(signature)
}

public static string GetRequestBody()
{
    var bodyStream = new StreamReader(Request.InputStream);
    bodyStream.BaseStream.Seek(0, SeekOrigin.Begin);
    var bodyText = bodyStream.ReadToEnd();
    return bodyText;
}
```
{% endtab %}
{% endtabs %}

## Dépannage

Le webhook sera automatiquement bloqué et considéré en erreur quand le seuil de 5 erreurs est dépassé.
