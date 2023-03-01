---
description: >-
  Apprenez à renseigner les catégories de données ainsi que les règles de
  conservation associées spécifiques à un traitement.
---

# Données et conservation

{% embed url="https://www.youtube.com/watch?v=BJSynYF0aDw&list=PL-EvtNdEiDxEUikz6mrcMlKZ54r3RpBLZ&index=6" %}

[**L’article 30 du RGPD**](https://www.cnil.fr/fr/reglement-europeen-protection-donnees/chapitre4) exige également l’inscription des catégories de données traitées.

Il s’agit ici de définir les catégories de données traitées. Celles-ci peuvent être dites courantes ou sensibles. On distingue en effet les données qui présentent un risque plus important sur les personnes physiques tel que les données relatives à la santé des personnes, les données relatives aux opinions politiques ou à l’activité syndicale. Les données relatives à des infractions ou autres mesures d’exécution de peines constituent également des données particulièrement protégées.&#x20;

De même, le numéro d’inscription au répertoire (NIR) ou numéro de sécurité sociale peut être assimilé à une donnée sensible.&#x20;

La collecte de données sensibles est par principe interdite. Seules les exceptions prévues à l’[**article 9 du RGPD**](https://www.cnil.fr/fr/reglement-europeen-protection-donnees/chapitre2) permettent de les collecter.



## Jeux de données

Le jeu de données regroupe les données d'un élément précis, par exemple, une table dans une base de données ou un formulaire de collecte papier.

### Plusieurs cas d'usage des jeux de données

Les jeux de données peuvent être utilisés selon plusieurs manières :

* **Cas n°1** : en associant **un jeu de données à un actif unique**. Dans ce cas, le jeu de données correspond aux données de l'actif et n'est pas générique
* **Cas n°2** : en associant **un jeu de données au traitement de données**. Ce jeu de données peut être spécifique au traitement de données et n'est pas réutilisé dans un autre traitement de données
* **Cas n°3** : en associant des **jeux de données génériques au traitement de données**. Dans ce cas, le jeu de données peut être réutilisé dans plusieurs traitements de données.

Pour utiliser les jeux de données génériques, nous recommandons la procédure suivante :

* Ouvrir la page du traitement concernant les jeux de données
* Ouvrir un nouvel onglet sur la page des jeux de données dans la cartographie
* Sélectionner le jeu de données dans le traitement de données
* Si le jeu de données doit être modifié, il faut en créer un autre : se rendre sur l'autre onglet et dupliquer le jeu de données générique en enlevant ou en ajoutant les champs souhaités
* Pour plus de clarté, il est recommandé d'utiliser un tag pour ces jeux de données (cela vous permettra de les distinguer facilement dans le sélecteur de jeux de données). Par exemple : un tag "générique" et un tag concernant la donnée ajoutée ou enlevée

#### Utiliser des jeux de données sans champs

Par ailleurs, il est possible de rester encore plus générique en ne précisant pas les données associées au jeu de données mais en nommant le jeu de données en tant que catégorie de données (ce qui est également valable au sens du RGPD par exemple).

Selon les traitements, vous pouvez avoir des approches différentes, en fonction de la sensibilité qu'ils présentent au regard des droits et libertés des personnes concernées.

### Associer la source des données dans le jeu de données

Dans chaque jeu de données, vous pouvez inscrire l'origine des données. Celle est soit directe, soit indirecte, soit les deux.&#x20;

Un champ vous permettant de décrire l'origine de la collecte permet d'apporter la précision nécessaire.

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption><p>Source des données</p></figcaption></figure>



## Conservation des données

La conservation limitée des données fait partie des principes généraux du droit des données à caractère personnel et est rappelée à l’[**article 5 1. e) du RGPD**](https://www.cnil.fr/fr/reglement-europeen-protection-donnees/chapitre2). Celui-ci prévoit en effet que « _conservées sous une forme permettant l'identification des personnes concernées pendant une durée n'excédant pas celle nécessaire au regard des finalités pour lesquelles elles sont traitées_ ».

Concrètement, cela signifie que lors de la mise en œuvre d’un traitement de données, il faut penser à son devenir lorsque la finalité aura été accomplie. La donnée devra être soit détruite de manière définitive, soit anonymisée, soit traitée pour une nouvelle finalité compatible.&#x20;

La durée de conservation dépend de la finalité du traitement et de la nature des données. Les durées de conservation peuvent être définies en fonction des types de données. Par exemple, pour la gestion de la paie, les données relatives au bulletin de salaire sont conservées 1 mois en base active et 5 ans en archivage intermédiaire tandis que les données relatives à l’ordre de virement pour paiement sont conservées le temps nécessaire à l’émission du bulletin de paie en base active et 10 ans à compter de la clôture en archive intermédiaire.&#x20;

La durée peut être exprimée en valeur ou, si ce n’est pas possible, les critères utilisés pour définir la période de conservation (jusqu’à la désinscription par exemple). Il est recommandé, en particulier par la CNIL dans sa [**recommandation du 11 octobre 2005 sur l’archivage électronique dans le secteur privé**](https://www.legifrance.gouv.fr/affichCnil.do?id=CNILTEXT000017651957), de mettre en place des procédures permettant de gérer les durées de conservation au niveau de la catégorie de données et en particulier, de gérer les purges ou destructions de données.

#### Personnaliser les règles de conservation d'un jeu de données

Les champs de données d'un jeu de données générique ne peuvent pas varier d'un traitement à l'autre. Cependant, la durée de conservation peut être différente. En effet, il est possible de personnaliser la durée de conservation d'un jeu de données en fonction du traitement. Ainsi, la durée de conservation du jeu de données ne sera plus prise en compte.&#x20;

Pour cela, il est nécessaire d'ajouter le jeu de données au traitement. Sur la liste des jeux de données, il faut cliquer sur les boutons "base active/...".

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Bouton "base active"</p></figcaption></figure>

Vous pourrez voir apparaitre la fenêtre de personnalisation.&#x20;

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption><p>Fenêtre de personnalisation des durées de conservation</p></figcaption></figure>

Lorsque la durée de conservation est personnalisée au niveau du traitement, un petit logo de stylo apparait sur le bouton concerné :&#x20;

L'objectif à terme peut être de limiter l'utilisation de jeux de données génériques et de s'orienter vers une cartographie plus précise soit via les traitements de données (cas n°2) soit via les actifs (cas n°1).

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Durée personnalisée au niveau du traitement</p></figcaption></figure>



####

##

\
