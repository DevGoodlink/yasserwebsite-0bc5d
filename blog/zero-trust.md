---
title: Zero Trust architecture
subtitle: lorem-ipsum
date: '2021-09-14'
excerpt: lorem-ipsum
image_alt: lorem-ipsum
thumb_image_alt: lorem-ipsum
seo:
  title: ''
  description: ''
  robots: []
  extra: []
layout: post
---
## L’approche Zero Trust, de quoi parle-t-on concrètement ?



Le Zero Trust est un modèle stratégique de cybersécurité qui part du principe qu’il n’existe aucune zone de confiance lorsqu’il s’agit de protéger le système d’information et les données de l’entreprise.

Il vient se substituer au modèle traditionnel de sécurité, qui considère le système d’information de l’entreprise comme un périmètre de confiance à protéger contre les menaces extérieures, en positionnant des points de vérification (Firewall, DMZ, ACL…).

Soulignons tout de même que le concept n’est pas nouveau. Ses origines remontent au début des années 2000 où le [Jericho Forum](https://whatis.techtarget.com/definition/Jericho-Forum), un groupe de travail international consacré à la sécurité, formulait déjà les bases d’une nouvelle architecture de sécurité pour sortir de la vision « périmétrique » qui régnait alors en maître. C’est en 2010 que le cabinet d’analystes [Forrester Research](https://go.forrester.com/) introduit pour la première fois le terme « **Zero Trust** ».

Ci-dessous quelques acronymes sur le sujet :

*   **ZTA :** acronyme anglais de Zero Trust Architecture

*   **ZTNA :** acronyme anglais de Zero Trust Network Access. Expression plus récente utilisée par les principaux analystes IT du marché.

*   **ZT :** acronyme anglais de Zero Trust

## **Mais alors, pourquoi ce modèle ressurgit-il aujourd’hui de plus en plus dans les feuilles de route cybersécurité des RSSI ?**

Tout simplement parce qu’il est désormais impensable pour une organisation de fermer complètement son système d’information ! Les utilisateurs de celui-ci sont de plus en plus nombreux (collaborateurs, clients, partenaires, prestataires, fournisseurs, investisseurs…) et leurs usages sont variés (télétravail, nomadisme, ressources partagées…). Le système d’information a évolué et est désormais décentralisé et distribué au-delà du réseau local de l’organisation (Cloud, SaaS, …). Tout cela contribue à repousser les frontières du SI telles qu’on les a connues par le passé.

**Cependant, l’**[ouverture du SI](https://www.ilex-international.com/fr/strategie-iam/ouverture-si) **se fait dans un contexte plus qu’hostile** : on fait face à une véritable explosion des cyberattaques en France. Guillaume Poupard, directeur général de l’ANSSI, déclarait en début d’année que les interventions de l’ANSSI auprès d’organisations victimes des ransomwares avaient été multipliées par quatre en 2020\* par rapport à l’année précédente !

*\*Source :* [*https://www.lefigaro.fr/flash-eco/les-attaques-informatiques-criminelles-ont-explose-l-an-dernier-20210111*](https://www.lefigaro.fr/flash-eco/les-attaques-informatiques-criminelles-ont-explose-l-an-dernier-20210111)

Cette augmentation inquiétante d’incidents de sécurité et de fuites de données a complètement anéanti le concept de confiance. Aujourd’hui, la menace existe aussi bien en interne qu’en externe et il faut impérativement repenser le modèle de sécurité pour gagner en sérénité et en agilité.

**Les RSSI l’ont bien compris et sont de plus en plus nombreux à se tourner vers des approches Zero Trust Network Access (ZTNA).** La [dernière édition du baromètre annuel](https://www.cesin.fr/fonds-documentaire-6eme-edition-du-barometre-annuel-du-cesin.html) du CESIN confirme bien la nette progression du concept Zero Trust avec 29% des entreprises réellement engagées ou en passe de mettre en œuvre ce concept, contre 16% l’année dernière.

## Quels sont les principes fondamentaux d’une architecture Zero Trust (ZTA) ?

Afin d’éviter que le terme Zero Trust devienne une expression « fourre-tout », l’institut national des standards et de la technologie ([NIST](https://www.nist.gov/)), une division du département du commerce des États-Unis, a publié en août dernier la spécification « [800-207 Zero TRUST Architecture](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-207.pdf) », que je vous recommande fortement de lire pour approfondir le sujet.

Dans cette publication, le NIST définit 7 principes sur lesquels repose une architecture Zero Trust (ZTA) :

**1 – Toutes les données, les services réseaux et les équipements sont considérés comme des ressources**.

*On entend donc par ressources les utilisateurs, les procédures, les éléments matériels, logiciels, annuaires et les données. Ainsi, une application de gestion des ressources humaines, une base de données de prospects, un serveur de fichiers ou un équipement d’impression sont autant d’exemples de ressources dont l’accès et les actions doivent être systématiquement contrôlés et supervisés*

**2 – Toutes les communications sont sécurisées indépendamment de l’emplacement du réseau.**

*En bref, l’usage de certificat et le chiffrement des communications réseau deviennent de facto la norme, que les utilisateurs se connectent depuis le réseau local ou depuis l’extérieur. Pensez à renouveler régulièrement vos certificats et clés de chiffrement !*

**3 – Chaque tentative d’accès à une ressource est vérifiée et évaluée conformément à la politique de sécurité définie par l’organisation.**

*Cela signifie qu’il est impératif de mettre en place une authentification et un contrôle d’accès systématique basés sur les habilitations préalablement définies. Rappelons que dans le cadre d’une architecture Zero Trust, il convient d’adopter le principe du moindre privilège. Un utilisateur doit disposer uniquement des droits nécessaires à sa fonction, ni plus ni moins.
Certaines composantes de l’IAM (Identity and Access Management) peuvent être mises en place afin de concilier sécurité et ergonomie pour vos utilisateurs finaux. C’est notamment le cas de la *[*fédération d’identité*](https://www.ilex-international.com/fr/strategie-iam/federation-identite)* qui permet de déléguer la gestion de l’authentification et de l’autorisation à une partie tierce dédiée dite IDP. Pour aller plus loin techniquement, n’hésitez pas à consulter notre billet blog sur les protocoles *[*Oauth2 et OpenId Connect*](https://www.ilex-international.com/fr/federation-identite/oauth2-vs-openid-connect)*.*

**4 – L’accès à une ressource est soumis à une politique d’accès dynamique tenant compte de :**

*   L’identité du client, du service ou de l’application requérante

*   L’état du service demandant l’accès (versions installées, localisation du réseau, date de la requête, comportements précédents, certificats…)

*   Les attributs comportementaux (analyse de l’équipement, écart constaté par rapport l’usage courant enregistré…)

*   Les attributs d’environnement (localisation réseau, le temps, les attaques enregistrées…)

*Le ZTNA (Zero Trust Network Access) implique donc la mise en place de mécanismes d’authentification adaptative afin d’adapter le niveau de sécurité nécessaire pour accéder à chaque ressource du système d’information en fonction du contexte dans lequel se trouve l’utilisateur. Concrètement, un utilisateur qui tenterait par exemple d’accéder à une ressource avec une version compromise de son navigateur ou de son système d’exploitation pourra se voir refuser l’accès dynamiquement jusqu’à l’installation des correctifs nécessaires sur sa machine afin d’éviter de faire courir le moindre risque de *[*sécurité sur le système d’information*](https://www.ilex-international.com/fr/strategie-iam/securite)*.*

**5 – L’organisation met en place un système de surveillance en temps réel, visant à contrôler le bon fonctionnement du système d’information et à remonter toutes anomalies ou interruptions qui lui feraient courir un risque de sécurité élevé.**

*Là encore, il n’existe aucune confiance par défaut, l’intégralité des composants du réseau doit être surveillée afin de détecter rapidement tout comportement suspect ou anormal.
Pour répondre à ce principe, il est possible de coupler un Security Operations Center (SOC) à un Security Information Event Management (SIEM) selon les besoins de l’organisation.*

**6 – Les mécanismes d’authentification et d’autorisation sont dynamiques et peuvent être renforcés avant qu’un accès soit accordé.**

*Prenons l’exemple de certains collaborateurs qui, dans le cadre de leurs fonctions, peuvent avoir des droits étendus sur certaines applications sensibles. Si ces derniers se connectent en dehors des horaires de travail de leur organisation, on pourra alors renforcer le niveau de sécurité en leur demandant une *[*authentification multifacteur (MFA)*](https://www.ilex-international.com/fr/strategie-iam/authentification-forte-mfa)* afin de protéger le système d’information d’une éventuelle usurpation d’identité.*

**7 – L’entreprise assure une supervision constante de la sécurité en collectant le maximum d’informations possibles sur l’état actuel des ressources, l’infrastructure réseau et les communications en cours sur celui-ci.**

*La traçabilité et l’exploitation continue des informations collectées ont pour objectif l’amélioration constante de la sécurité du système d’information.*
