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

Le 31 mars 2026, une erreur de packaging a exposé le code source complet de Claude Code sur npm via un fichier source map oublié. Cette fuite involontaire a révélé environ 1 900 fichiers TypeScript et 512 000 lignes de code, permettant une analyse détaillée de l'architecture interne de l'agent de développement d'Anthropic. L'incident a catalysé la création de Claw Code, un clone open source en Rust devenu viral. Au-delà de l'aspect sensationnel, cette divulgation expose les mécanismes fondamentaux des systèmes agentiques autonomes : boucles d'exécution minimalistes, gestion d'état basée sur les messages, utilisation du protocole MCP pour les outils externes, et fonctionnalités non documentées. Les enjeux croisent la sécurité logicielle, la gouvernance des modèles d'IA et la propriété intellectuelle face aux outils générés par IA.

## Principaux points abordés

- **Architecture de la boucle agentique** : le noyau de Claude Code repose sur une boucle de 88 lignes minimaliste gérant l'orchestration des appels au modèle, la récupération d'outils et la gestion des sessions via un état stocké sous forme de messages.

- **Protocole MCP pour l'intégration d'outils** : Claude Code s'appuie sur le Model Context Protocol pour communiquer avec des outils externes, permettant une modulabilité et une extensibilité contrôlées des capacités agentiques.

- **Fichier undercover.ts et fonctionnalités cachées** : la fuite révèle l'existence de composants non documentés publiquement, incluant Kairos (probablement un système de planification temporelle), un classificateur « YOLO » et Ultraplan, soulevant des questions sur les capabilités réelles de l'agent comparées à sa documentation officielle.

- **Latence assumée et choix architecturaux** : le code met en évidence une acceptation délibérée de latences dans l'exécution agentique, favorisant la robustesse et la gestion d'état sur la réactivité immédiate.

- **Réplication rapide en Rust** : Claw Code a atteint 105 000 stars en 24 heures, démontrant que la barrière technique à la reproduction d'architectures agentiques complexes s'est effondrée, augmentant les risques de déploiements non sécurisés ou non vérifiés.

- **Paradoxe de la propriété intellectuelle** : la publication accidentelle du code source, suivi d'une campagne de 8 000 takedowns DMCA, pose la question de la protection légale du code d'IA écrit par des modèles face aux clones générés par d'autres modèles, révélant un vide juridique structurel.

- **Limitation : divergence GitHub vs production** — les sources indiquent que le code publié diffère potentiellement des versions déployées en production, limitant la compréhension réelle des systèmes autonomes actuels.

## Références (Golden Sources)

- [Claude Code Architecture Explained: Agent Loop, Tool System, and Permission Mode](https://dev.to/brooks_wilson_36fbefbbae4/claude-code-architecture-explained-agent-loop-tool-system-and-permission-model-rust-rewrite-41b2)
- [Claw Code: Open-Source Claude Code Clone With 105K Stars in 24 Hours](https://klymentiev.com/blog/claw-code-claude-source)
- [AI Governance & Security Platform | Harmonic Security](https://www.harmonic.security/resources/security-lessons-from-claude-codes-first-year)
- [After Anthropic Open-Sourced Its Source Code, It Issued Over 8,000 Copyright Tak](https://www.techflowpost.com/en-US/article/30966)
- [When AI-Written Code Gets Rewritten by AI: The Copyright Vacuum Exposed by the C](https://yage.ai/share/claude-code-copyright-paradox-en-20260402.html)
- [Anthropic keeps latest AI tool out of public's hands for fear of enabling widesp](https://www.theguardian.com/technology/2026/apr/08/anthropic-ai-cybersecurity-software)
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
