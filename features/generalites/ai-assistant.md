---
description: >-
  L'assistant IA de Dastra utilise la puisse de l'IA OpenAI GPT-4 pour générer
  automatiquement des fiches de traitement
---

# Assistant IA (beta)

{% hint style="info" %}
Cette page est en cours de construction car il s'agit d'une fonctionnalité en cours de développement
{% endhint %}

## Comment utiliser l'IA générative de Dastra ?

Vous pouvez utiliser l'assistant IA pour générer des traitements de données ou des actifs. Pour cela cliquez sur le bouton "Créer un traitement" et sur "générer avec IA". L'assistant IA vous fera une proposition de modèle de données que vous pourrez ensuite adapter à vos besoins.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>



{% hint style="warning" %}
**Que faire si je ne souhaite pas avoir cette fonctionnalité sur mon compte ?**

Si jamais vous ne souhaitez pas que cette option soit disponible dans votre espace de travail, vous pouvez nous contacter pour que nous désactivions la fonctionnalité au niveau de votre organisation.
{% endhint %}

## Comment ça marche ?

Dastra utilise le modèle d'**IA GPT 3.5 boost** fourni par le service OpenAI **hébergé sur Azure**. Nous utilisons un modèle pré-entrainé et **nous ne transférons aucune donnée de votre organisation** dans le but d'entraîner cette intelligence artificielle.&#x20;

Dastra utilise simplement la puissance de l'IA générative de GPT pour générer du contenu à partir de simple requête textuelle. Dastra a simplement fourni le modèle de document attendu (JSON) et un exemple de traitement de données (issu de notre bibliothèque) que nous souhaitons avoir et le modèle d'IA s'occupe du reste.

{% hint style="warning" %}
**Avertissement sur la qualité du contenu suggéré !**&#x20;

Les données générées par l'assistant **sont uniquement des propositions**. Il est nécessaires de bien relire et mettre à jour les informations générées automatiquement par l'assistant. Dastra ne s'engage pas sur la qualité des informations proposées.
{% endhint %}

Dastra **ne fait aucun transfert de données** présentes dans votre espace de travail vers le service d'IA.

{% hint style="info" %}
**Informations importantes sur l'utilisation des données d'entrée et de sortie de l'assistant IA (hébergé par Microsoft)**

Les requêtes textuelles et les résultats :

* **ne sont PAS disponibles pour d'autres clients**. ne sont PAS à la disposition de l'OpenAI.&#x20;
* **ne sont PAS utilisés pour améliorer les modèles de l'OpenAI**&#x20;
* **ne sont PAS utilisés pour améliorer les produits ou services de Microsoft** ou d'une tierce partie.&#x20;
* **ne sont PAS utilisées pour améliorer automatiquement les modèles Azure OpenAI** pour votre utilisation dans votre ressource (les modèles sont sans état, sauf si vous affinez explicitement les modèles avec vos données d'entraînement).&#x20;

Vos modèles Azure OpenAI affinés sont disponibles exclusivement pour votre usage. Le service Azure OpenAI est entièrement contrôlé par Microsoft ; Microsoft héberge les modèles OpenAI dans l'environnement Azure de Microsoft et le service n'interagit PAS avec les services exploités par OpenAI (par exemple, ChatGPT ou l'API OpenAI).
{% endhint %}

Si vous souhaitez avoir plus d'informations sur le fonctionnement de ce modèle, [rendez-vous sur cette page ](https://learn.microsoft.com/en-us/legal/cognitive-services/openai/data-privacy)
