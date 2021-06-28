---
description: Apprenez à utiliser Dastra étape par étape à travers un exemple concret.
---

# Premières étapes

## Exemple de cas : l'entreprise SHIPBUILDER \(cas fictif\)

Vous êtes chef d'entreprise de SHIPBUILDER, une organisation qui construit des bateaux. Celle-ci est composée de 8 départements:

* RH
* Secrétariat Général
* Production
* Marketing & ventes 
* Sécurité
* Informatique
* Juridique
* Achats

Vous avez décidé de mettre votre entreprise en conformité avec le Règlement Général de la Protection des Données \(RGPD\). Après avoir lu l'[article de la CNIL sur la préparation RGPD en six étapes](https://www.cnil.fr/fr/principes-cles/rgpd-se-preparer-en-6-etapes), vous débutez sans plus attendre.

## Etape 1 : Désigner un délégué à la protection des données \(DPO\)

Tout d'abord, vous vous êtes renseigné sur le [rôle du DPO](https://www.cnil.fr/fr/designer-un-pilote) et les conditions à remplir pour nommer un DPO, puis vous décider de [désigner un DPO](https://www.cnil.fr/fr/designation-dpo) afin notamment de réduire les risques de contentieux. Votre choix s'arrête sur un collaborateur qui, à son tour, définit et anime un réseau de correspondants RGPD au sein des différents métiers de l'entreprise.

{% hint style="info" %}
La désignation d'un délégué à la protection des données \(DPO\) est **obligatoire** uniquement pour:

* Les organismes publics ;
* Les entreprises dont l'activité de base les amène à réaliser un suivi régulier et systématique des personnes à grande échelle, ou à traiter à grande échelle des données dites "sensibles" ou relatives à des condamnations pénales et infractions. 
{% endhint %}

## Etape 2 : Cartographier vos traitements de données à caractère personnel et établir le registre

