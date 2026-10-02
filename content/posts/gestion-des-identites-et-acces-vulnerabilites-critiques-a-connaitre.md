---
title: "IAM : pourquoi VPN et pare-feu sont devenus des cibles prioritaires"
date: 2026-05-27
slug: "gestion-des-identités-et-accès-vulnérabilités-critiques-à-connaître"
youtube_url: "https://youtu.be/_ipXrAM-cIg"
youtube_video_id: "_ipXrAM-cIg"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "cybersecurity"
categories: ["Cybersécurité"]
tags: ["cybersecurity", "CybersécuritéFR", "GestionIdentités", "IAM", "OpenIDConnect", "SécuritéRéseau"]
summary: "Entre 2023 et 2024, VPN et pare-feu sont devenus des cibles prioritaires des attaquants. Ce que ça change pour la gestion des identités et des accès."
cover:
  image: "/covers/_ipXrAM-cIg.jpg"
  alt: "IAM : pourquoi VPN et pare-feu sont devenus des cibles prioritaires"
  caption: "Cybersécurité"
draft: false
catalogue_id: "b52d50cd"
translationKey: "b52d50cd"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/_ipXrAM-cIg" title="Voir la vidéo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

Entre 2023 et 2024, les attaques contre les équipements de sécurité périmétrique (VPN et pare-feu) se sont intensifiées, modifiant profondément les priorités de défense. Le CERT-FR documente une exploitation systématique de ces failles par des acteurs étatiques et des groupes criminels pour obtenir un accès persistant aux réseaux. Cette tendance révèle une limitation majeure : les dispositifs frontières, bien que critiques, ne suffisent plus à garantir la protection des identités et des accès. Les organisations doivent réorienter leur stratégie vers une gestion des identités stricte, combinant authentification standardisée (OpenID Connect 1.0), segmentation réseau et logging exhaustif. L'enjeu dépasse la simple correction de failles techniques : il porte sur la reconstruction d'une architecture de confiance zéro, où chaque accès est validé indépendamment de la position réseau de l'utilisateur.

## Principaux points abordés

- **Vague d'attaques ciblées sur la sécurité périmétrique** — Le CERT-FR identifie une augmentation substantielle des compromissions de passerelles VPN et pare-feu sur la période 2023-2024, exploitées comme vecteurs d'entrée initial par des acteurs sophistiqués (états et cybercriminels).

- **Accès persistant et mouvement latéral** — Une fois les équipements de frontière neutralisés, les attaquants établissent une présence durable permettant l'exfiltration de données et le pivotage interne, selon le retour d'expérience du CERT-FR sur les incidents du secteur social.

- **Standardisation de l'authentification via OpenID Connect 1.0** — Cette couche d'identité bâtie sur OAuth 2.0 fournit des mécanismes normalisés (ID Tokens, interaction flows) pour sécuriser l'authentification utilisateur, réduisant la dépendance aux seules barrières réseau.

- **Segmentation réseau comme rempart supplémentaire** — La documentation ANSSI préconise une microsegmentation rigoureuse et un logging centralisé pour détecter les mouvements anormaux post-compromission, complément indispensable au contrôle d'identité.

- **Limite majeure : confusion entre périmètre et accès** — Les organisations ayant tablé exclusivement sur des pare-feu robustes ne disposent pas des mécanismes d'authentification granulaire ni du Zero Trust nécessaires ; la sécurité du VPN/pare-feu ne compense pas l'absence de gouvernance des identités.

- **Impact opérationnel** — Les équipes de sécurité doivent intégrer : audit continu des accès (Privileged Access Manager), vérification des identités à chaque requête (FIDO Alliance), conformité aux modèles de maturité Zero Trust (CISA), et gestion centralisée des comptes (SCIM).

## Références (Golden Sources)

- [Failles sur les équipements de sécurité : retour d'expérience du CERT-FR - ANSSI](https://www.cert.ssi.gouv.fr/uploads/20240612_NP_ANSSI-SDO_Retex-Vuln_vf.pdf)

- [Cloud Computing - CERT-FR - ANSSI](https://www.cert.ssi.gouv.fr/uploads/CERTFR-2025-CTI-001.pdf)

- [OpenID Connect Core 1.0 incorporating errata set 2](https://openid.net/specs/openid-connect-core-1_0.html)

- [Zero Trust Maturity Model Version 2.0 - CISA](https://www.cisa.gov/sites/default/files/2023-04/zero_trust_maturity_model_v2_508.pdf)

- [Exfiltration de données du secteur social : retour d'expérience du CERT-FR](https://www.cert.ssi.gouv.fr/uploads/CERTFR-2024-CTI-009.pdf)

- [Privileged Access Manager - Self-Hosted Architecture - CyberArk Docs](https://docs.cyberark.com/pam-self-hosted/latest/en/content/pasimp/privileged-account-security-solution-architecture.htm)
## Chapitres

- `0:00` — Introduction générale
- `0:33` — Gestion identités et accès
- `1:04` — L'identité numérique expliquée
- `2:10` — Authentification et sécurité

## Ressources Wet & Sea Tech

**Chaîne YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Boutique :** https://wetseatech.etsy.com

**Tous les articles Cybersécurité :** https://wst-tech.org/tags/cybersecurity/
