---
title: "Comptes orphelins, RBAC, ABAC : les bases de l'IAM à maîtriser"
date: 2026-05-22
slug: "gestion-identités-accès-guide-iam/iga-pour-leaders-tech"
youtube_url: "https://youtu.be/_Dk6aVFX8U8"
youtube_video_id: "_Dk6aVFX8U8"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "cybersecurity"
categories: ["Cybersécurité"]
tags: ["cybersecurity", "IAM", "IGA", "cybersécurité", "identitésnumériques", "sécuritéIT"]
summary: "Un ancien salarié dont le compte est toujours actif : c'est la faille IAM la plus banale… et la plus dangereuse. Cycle de vie des identités, RBAC, ABAC et moindre privilège."
cover:
  image: "/covers/_Dk6aVFX8U8.jpg"
  alt: "Comptes orphelins, RBAC, ABAC : les bases de l'IAM à maîtriser"
  caption: "Cybersécurité"
draft: false
catalogue_id: "d0237fc5"
translationKey: "d0237fc5"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/_Dk6aVFX8U8" title="Voir la vidéo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

La gestion des identités et des accès (IAM) constitue un pilier fondamental de la sécurité informatique d'entreprise, souvent négligé au profit de solutions perceptrales. Les comptes orphelins — identités numériques toujours actives après le départ d'un collaborateur — incarnent une exposition majeure, particulièrement lorsqu'aucun processus de révocation n'existe. Au-delà de cette vulnérabilité, les organisations doivent maîtriser le cycle de vie complet des identités (création, évolution, suppression), distinguer authentification et autorisation, et implémenter des modèles de contrôle d'accès adaptés à leur architecture. L'escalade de privilèges, l'accumulation progressive de droits non justifiés, et la violation du principe du moindre privilège figurent parmi les vecteurs d'exploitation les plus courants en réponse à incident. Les approches RBAC et ABAC, fondamentalement différentes, répondent à des contextes d'infrastructure et de gouvernance distincts.

## Principaux points abordés

- **Comptes orphelins et escalade de privilèges** — Une identité non révoquée demeure accessible longtemps après la fin de la relation emploi ou partenaire, créant une porte d'entrée persistante. L'escalade intervient lorsque des permissions s'accumulent sans audit régulier, transformant un compte standard en vecteur de mouvement latéral.

- **Cycle de vie des identités numériques** — Suivant le modèle Joiner-Mover-Leaver, chaque identité traverse des états distincts : création à l'onboarding, modifications lors de changements de rôle ou équipe, révocation à la résiliation. L'absence d'orchestration de ces transitions expose l'organisation à des droits résiduels et à des incohérences de gouvernance.

- **Distinction authentification / autorisation** — L'authentification valide l'identité (« êtes-vous bien qui vous prétendez être ? ») via MFA ou SSO. L'autorisation définit les ressources accessibles après authentification. Confondre ces deux niveaux compromet la sécurité du contrôle d'accès.

- **RBAC (Role-Based Access Control)** — Modèle d'autorisation structuré par rôles prédéfinis auxquels sont attachées des permissions. Scalable dans les environnements classiques, il offre une granularité insuffisante en environnement cloud multi-tenant ou avec ressources hétérogènes. Son rigidité limite l'adaptabilité à des politiques contextuelles.

- **ABAC (Attribute-Based Access Control)** — Approche décisionnelle fondée sur les attributs (utilisateur, ressource, contexte, action). Permet une granularité fine mais introduit une complexité opérationnelle accrue : gestion des attributs, moteurs de politiques, coûts de déploiement et maintenance supérieurs. Mieux adapté aux architectures cloud et aux besoins dynamiques.

- **Moindre privilège et séparation des tâches** — Principes de gouvernance exigeant que chaque compte dispose uniquement des permissions minimales pour exercer ses fonctions, et que les tâches sensibles soient réparties entre plusieurs identités. L'audit régulier des droits (access review) constitue le mécanisme de conformité à ces principes.

- **Provisioning automatisé** — Intégration des systèmes d'information RH, annuaires et plateformes IAM pour générer, modifier et révoquer les accès sans intervention manuelle. Réduit les délais d'erreur humaine mais exige une synchronisation des données fiable et un contrôle des règles de business.

- **Limite opérationnelle : complexité vs. sécurité** — L'ABAC offre une sécurité fine-grained au prix d'une complexité de gestion élevée ; les petites structures manquent souvent de ressources pour exploiter cette granularité. Le RBAC reste plus simple à opérer mais moins adaptable aux contextes volatiles. Le choix dépend de la maturité, de la taille et de l'architecture cible, non d'une supériorité absolue.

- **Impact gouvernance et compliance** — Un IAM mal conçu expose l'organisation à des risques de conformité réglementaire (RGPD, NIS2, SOC2), d'audit de contrôle d'accès échoués, et d'incidents de sécurité amplifiés par un contexte de privilèges excessifs ou périmés.

## Références (Golden Sources)

- [ABAC vs. RBAC: What's The Difference? - Wiz](https://www.wiz.io/academy/cloud-security/
## Chapitres

- `0:00` — Introduction
- `0:33` — Comptes orphelins et risques
- `1:06` — Identité numérique et cycle
- `1:40` — Authentification vs autorisation
- `2:20` — Provisioning et automatisation
- `2:54` — Moindre privilège et SoD

## Ressources Wet & Sea Tech

**Chaîne YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Boutique :** https://wetseatech.etsy.com

**Tous les articles Cybersécurité :** https://wst-tech.org/tags/cybersecurity/
