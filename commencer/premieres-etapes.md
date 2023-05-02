---
description: Learn how to use Dastra step by step through a concrete example.
---

# First steps

## Use case (fictional): The SHIPBUILDER company

You are the business manager of SHIPBUILDER, an organization that builds boats. It is made up of 8 departments:

* HR
* General Secretary
* Delivery
* Sales & Marketing
* Security
* IT
* Law
* Procurement

You have decided to bring your company into compliance with the General Data Protection Regulations (GDPR). After learning what GDPR is, you start without further delay.

## Step 1: Designate a Data Protection Officer (DPO)

First, you learned about the role of the DPO and the conditions to be met to appoint a DPO, then you decided to designate a DPO in order to reduce the risk of litigation. Your choice is made by a collaborator who, in turn, defines and coordinates a network of GDPR correspondents within the various businesses of the company.

{% hint style="info" %}
The designation of a Data Protection Officer is **mandatory** only for:

* Public bodies ;
* Companies whose basic activity leads them to carry out regular and systematic monitoring of people on a large scale, or to process large-scale data known as "sensitive" or relating to criminal convictions and offenses.
{% endhint %}

## Step 2 :Map your personal data processing and establish the record of processing

After having trained in the mapping of treatments and having interviewed the treatment managers, you identify your first data processing activities below:

| #  | Department        | Data processing activities        | Support / application      | Is a DPIA required a priori ? |
| -- | ----------------- | --------------------------------- | -------------------------- | ----------------------------- |
| 1  | HR                | Hiring                            | Linkedin (external)        | No                            |
| 2  | HR                | Payroll management                | Payfit (external)          | No                            |
| 3  | HR                | Staff management                  | Microsoft Office           | No                            |
| 4  | General Secretary | Company council data management   | Internal application       | No                            |
| 5  | Delivery          | Quality management                | Microsoft Office           | No                            |
| 6  | Sales & Marketing | Client management                 | Salesforce (external)      | No                            |
| 7  | Sales & Marketing | Sending promotional emails        | Mailjet (external)         | No                            |
| 8  | Sales & Marketing | Prospects profiling               | Salesforce                 | Yes                           |
| 9  | Security          | Entry / exit building management  | IBM                        | Yes                           |
| 10 | Security          | Background check                  | Microsoft Office           | No                            |
| 11 | IT                | Application development           | Microsoft Azure (external) | No                            |
| 12 | IT                | Application maintenance & support | CGI (external)             | No                            |
| 13 | Law               | Contract management               | Microsoft Office           | No                            |
| 14 | Procurement       | Provider management               | SAP (external)             | No                            |

Aware of the importance of good mapping and having little time to do so, you choose Dastra as a solution to facilitate the work of completing the registry.

To do this, you start a project on Dastra:

{% content-ref url="commencer-un-projet-sur-dastra.md" %}
[commencer-un-projet-sur-dastra.md](commencer-un-projet-sur-dastra.md)
{% endcontent-ref %}

Then, complete your register in Dastra:

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

See below an example of a record of processing activities respecting the requested format available for download and which can be imported by "drag and drop" in Dastra:

{% file src="../.gitbook/assets/sample-datatreatments-shipbuilder.xlsx" %}

{% hint style="info" %}
Not all information in the record of processing can be imported into DASTRA from a single file. **To complete 100% of the the record**, simply edit each of the treatments and fill in the missing information.
{% endhint %}

You then fill in all the information necessary for processing.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

You share the register with all of the data controllers and your network of GDPR correspondents and request validation from all stakeholders.

{% content-ref url="../features/editer-le-registre/partager-le-registre.md" %}
[partager-le-registre.md](../features/editer-le-registre/partager-le-registre.md)
{% endcontent-ref %}

That's it, **your record of processing actitivities is made** and your processing activities are ready to be protected!

To find out more about how to edit your registry:

{% content-ref url="../features/editer-le-registre/" %}
[editer-le-registre](../features/editer-le-registre/)
{% endcontent-ref %}

## Step 3 : Prioritize actions to be taken

Once the record has been established and on the basis of it, you set out to list all the tasks to be carried out to comply with the current and future obligations of the General Data Protection Regulation (GDPR). Then, you prioritize these actions with regard to the risks that your processing poses for the rights and freedoms of the persons concerned.

{% hint style="info" %}
You don't know how to start? Feel free to consult the [**Guide to Data Protection**](https://ico.org.uk/for-organisations/guide-to-data-protection/) of the ICO.
{% endhint %}

