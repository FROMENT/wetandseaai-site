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

La gestion des identités et des accès (IAM) constitue un pilier fondamental de la posture de sécurité organisationnelle. Cette vidéo articule les risques concrets liés aux comptes orphelins—comptes actifs appartenant à d'anciens employés—et décrit les mécanismes de contrôle d'accès basé sur les rôles (RBAC) et les attributs (ABAC). Le cycle de vie des identités numériques, du provisioning à la suppression, détermine directement la surface d'exposition aux compromissions. Les frameworks d'automatisation comme Joiner-Mover-Leaver (JML) réduisent les délais de déprovisioning et l'escalade de privilèges, tandis que les principes du moindre privilège et de la séparation des tâches encadrent l'architecture des droits d'accès. Comprendre ces éléments s'avère critique pour les responsables de la sécurité et les auditeurs internes.

## Principaux points abordés

- **Comptes orphelins et escalade de privilèges** — Les comptes d'utilisateurs non supprimés après un départ conservent potentiellement des droits étendus accumulés au fil du temps. Cette situation crée des vecteurs d'attaque directes exploitables sans modification des configurations de sécurité.

- **Cycle de vie des identités numériques** — Chaque identité traverse quatre phases : création (jointure), modification (mobilité interne), gestion courante (accès différencié) et suppression (départ). Les ruptures dans ce cycle amplifient les risques de non-conformité réglementaire et de fuite d'accès.

- **Distinction authentification / autorisation** — L'authentification établit l'identité de l'utilisateur (qui êtes-vous), tandis que l'autorisation définit les ressources accessibles (quels droits). Ces mécanismes relèvent de domaines distincts et nécessitent des approches techniques séparées.

- **RBAC versus ABAC** — RBAC (Role-Based Access Control) attribue les droits par rôle préaffecté ; ABAC (Attribute-Based Access Control) évalue dynamiquement les attributs utilisateur, contextuels et informationnels pour chaque demande d'accès. ABAC offre une granularité supérieure mais complexifie la gouvernance.

- **Provisioning automatisé et framework JML** — L'automatisation du provisioning via des règles Joiner-Mover-Leaver réduit les délais de déploiement des droits et accélère le déprovisioning lors des transitions d'emploi, diminuant ainsi les fenêtres d'exposition.

- **Principes du moindre privilège et séparation des tâches** — Chaque utilisateur reçoit le minimum de droits requis pour exercer sa fonction ; la séparation des tâches empêche une même personne de détenir des permissions contradictoires (validation et approbation, par exemple).

- **Limite opérationnelle : scalabilité ABAC** — Bien que plus fin, ABAC nécessite une maintenance d'attributs rigoureuse et peut générer une surcharge décisionnelle en environnement cloud hyperscalaire ; RBAC reste plus simple à gérer dans les organisations de taille modérée.

- **Impact gouvernance et audit** — La traçabilité des cycles de vie et l'audit des droits d'accès deviennent obligatoires pour la conformité réglementaire (RGPD, SOC 2, ISO 27001). Les plateformes IAM/IGA centralisées facilitent cette démonstration de conformité.

## Références (Golden Sources)

- [ABAC vs. RBAC: What's The Difference?](https://www.wiz.io/academy/cloud-security/abac-vs-rbac)
- [Complete Guide to Identity Governance and Administration (IGA) - Opti](https://www.opti.ai/articles/complete-guide-to-identity-governance-and-administration)
- [A Defender's Guide to Privileged Account Monitoring | Google Cloud Blog](https://cloud.google.com/blog/topics/threat-intelligence/privileged-account-monitoring)
- [CIEM vs. IAM: How Do They Compare? | Wiz](https://www.wiz.io/academy/cloud-security/ciem-vs-iam)
- [Federated Identity Governance & Zero Trust Identity and Access - Sequretek](https://www.sequretek.com/products/identity-and-access-governance)
- [How to Detect Lateral Movement Before Attackers Reach Critical Assets - Daylight](https://daylight.ai/blog/lateral-movement-detection)
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
