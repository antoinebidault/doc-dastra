---
description: Fonctionnement des modèles de messages
---

# Modèles de messages

## Personnalisation des modèles de messages



Pour optimiser votre temps et gagner en efficacité, vous pouvez paramétrer des modèles de messages à réutiliser dans les modules de Dastra.



### Types de modèles de messages accessibles&#x20;

Les types de modèles sont les suivants :

<figure><img src="../../.gitbook/assets/image (3) (1) (2).png" alt=""><figcaption></figcaption></figure>

*   **Message dans les demandes d'exercice des droits**

    Lors des échanges avec les demandeurs, vous pouvez enregistrer des modèles pour gagner du temps. Par exemple, un modèle d'accusé réception de la demande.
*   **Tâche**

    Vous pouvez personnaliser le contenu de la description d'une tâche. Idéal pour gagner du temps sur des tâches répétitives. Par exemple, quand vous demandez à quelqu'un de renseigner des éléments sur un traitement de données, vous pouvez réutiliser le même modèle de message.&#x20;
*   **Audits**

    Vous pouvez personnaliser les invitations à répondre à un audit. Utilisez ici un modèle pour inscrire le même message pour tous vos répondants. Par exemple, vous pouvez inviter vos sous-traitants à renseigner un audit de vérification de la bonne application du contrat de sous-traitance à partir d'un modèle créé à l'image de votre organisation.
*   **Compléter un traitement**

    Vous pouvez inviter un utilisateur de Dastra à compléter un traitement de données à partir d'une étape. Ecrivez une fois le modèle ou sélectionnez un modèle en fonction de la qualité du destinataire (juriste, DSI etc.) pour gagner du temps.&#x20;

### Création du modèle

La création de modèle s'effectue soit à partir des réglages de l'espace de travail, soit à partir du lieu du message.&#x20;

<figure><img src="../../.gitbook/assets/image (1) (1) (2) (1).png" alt=""><figcaption><p>Création depuis les réglages de l'espace de travail</p></figcaption></figure>

Cliquez sur Créer modèle

<figure><img src="../../.gitbook/assets/image (4) (1) (2).png" alt=""><figcaption><p>Interface de création d'un modèle</p></figcaption></figure>

N'oubliez pas d'enregistrer votre travail !

### Variables personnalisées dans les modèles

Dastra vous permet de **remplir automatiquement le modèle avec des variables personnalisées**.&#x20;

Cela signifie que vous pouvez inclure automatiquement des informations concernant l'objet lié au modèle dans le texte du modèle de message.&#x20;

Par exemple, dans l'invitation à répondre à un audit, il sera possible de reprendre automatiquement la date d'échéance d'un audit.&#x20;

<figure><img src="../../.gitbook/assets/image (2) (1) (2).png" alt=""><figcaption><p>Les champs personnalisés du message d'invitation à répondre à un audit</p></figcaption></figure>



Vous pouvez ainsi ajouter facilement des champs dynamiques directement dans le modèle. En tant que langage de création de modèles, nous utilisons la synthax liquidJS.&#x20;

Voici le guide complet ici : [les tags ](https://liquidjs.com/tags/overview.html)et [les filtres](https://liquidjs.com/filters/overview.html).&#x20;

Pour traduire les statuts, vous pouvez utiliser le filtre personnalisé getTranslation de cette manière \{{data | getTranslation: ''\}}. Exemple : \{{data | getTranslation: 'dataSubjectRequestStates'\}}



Les champs variables sont les suivants :&#x20;



|   |   |   |
| - | - | - |
|   |   |   |
|   |   |   |
|   |   |   |
