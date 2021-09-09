# Créer une relation entre les traitements

Dans Dastra vous avez la possibilité de créer des relations entre vos traitements afin de faciliter leur gestion.

Ces relations sont possibles entre des traitements situés dans un même espace de travail mais également au sein d'espaces de travail différents.



### Ajouter une relation

Pour ce faire, il faut aller sur une fiche de traitement et sélectionner l'onglet "Relations" situé en haut de la fiche.



![L&apos;onglet &quot;Relations&quot;](../../.gitbook/assets/image%20%28245%29.png)



Ensuite, il faudra sélectionner un type de relations.

![](../../.gitbook/assets/image%20%28244%29.png)

Vous pouvez sélectionner le type de relation entre les traitements.

![](../../.gitbook/assets/image%20%28246%29.png)





### Détail des relations

#### Est l'enfant de : 

Relation hiérarchique permettant la visualisation graphique. Pas d’asservissement entre les champs.

Le traitement A est hiérarchiquement sous le traitement B.

#### Est le parent de : 

Relation hiérarchique permettant la visualisation graphique. Pas d’asservissement entre les champs.

Le traitement A est hiérarchiquement au dessus du traitement B.

#### Est relatif à : 

Simple lien logique entre 2 traitements, aucun asservissement entre les deux ni de règle de contrôle. 

#### Est copié par :

Cette relation permet de garder une trace des éléments dupliqués à partir de ce traitement. Un lien relationnel est créé automatiquement lorsqu’un traitement est dupliqué. 

#### Est une copie de : 

Cette relation permet de garder une trace de la source de duplication du traitement. Un lien relationnel est créé automatiquement lorsqu’un traitement est dupliqué. 

#### Transmet strictement \(Héritage fort\) :

Les champs du traitement d'origine \(A\) remplacent les champs du traitement cible \(B\). 

Asservissement strict entre le traitement A et le traitement B. Les champs du traitement B préexistants sont supprimés au moment où le lien est mis en place. Les champs du traitement B asservis au traitement A ne sont pas modifiables dans le traitement B, et aucun nouveau champ ne peut être ajouté, supprimé ou modifié. Dans la mesure où les éléments de référentiels sont conservés, les champs préexistants au traitement B sont rétablis lorsque le lien est révoqué.

#### Hérite strictement de \(Héritage fort\) : 

Les champs du traitement cible \(B\) remplacent les champs du traitement d'origine \(A\). 

Asservissement strict entre le traitement B et le traitement A. Les champs de A préexistants sont supprimés au moment où le lien est mis en place. Les champs de A asservis à B ne sont pas modifiables dans A, et aucun nouveau champ ne peut être ajouté, supprimé ou modifié. Dans la mesure où les éléments de référentiels sont conservés, les champs préexistants au traitement B sont rétablis lorsque le lien est révoqué.

#### Hérite de \(Héritage faible\) : 

Le traitement cible \(B\) hérite automatiquement des champs du traitement d'origine \(A\). 

Il est possible d'ajouter, de supprimer ou modifier des nouveaux champs dans le traitement B, mais ne peut pas modifier les champs hérités du traitement A. Toute modification dans les champs du traitement A est automatiquement répercutée dans les champs hérités du traitement B . Lorsque le lien est révoqué, les champs hérités du traitement A redeviennent modifiables dans le traitement B. Les champs préexistant dans le traitement B avant la mise en place du lien sont conservés une fois le lien créé.

#### Transmet \(Héritage faible\) : 

Le traitement d'origine \(A\) transmet automatiquement ses champs au traitement cible \(B\). 

Le traitement cible B hérite automatiquement des champs du traitement d'origine A. Le traitement cible B peut ajouter, supprimer ou modifier des nouveaux champs, mais ne peut pas modifier les champs hérités du traitement A. Toute modification dans les champs du traitement A est automatiquement répercutée dans les champs hérités du traitement B. Lorsque le lien est révoqué, les champs hérités redeviennent modifiables dans le traitement B. Les champs préexistant à B avant la mise en place du lien sont conservés une fois le lien créé.