Once the actions necessary to carry out your compliance project have been identified, you create the associated tasks and allocate them to the associated employees directly in the "Planning" tab of the Dastra tool:

![Action plan example](<../.gitbook/assets/image (65).png>)

To find out more about the Dastra "Planning" functionality:

{% content-ref url="../features/planifier/" %}
[planifier](../features/planifier/)
{% endcontent-ref %}

## Step 4 : Manage the risks

If you have identified processing of personal data likely to generate high risks for the rights and freedoms of the data subjects, you will have to conduct, for each of these processing, a data protection impact assessment (AIPD).

{% hint style="info" %}
Conducting an AIPD is compulsory for any processing likely to generate high risks for the rights and freedoms of the data subjects (Article 35 of the GDPR)
{% endhint %}

To help you determine if your processing activity is likely to create high risks, the following 9 criteria are defined in the G29 guidelines:

1. Assessment or grading;&#x20;
2. Automated decision with significant legal or similar effect;&#x20;
3. Systematic monitoring;&#x20;
4. Sensitive data or highly personal data;&#x20;
5. Personal data processed on a large scale;&#x20;
6. Crossing of data sets;&#x20;
7. Data concerning vulnerable people;&#x20;
8. Innovative use or application of new technological or organizational solutions;&#x20;
9. Exclusion of the benefit of a right, service or contract.

These criteria are directly integrated into our data processing creation workflow, and you can provide information for each of your treatments if there has been a PIA on it or not.

![.](<../.gitbook/assets/image (93).png>)

## Step 5 :  Organize internal processes

To ensure a high level of protection of personal data at all times, you must put in place internal procedures which guarantee that data protection is taken into account at all times, taking into account all the events that may occur during of the life of a processing (ex: security breach, management of requests for rectification or access, modification of the data collected, change of provider).

&#x20;Dastra allows you to digitize and at least partially automate the internal processes below:

* **Managing requests to exercise rights:**

{% content-ref url="../features/gerer-les-exercices-des-droits/" %}
[gerer-les-exercices-des-droits](../features/gerer-les-exercices-des-droits/)
{% endcontent-ref %}

* **Managing consent to cookies:**

{% content-ref url="../features/gerer-le-consentement-aux-cookies/" %}
[gerer-le-consentement-aux-cookies](../features/gerer-le-consentement-aux-cookies/)
{% endcontent-ref %}

* **Managing data breach notifications:**

{% content-ref url="../features/notifier-les-violations-de-donnees/" %}
[notifier-les-violations-de-donnees](../features/notifier-les-violations-de-donnees/)
{% endcontent-ref %}

## Step 6: Document compliance

To prove your compliance with the regulations, you must establish and gather the necessary documentation. The actions and documents carried out at each stage must be reviewed and updated regularly to ensure continuous data protection.

**Your file must include the following elements:**

| Category                                                               |  Documentation                                                                                                                                |
| ---------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| DOCUMENTATION ON YOUR PERSONAL DATA PROCESSING                         | The **record of processing** (for data controllers) or categories of processing activities (for data processors)                              |
| DOCUMENTATION ON YOUR PERSONAL DATA PROCESSING                         | **Data protection impact analysis** (AIPD) for processing operations likely to generate high risks for the rights and freedoms of individuals |
| DOCUMENTATION ON YOUR PERSONAL DATA PROCESSING                         | **Supervision of data transfers outside the European Union** (in particular, standard contractual clauses, BCRs and certifications)           |
| INFORMATION OF PEOPLE                                                  | **Information notices**                                                                                                                       |
| INFORMATION OF PEOPLE                                                  | Models for **obtaining the consent of the persons concerned**                                                                                 |
| INFORMATION OF PEOPLE                                                  | The procedures put in place for the **exercise of rights**                                                                                    |
| THE CONTRACTS THAT DEFINE THE ROLES AND RESPONSIBILITIES OF THE ACTORS | **Contracts with subcontractors**                                                                                                             |
| THE CONTRACTS THAT DEFINE THE ROLES AND RESPONSIBILITIES OF THE ACTORS |  nternal procedures **in the event of data breaches**                                                                                         |
| THE CONTRACTS THAT DEFINE THE ROLES AND RESPONSIBILITIES OF THE ACTORS |  Evidence that the data subjects have **given their consent** when the processing of their data is based on this basis.                       |

If your documentation shows that you comply with the obligations provided for by European regulations, then you will have completed this step. Well done !