Après vous avoir [formés à la cartographie des traitements ](https://www.cnil.fr/fr/cartographier-vos-traitements-de-donnees-personnelles)et avoir interviewés les responsables de traitements, vous identifiez vos premiers traitements ci-dessous :

| \# | Département | Traitement de données personnelles | Support / application | DPIA requis a priori ? |
| :--- | :--- | :--- | :--- | :--- |
| 1 | RH | Gestion du recrutement | Linkedin \(externe\) | Non |
| 2 | RH | Gestion de la paie | Payfit \(externe\) | Non |
| 3 | RH | Gestion du personnel | Microsoft Office | Non |
| 4 | Secrétariat Général | Gestion des données du Comité d'Entreprise | Application interne | Non |
| 5 | Production | Gestion de la qualité | Microsoft Office | Non |
| 6 | Marketing & Ventes | Gestion des clients | Salesforce \(externe\) | Non |
| 7 | Marketing & Ventes | Envoi d'emails promotionnels  | Mailjet \(externe\) | Non |
| 8 | Marketing & Ventes | Profilage de prospects | Salesforce | Oui |
| 9 | Sécurité | Gestion des entrées / sorties des bâtiments | IBM | Oui |
| 10 | Sécurité | Contrôle d'antériorité | Microsoft Office | Non |
| 11 | Informatique | Développement d'application | Microsoft Azure \(externe\) | Non |
| 12 | Informatique | Maintenance d'application | CGI \(externe\) | Non |
| 13 | Juridique  | Gestion des contrats | Microsoft Office | Non |
| 14 | Achats | Gestion des fournisseurs | SAP \(externe\) | Non |

Conscient de l'importance d'une bonne cartographie et disposant de peu de temps pour ce faire, vous choisissez Dastra comme solution pour vous faciliter le travail d'achèvement du registre. 

Pour faire cela, vous commencez un projet sur Dastra :

{% page-ref page="commencer-un-projet-sur-dastra.md" %}

Puis, vous compléter votre registre dans Dastra :

{% page-ref page="../fonctionalites/editer-le-registre/gerer-votre-registre.md" %}

_Cf. ci-dessous un exemple de registre respectant le format demandé disponible au téléchargement et pouvant être importé en "glisser-déposer" dans Dastra :_

{% file src="../.gitbook/assets/sample-datatreatments-shipbuilder.xlsx" %}

{% hint style="info" %}
Les informations du registre de traitement ne peuvent pas toutes être importées dans DASTRA à partir d'un fichier. Pour **compléter le registre à 100%**, il vous suffit d'éditer chacun des traitements et renseigner les informations manquantes.
{% endhint %}

Vous remplissez ensuite toutes les informations nécessaires à un traitement.

{% page-ref page="../fonctionalites/editer-le-registre/gerer-votre-traitement.md" %}

Vous partagez le registre avec l'ensemble des responsables de traitement ainsi que votre réseau de correspondants RGPD et demandez validation de toutes les parties prenantes. 

{% page-ref page="../fonctionalites/editer-le-registre/partager-le-registre.md" %}

Ca y est, **votre registre est constitué** et vos traitements sont prêts à être protégés !

Pour en savoir plus sur comment éditer votre registre :

{% page-ref page="../fonctionalites/editer-le-registre/" %}

## Etape 3 : Prioriser les actions à mener

Une fois le registre constitué et sur la base de celui-ci, vous vous attelez à [lister l'ensemble des tâches à réaliser](https://www.cnil.fr/fr/prioriser-les-actions-mener) pour vous conformer aux obligations actuelles et à venir du Règlement Général de la Protection des Données \(RGPD\). Puis, vous priorisez ces actions au regard des risques que font peser vos traitements sur les droits et les libertés des personnes concernées.

{% hint style="info" %}
Vous ne savez pas par quelles actions commencez ? Consultez le [guide de la sécurité des données personnelles](https://www.cnil.fr/fr/principes-cles/guide-de-la-securite-des-donnees-personnelles) édité par la CNIL qui constitue un bon point de départ.
{% endhint %}

Une fois les actions nécessaires pour réaliser votre projet de mise en conformité identifiées, vous créez les tâches associées et les allouez aux collaborateurs associés directement dans l'onglet "Planification" de l'outil Dastra :

![Exemple de plan d&apos;action](../.gitbook/assets/image%20%2865%29.png)

Pour en savoir plus sur la fonctionnalité "Planification" de Dastra :

{% page-ref page="../fonctionalites/planifier/" %}

## Etape 4 : Gérer les risques

Si vous avez identifié des traitements de données personnelles susceptibles d'engendrer des risques élevés pour les droits et libertés des personnes concernées, vous devrez mener, pour chacun de ces traitements, une [analyse d'impact relative à la protection des données ](https://www.cnil.fr/fr/gerer-les-risques)\(AIPD\).

{% hint style="info" %}
Mener une AIPD est obligatoire pour tout traitement susceptible d'engendrer des risques élevés pour les droits et libertés des personnes concernées \(Article 35 du RGPD\)
{% endhint %}

Pour vous aider à déterminer si votre traitement est susceptible d’engendrer des risques élevés, les 9 critères suivants sont définis dans les lignes directrices du G29 :

1. Evaluation ou notation;
2. Décision automatisée avec effet juridique ou effet similaire significatif;
3. Surveillance systématique ;
4. Données sensibles ou données à caractère hautement personnel ;
5. Données personnelles traitées à grande échelle ;
6. Croisement d’ensembles de données ;
7. Données concernant des personnes vulnérables ;
8. Usage innovant ou application de nouvelles solutions technologiques ou organisationnelles ;
9. Exclusion du bénéfice d’un droit, d’un service ou contrat.

Ces critères sont directement intégrés à notre workflow de création de traitement de données, et vous pouvez renseigner pour chacun de vos traitements s'il y a eu de réaliser un PIA sur celui-ci ou non.

![Exemple de traitement n&#xE9;cessitant potentiellement un PIA.](../.gitbook/assets/image%20%2893%29.png)

## Etape 5 :  Organiser les processus internes

Pour assurer un haut niveau de protection des données personnelles en permanence, vous devez [mettre en place des procédures internes](https://www.cnil.fr/fr/organiser-les-processus-internes) qui garantissent la prise en compte de la protection des données à tout moment, en prenant en compte l’ensemble des événements qui peuvent survenir au cours de la vie d’un traitement \(ex : faille de sécurité, gestion des demande de rectification ou d’accès, modification des données collectées, changement de prestataire\).

Dastra vous permets de digitaliser et d'automatiser au moins partiellement les processus internes ci-dessous:

* **La gestion des demandes d'exercice de droits :**

{% page-ref page="../fonctionalites/gerer-les-exercices-des-droits/" %}

* **La gestion du consentement aux cookies :**

{% page-ref page="../fonctionalites/gerer-le-consentement-aux-cookies/" %}

* **La gestion des notifications de violation de données :**

{% page-ref page="../fonctionalites/notifier-les-violations-de-donnees/" %}

* La gestion des contrats :

{% page-ref page="../fonctionalites/generer-des-clauses-contractuelles.md" %}

## Etape 6 : Documenter la conformité

Pour prouver votre conformité au règlement, vous devez[ constituer et regrouper la documentation nécessaire](https://www.cnil.fr/fr/documenter-la-conformite). Les actions et documents réalisés à chaque étape doivent être réexaminés et actualisés régulièrement pour assurer une protection des données en continu. 

#### Votre dossier devra notamment comporter les éléments suivants :

| Catégorie |  Documentation |
| :--- | :--- |
| LA DOCUMENTATION SUR VOS TRAITEMENTS DE DONNÉES PERSONNELLES |  [**Le registre des traitements**](https://www.cnil.fr/fr/RGDP-le-registre-des-activites-de-traitement) \(pour les responsables de traitements\)  ou des catégories d’activités de traitements \(pour les sous-traitants\) |
| LA DOCUMENTATION SUR VOS TRAITEMENTS DE DONNÉES PERSONNELLES |  [**Les analyses d’impact relatives à la protection des données**](https://www.cnil.fr/fr/RGPD-analyse-impact-protection-des-donnees-aipd) \(AIPD\) pour les traitements susceptibles d'engendrer des risques élevés pour les droits et libertés des personnes |
| LA DOCUMENTATION SUR VOS TRAITEMENTS DE DONNÉES PERSONNELLES |  [**L'encadrement des transferts**](https://www.cnil.fr/fr/transferts-de-donnees-hors-ue-ce-qui-change-avec-le-reglement-general-sur-la-protection-des-donnees) de données hors de l'Union européenne \(notamment, les clauses contractuelles types, les BCR et certifications\) |
| L'INFORMATION DES PERSONNES |  [**Les mentions d’information**](https://www.cnil.fr/fr/conformite-rgpd-information-des-personnes-et-transparence) |
| L'INFORMATION DES PERSONNES |  ​Les modèles de **recueil du consentement des personnes concernées**, |
| L'INFORMATION DES PERSONNES |  Les procédures mises en place pour **l'exercice des droits** |
| LES CONTRATS QUI DEFINISSENT LES RÔLES ET RESPONSABILITES DES ACTEURS |  [**Les contrats avec les sous-traitants**](https://www.cnil.fr/fr/sous-traitance-exemple-de-clauses) |
| LES CONTRATS QUI DEFINISSENT LES RÔLES ET RESPONSABILITES DES ACTEURS |  [Les procédures internes **en cas de violations de données**](https://www.cnil.fr/fr/les-violations-de-donnees-personnelles) |
| LES CONTRATS QUI DEFINISSENT LES RÔLES ET RESPONSABILITES DES ACTEURS |  Les preuves que les personnes concernées **ont donné leur consentement** lorsque le traitement de leurs données repose sur cette base. |

Si votre documentation démontre que vous respectez les obligations prévues par le règlement européen, alors vous aurez franchi cette étape. Bravo !











