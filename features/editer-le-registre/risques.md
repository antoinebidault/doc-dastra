---
description: >-
  Dastra permet de cartographier les risques liés aux traitements afin d’évaluer
  rapidement le niveau de priorité et les actions à mener sur un traitement de
  données.
---

# Associer un risque au traitement

### Définition des risques

Un risque de sécurité est défini par l’Agence nationale de la sécurité des systèmes d’information \(ANSSI\) comme étant un scénario qui combine un **événement redouté** \(sources de menaces, bien essentiel, critère de sécurité, besoin de sécurité, impacts\) et **un ou plusieurs scénarios de menaces** \(sources de menaces, bien support, critère de sécurité, menaces, vulnérabilités\).

On peut distinguer plusieurs typologies de risques :   


* les risques liés à la sécurité 
  * atteinte à la confidentialité des données
  * atteinte à la disponibilité des données
  * atteinte à l’intégrité des données
* les risques juridiques
  * violation du secret professionnel 
  * responsabilité civile délictuelle et contractuelle
  * responsabilité pénale
  * perte de conformité à des référentiels légaux, réglementaires, normatifs, sectoriels ou internes

Le **niveau de risque** est évalué en fonction de la gravité de son impact et de la vraisemblance de réalisation.

La **gravité** représente l'ampleur d'un risque. Elle est estimée au regard des conséquences de la réalisation de la menace. 

La **vraisemblance** traduit la possibilité qu'un risque se réalise. Elle est estimée au regard des vulnérabilités et de la capacité, le cas échéant, des sources de risques à les exploiter.  



### Ajouter un risque dans un traitement 

Pour ajouter un risque sur un traitement, il faut aller dans l'onglet risques présent sur la page d'édition du traitement.

![](../../.gitbook/assets/image%20%2812%29.png)

et cliquer sur le bouton "Créer un risque".

![](../../.gitbook/assets/image%20%28128%29.png)

Vous arrivez sur une page d'édition du risque et vous pouvez commencer à renseigner les informations concernant le risque que vous avez identifié. 

![](../../.gitbook/assets/image%20%28174%29.png)

Vous pouvez ensuite retrouver tous les risques de votre registre dans le référentiel des risques.

![](../../.gitbook/assets/image%20%28138%29.png)



### Visualiser les risques

Sur chaque traitement, vous pouvez afficher le niveau de risque associé. Pour cela, il suffit de sélectionner l'élément dans l'onglet "Colonnes".

![](../../.gitbook/assets/image%20%2816%29.png)

Ensuite, sélectionnez "Niveau de risque".

![](../../.gitbook/assets/image%20%28167%29.png)

Vous afficherez le niveau de risque associé : 

![](../../.gitbook/assets/image%20%2897%29.png)

Le niveau de risque est calculé selon la formule suivante :

`Niveau de risque = valeur de probabilité X valeur d'impact`   


Dans le tableau de bord, un module de risque présente le nombre de risques, les traitements avec les risques les plus élevés, le risque global et le niveau du traitement ayant le plus de risques. 

Le risque global est calculé selon la formule suivante :  


`somme (probabilité* impact ) / nombre de risques`  
  
****

Le niveau du traitement ayant le plus de risque est calculé selon la formule suivante :  


`((impact x probabilité) / 25)`  
****







\*\*\*\*

\*\*\*\*

\*\*\*\*

\*\*\*\*

\*\*\*\*

\*\*\*\*

