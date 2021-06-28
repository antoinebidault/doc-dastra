---
description: "Assurez-vous de ne pas manquer de nouvelles fonctionnalités et améliorations! \U0001F680"
---

# Journal des modifications

## 15 Septembre 2020 - Bêta 0.9.8

**Bugfixes** 

* 
**Fonctionnalités**

* Sécurité / authentification à 2 facteurs
* Sécurité / filtres sur adresses ip
* Sécurité / filtres des domaines des emails
* Sécurité / Possibilité de forcer l'authentification à deux facteurs pour tout le monde

**Améliorations**

* 
## 19 Aout 2020 - Bêta 0.9.7

**Bugfixes** 

* Suppression de requête d'exercice de droit qui plantait
* Enregistrement de requête d'exercice de droit qui plantait \(avec pièce jointe ou une fois la requête fermée par un utilisateur\)
* Bugs du widget de collecte des demandes d'exercice de droit



**Fonctionnalités**

* Messagerie des demandes d'exercice de droit : possibilité de communiquer avec le client avec un système de messagerie simple et efficace qui vous permettra également d'envoyer les pièces jointes.

On accède à la messagerie dans l'onglet message des exercices de droit :

![](../.gitbook/assets/image%20%28142%29.png)

* Espace de messagerie du client avec connection par token envoyé par email. L'envoi de pièce jointe est possible jusque 50 mo.
* Cloud documentaire dans la navigation gauche :

![](../.gitbook/assets/image%20%2889%29.png)

* Gestion de fichiers et dossiers du cloud documentaire complet
* Configuration du sender : [https://app.dastra.eu/workspace/1/settings/sender](https://localhost:63318/workspace/3009/settings/sender) : ce système vous permet de configurer l'apparence des emails envoyés depuis votre workspace : replyto, \(avec le nom\), couleur principale, le logo du workspace est automatiquement repris dans l'entête du mail.

**Améliorations**

* Prévisualisation du traitement au clic dans la liste des traitement
* Templating des emails: les emails de notification des utilisateurs externes \(Exercice de droit\) sont brandés avec la marque du client et sont localisés.
* Animations de chargements des tâches
* Ajout d'un système de traitement batch au tableau de demandes d'exercice de droit
* Traductions diverses revues et corrigées
* Ajout d'un système de notification prioritaires =&gt; elles sont envoyées sans transition ou accumulation à l'ensemble des destinataires.
* Ajout d'un cache mémoire sur la récupération d'un traitement de données pour améliorer sensiblement les performances
* Ajout de pièces jointes aux tâches

**Tests**

* e2e : login front-end
* e2e : login back-office + nav

## 22 Juillet 2020 - Bêta 0.9.6

Bugfixes

* Pagination des datasets
* Gestion des colonnes dans le registre
* Tri par tag : erreur 500
* Format word : bug de mise en forme des données du traitement
* Recherche dans le glossaire de données
* Affichage du plan d'action

Améliorations

* Editeur de texte riche \(Commentaires + gestion de dossier\)
* Ajout d'un ID unique aux demandes d'exercice de droit.

Fonctionnalités

* Stockage de documents au niveau du sous-traitant
* Nouveau gestionnaire de fichier avec des dossiers
* Relations inter-traitements \(Héritage strict ou léger\)
* Visualisation des audits de sécurité 
* Export des audits de sécurité

## 02 Juillet 2020 - Bêta 0.9.5

**Bugfixes**

* Recherche full text dans les selecteurs corrigée
* Import de fichier XLSX : problème de décalage des colonnes
* Export du glossaire des données qui plante
* Certaines règles de validation de traitement ne disparaissaient jamais
* La sauvegarde du workflow du registre impactait celle des demandes d'exercice et réciproquement

**Améliorations**

* Changements de conventions de nommage : règles de rétention =&gt; jeux de données
* Bouton retour à la fin du processus d'import
* Ajout d'un texte d'aide pour l'interface d'import
* Affichage du message d'erreur dans le cas d'un problème lors du scan des cookies \(En anglais seulement pour l'instant\)
* Transformation en popup du tableau de description des colonnes d'import
* Ordre des colonnes à importer/exporter revu légèrement
* Amélioration de l'affichage des règles de validation du traitement \(Avec dropdown\)
* Amélioration ergonomique du formulaire de demandes du support 
* Pour plus de commodités, lors de la création d'une équipe, possibilité d'affecter des membres à la volées.

**Fonctionnalités**

* Guide de démarrage de l'application
* Dans les "settings", possibilité de supprimer une entité ou un utilisateur dans la "Zone de danger" 
* Menu dropdown d'aide en bas à gauche de l'écran

![](../.gitbook/assets/image%20%28154%29.png)

## 27 Juin 2020 - Bêta 0.9.4

* Cartographie des traitement sous format graphique
* Allocation des objets dans les tâches
* Assignation de personnes aux exercices des droits
* Refonte des rôles et permissions avec possibilité de créer des rôles personnalisés

## 29 Mai 2020 - Bêta 0.9.3

* Vue des traitements sous forme d'arbre
* Correction de plusieurs bugs \(refus du consentement, changement de langue, traductions, violations de données\)

## 30 Avril 2020 - Bêta 0.9.2

* Un bug sur l'authentification des utilisateurs non actifs a été résolu.
* Le modèle de donnée a été revu pour accueillir un glossaire des données et les règles de conservation des données.

## 03 Février 2020 - Bêta 0.9.1

* La nouvelle bêta Dastra est rendu publique en tant que version 0.9.1 🚀🎉

Avant ça, la nouvelle version bêta publique était encore en bêta privée. 



