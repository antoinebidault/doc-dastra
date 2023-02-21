---
description: Learn how to set up a cookie consent widget on your site.
---

# Implement a cookie consent widget

DASTRA allows you to set up a cookie consent widget directly on your site in compliance with the recommendations of the CNIL (French Data Protection Authority) on cookies and other tracking devices.

## What is the Dastra cookie consent widget?

This widget is composed of several elements

<figure><img src="https://138894690-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LvBxs22wUMicv9uWp6C-2584506019%2Fuploads%2F6C7JDBYbJydNYzQ8vGjp%2FCapture%20web_6-5-2022_93427_www.dastra.eu.jpeg?alt=media&#x26;token=bab7e0b0-450a-4ff4-8117-91e121d03c94" alt=""><figcaption><p>A "cookies" symbol appearing at the bottom left of the screen</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Capture d’écran 2023-02-21 à 15.11.52.png" alt=""><figcaption><p>A fold-out introduction window</p></figcaption></figure>

## Prerequisites&#x20;

To implement your cookie consent widget, you must first **identify** and **classify** the cookies **placed on your website by purpose**. DASTRA's Cookie Consent module allows you to do this in just a few clicks.

{% hint style="info" %}
To make the implementation of the cookie consent widget easier, Dastra has integrated all the necessary steps, from setting up the prerequisites to the lines of code, in the same module.
{% endhint %}

To scan the cookies placed on your website, go to the following page:

{% content-ref url="scannez-les-cookies-deposes-sur-votre-site-web.md" %}
[scannez-les-cookies-deposes-sur-votre-site-web.md](scannez-les-cookies-deposes-sur-votre-site-web.md)
{% endcontent-ref %}

To classify cookies by consent categories, go to the following page:

{% content-ref url="classifiez-les-cookies-par-categories-de-consentement.md" %}
[classifiez-les-cookies-par-categories-de-consentement.md](classifiez-les-cookies-par-categories-de-consentement.md)
{% endcontent-ref %}

## Set the appearance of your target cookie consent widget

To set up a cookie consent widget on your website, you must go to the "Appearance" interface of the DASTRA cookie consent module.

<figure><img src="../../../.gitbook/assets/Capture d’écran 2023-02-21 à 15.18.41 (1).png" alt=""><figcaption><p>DASTRA Cookie Consent Module "Templating" Interface</p></figcaption></figure>

From this interface, you can **fully customize your widget** so that it displays the way you want it to on your website.

{% hint style="info" %}
You can also make other more general changes to the widget in the "Configuration", "Texts and translations" and "Triggers" sections.
{% endhint %}

Once the settings are complete, click on "Save and continue".

![](<../../../.gitbook/assets/image (120).png>)

## Insérez le code du widget sur votre site web

Une fois votre widget de consentement aux cookies cible défini, vous pouvez l'intégrer directement sur votre site web grâce aux l**ignes de code générées automatiquement** par DASTRA.\
\
Pour cela, rendez-vous dans l'interface "Code" du module Consentement aux cookies de DASTRA, et insérez le code généré automatiquement avant la fin de la balise html \<body> de votre site internet.

![Génération de code html du widget](<../../../.gitbook/assets/image (140).png>)

{% hint style="info" %}
Vous pouvez utiliser le Google tag manager pour insérer dynamiquement ce code sur chaque page.
{% endhint %}



