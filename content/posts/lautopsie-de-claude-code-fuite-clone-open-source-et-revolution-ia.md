---
title: "Fuite du code de Claude Code sur npm : ce qu'on a trouvé dedans"
date: 2026-06-06
slug: "lautopsie-de-claude-code-fuite-clone-open-source-et-révolution-ia"
youtube_url: "https://youtu.be/IuDPR-uIw3A"
youtube_video_id: "IuDPR-uIw3A"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "ia-travail"
categories: ["IA & Travail"]
tags: ["ia-travail", "Anthropic", "ClaudeCode", "ClawCode", "IA", "OpenSource"]
summary: "Le 31 mars 2026, un fichier source map oublié dans un paquet npm expose les 512 000 lignes de Claude Code. Boucle de 88 lignes, fichier undercover.ts, fonctions cachées : l'autopsie."
cover:
  image: "/covers/IuDPR-uIw3A.jpg"
  alt: "Fuite du code de Claude Code sur npm : ce qu'on a trouvé dedans"
  caption: "IA & Travail"
draft: false
catalogue_id: "53472135"
translationKey: "53472135"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/IuDPR-uIw3A" title="Voir la vidéo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

Le 31 mars 2026, une fuite accidentelle expose le code source complet de Claude Code sur npm via un fichier source map oublié. Cette divulgation de 512 000 lignes de TypeScript révèle l'architecture interne de l'agent de développement d'Anthropic : une boucle d'agent minimaliste, une gestion d'état par messages et des fonctionnalités non documentées. La fuite a déclenché une réaction en chaîne : création immédiate de Claw Code, un clone open source réécrit en Rust attirant 105 000 étoiles GitHub en 24 heures. Au-delà des enjeux de sécurité opérationnelle, cet incident soulève des questions critiques sur la gouvernance du code, la gestion des droits d'auteur en contexte IA, et les limites des stratégies de confinement technologique face aux agents autonomes.

## Principaux points abordés

- **Mécanisme de la fuite** : un source map non supprimé lors du packaging npm expose les 1 900 fichiers TypeScript originaux, révélant l'absence de minification et de protection au niveau build.

- **Architecture révélée** : boucle d'agent de 88 lignes, stockage d'état sous forme de messages (pattern conversationnel), intégration du protocole MCP pour l'invocation d'outils, file d'attente de tâches et gestion des permissions implicite.

- **Fonctionnalités cachées documentées** : fichier `undercover.ts`, modules nommés Kairos (gestion de contexte), classificateur YOLO (décision rapide), Ultraplan (planification étendue), et utilitaires Dr non exposés publiquement.

- **Reproduction rapide et viable** : Claw Code atteint 105 000 stars en 24 heures, confirmant que l'architecture publiée est suffisamment complète pour être réimplémentée. La version Rust démontre qu'aucun secret propriétaire majeur n'était véhiculé par le code.

- **Paradoxe juridique** : après la fuite, Anthropic émet plus de 8 000 notifications DMCA, créant une situation où le code open source dérivé génère des conflits de propriété intellectuelle, particulièrement dans un contexte où le code original est lui-même généré ou amélioré par IA.

- **Implications de sécurité gouvernance** : la divulgation expose non seulement la logique métier, mais potentiellement les vecteurs d'attaque spécifiques au système d'agents, les limites de latence acceptées, et la surface d'interception MCP. Anthropic maintient intentionnellement Claude Code hors du domaine public pour limiter les usages adversariaux.

## Références (Golden Sources)

- [Claude Code Architecture Explained: Agent Loop, Tool System, and Permission Model — Rust Rewrite](https://dev.to/brooks_wilson_36fbefbbae4/claude-code-architecture-explained-agent-loop-tool-system-and-permission-model-rust-rewrite-41b2)
- [Claw Code: Open-Source Claude Code Clone With 105K Stars in 24 Hours](https://klymentiev.com/blog/claw-code-claude-source)
- [After Anthropic Open-Sourced Its Source Code, It Issued Over 8,000 Copyright Takedowns](https://www.techflowpost.com/en-US/article/30966)
- [AI Governance & Security Platform | Harmonic Security — Security Lessons from Claude Code's First Year](https://www.harmonic.security/resources/security-lessons-from-claude-codes-first-year)
- [When AI-Written Code Gets Rewritten by AI: The Copyright Vacuum Exposed by the Claude Code Leak](https://yage.ai/share/claude-code-copyright-paradox-en-20260402.html)
- [Anthropic Keeps Latest AI Tool Out of Public's Hands for Fear of Enabling Widespread Cybersecurity Risks](https://www.theguardian.com/technology/2026/apr/08/anthropic-ai-cybersecurity-software)
## Chapitres

- `0:00` — Introduction et contexte
- `0:34` — La fuite accidentelle d'Anthropic
- `1:09` — 512 000 lignes exposées
- `1:41` — L'erreur de packaging expliquée
- `2:14` — Performances de Claude Code
- `3:34` — Impact et révolution IA

## Ressources Wet & Sea Tech

**Chaîne YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Boutique :** https://wetseatech.etsy.com

**Tous les articles IA & Travail :** https://wst-tech.org/tags/ia-travail/
