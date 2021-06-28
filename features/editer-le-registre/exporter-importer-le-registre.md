---
description: Apprenez à exporter et importer un registre existant complet dans Dastra.
---

# Exporter / importer le registre

## L'export de registre

Pour exporter l'ensemble du registre, il vous suffit de vous rendre dans la fonctionnalité "Registre", de cliquer sur les 3 petits points en haut à droite, puis de sélectionner "exporter le registre".

![](../../.gitbook/assets/image%20%2856%29.png)

Choisissez ensuite le format d'export ainsi que le template d'export désiré \(par exemple "article 30"\), et cliquez sur "Télécharger le fichier". Ca y est, votre registre est exporté !

{% hint style="info" %}
Il est également possible de n'exporter qu'un ou plusieurs traitements du registre, au lieu du registre entier. Pour cela, sélectionnez les traitements concernés manuellement en cochant les cases à gauche du registre, puis "Action groupée" et "Exporter".
{% endhint %}

## L'import de registre

Pour éviter de remplir chaque traitement à la main et prendre en compte tous les formats possibles de registre, Dastra a conçu une méthodologie se reposant sur le principe de la **ségrégation du registre en domaines de données**. Ainsi, 9 étapes sont conseillées pour importer l’ensemble d’un registre existant dans Dastra.

{% hint style="info" %}
Ces étapes, non obligatoires, sont néanmoins fortement conseillées notamment lorsque le registre de traitement contient de nombreux traitements.
{% endhint %}

N'hésitez pas à consulter également les référentiels de la CNIL mis à disposition par Dastra  dans la page suivante:



## Etape 1 : Import des labels de traitement

Pour importer vos labels de traitements existants, il faut cliquer sur l'onglet "importer vos données" dans la section Registre, onglet Registre:

![](../../.gitbook/assets/image%20%28110%29.png)

Ensuite, téléchargez un échantillon de notre fichier tel que présenté à l'écran.

![](../../.gitbook/assets/image%20%2862%29.png)



Remplissez le fichier  téléchargé avec vos labels de traitements en respectant l'ordre suivant :

| Colonne | Description | Valeurs possibles |
| :--- | :--- | :--- |
| Ref | Référence interne \(string\) |  |
| Processing state | Etat du traitement \(processing state\) | "Study", "BeingDeployed", "InProduction", "Stopped" |
| Label | Nom \(string\) |  |
| Description | Description \(String\) |  |

Ci-dessous un exemple de fichier respectant le format demandé disponible à l'import et pouvant être importé en "glisser-déposer" dans Dastra :

{% file src="../../.gitbook/assets/sample-datatreatments-shipbuilder-3-.xlsx" %}

Importez-le directement dans notre interface par glisser-déposer, puis cliquez sur Continuez. 

Ca y est, vos labels de traitements sont importés !

## Etape 2 : import du référentiel des applications

Pour importer vos applications existantes, il faut cliquer sur l'onglet "importer vos données" dans la section Registre, onglet Application:

![](../../.gitbook/assets/image%20%2864%29.png)

Ensuite, téléchargez un échantillon de notre fichier tel que présenté à l'écran. Remplissez le fichier  téléchargé avec vos applications en respectant l'ordre suivant :

| Colonne | Description | Valeurs possibles |
| :--- | :--- | :--- |
| Description | Description \(string\) |  |
| Label | Nom \(string\) |  |
| ApplicationState | Application state \(applicationstate\) | "InProduction""InDevelopment""Stopped" |
| ApplicationType | Application type \(applicationtype\) | "Software""WebApp""Saas""Module""Other" |
| HostingType | Hosting type \(hostingtype\) | "InHouse""OutSourced" |
| SupportType | Support type \(supporttype\) | "InHouse""OutSourced" |
| DevelopmentType | Development type \(developmenttype\) | "InHouse""OutSourced" |
| HostName | Host name \(string\) |  |
| PrivacyByDesignImplemented | Privacy by design implemented \(boolean\) | "true""false" |

Ci-dessous un exemple de fichier respectant le format demandé disponible à l'import et pouvant être importé en "glisser-déposer" dans Dastra :

{% file src="../../.gitbook/assets/sample-applications-example.xlsx" %}

Importez-le directement dans notre interface par glisser-déposer, puis cliquez sur Continuez. 

Ca y est, vos applications sont importées !

## Etape 3 : import du référentiel des acteurs

Recommencez la procédure similaire aux précédentes depuis  la section Registre, onglet Acteurs. Ci-dessous un exemple:

{% file src="../../.gitbook/assets/sample-actors-example-xls.xlsx" %}

## Etape 4 : import du référentiel des sous-traitants

Recommencez la procédure similaire aux précédentes depuis  la section Registre, onglet Sous-traitants. Ci-dessous un exemple:

{% file src="../../.gitbook/assets/sample-vendor-csv.csv" %}

## Etape 5  : import du référentiel des clients

Recommencez la procédure similaire aux précédentes depuis  la section Registre, onglet Clients.

## Etape 6 : import du référentiel des mesures de sécurité

Recommencez la procédure similaire aux précédentes depuis  la section Registre, onglet Mesures de sécurité.

## Etape 7 : import du glossaire de données

Recommencez la procédure similaire aux précédentes depuis  la section Registre, onglet Glossaire de données.

## Etape 8 : import du référentiel de règle de conservation 

Recommencez la procédure similaire aux précédentes depuis  la section Registre, onglet Règles de conservation.

## Etape 9 : Construction des liaisons 

Maintenant que les référentiels ont tous été importés, éditez chacun des traitements et remplissez les informations sur la bases des informations importées en suivant le guide ci-dessous:

{% page-ref page="remplir-le-questionnaire/" %}

Ca y est, les liaisons sont construites !



