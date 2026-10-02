---
title: "DeepSeek Harness : les 4 modes d'exécution comparés, lequel choisir ?"
date: 2026-08-26
slug: "deepseek-harness-démystifier-larchitecture-des-agents-ia"
youtube_url: "https://youtu.be/jD3Qp1bkao4"
youtube_video_id: "jD3Qp1bkao4"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "ia-travail"
categories: ["IA & Travail"]
tags: ["ia-travail", "AIDevOps", "AgentsIA", "ArchitecturePlugin", "DeepSeekHarness", "DéveloppementAutonome", "ia", "chatgpt", "machine learning", "technologie", "claude code", "ai", "deep learning", "ai tools", "chat gpt", "ai agent", "llm", "intelligence artificielle"]
summary: "Standard, Minimal, Code ou Creator : DeepSeek Harness propose 4 modes pour ses agents IA. Lequel choisir, et pourquoi le « harness » compte autant que le modèle ?"
cover:
  image: "/covers/jD3Qp1bkao4.jpg"
  alt: "DeepSeek Harness : les 4 modes d'exécution comparés, lequel choisir ?"
  caption: "IA & Travail"
draft: false
catalogue_id: "a98acc82"
translationKey: "a98acc82"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/jD3Qp1bkao4" title="Voir la vidéo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

DeepSeek Harness, lancé en août 2026 avec le modèle V4 Pro, introduit une architecture modulaire où le modèle d'IA (« cerveau ») se dissocie du moteur d'exécution (« harness »). Cette séparation permet aux équipes DevOps et aux responsables d'infrastructure d'inspecter, configurer et contrôler chaque étape du cycle d'exécution des agents. Contrairement aux systèmes fermés comme Claude ou Codex, DeepSeek Harness expose quatre modes d'exécution distincts — Standard, Minimal, Code et Creator — adaptés à des contraintes opérationnelles différentes. Le choix du mode impacte directement la traçabilité, la consommation de ressources et la conformité de sécurité, ce qui place le harness au cœur de la stratégie de déploiement.

## Principaux points abordés

- **Architecture décentralisée basée sur les plugins** : chaque composant du runtime (cycle d'exécution, protocoles de sécurité, gestion des appels externes) fonctionne comme un plugin interchangeable, permettant une personnalisation sans modification du modèle sous-jacent.

- **Mode Standard : équilibre polyvalent** — configuration par défaut pour la plupart des cas d'usage ; offre journalisation complète et gestion intégrale des ressources sans surcharge opérationnelle significative.

- **Mode Minimal : économie de ressources** — réduit la charge de calcul et la mémoire en supprimant composants secondaires ; adapté aux déploiements sur VPS ou environnements contraints, au prix d'une traçabilité amoindrie.

- **Mode Code : optimisation pour le développement logiciel** — enrichit le harness avec des boucles de feedback spécialisées pour l'inspection de code, l'analyse statique intégrée et l'accès granulaire aux arbres syntaxiques ; ciblage des projets de génération et refactorisation automatisée.

- **Mode Creator : créativité et itération complexe** — configuration étendue pour les tâches multi-étapes d'exploration algorithmique ou conception ; augmente les ressources allouées aux cycles de raisonnement non linéaire.

- **Limite critique : dépendance à la chaîne de plugins** — une configuration modulaire exige une maintenance rigoureuse et une documentation des dépendances entre plugins ; le gain de flexibilité introduit des risques de divergence entre environnements de développement et production si les versions ne sont pas épinglées.

- **Enjeu de gouvernance et cybersécurité** — la journalisation intégrale et l'accessibilité des boucles d'exécution permettent un audit complet des décisions de l'agent, facilitant la conformité réglementaire (RGPD, ISO 27001) et le contrôle interne ; inversement, l'exposition des artefacts d'exécution nécessite des politiques de chiffrement et d'accès strictes.

## Références (Golden Sources)

- [DeepSeek Harness developer preview: Everything is a plugin](https://deepseek.com/harness/en/)
- [DeepSeek Harness Has 4 Modes: Standard, Code, Minimal, and Creator Explained](https://shop.zimaspace.com/blogs/tech-ai-hub/de-minimal-and-creator-explained)
- [DeepSeek Harness Explained: How Open Agent Runtimes Change AI](https://www.turingpost.com/p/deepseek-harness-explained)
- [DeepSeek Harness turns every part of an agent runtime into a swappable plugin](https://www.i-scoop.eu/deepseek-harness-turns-every-part-of-an-agent-runtime-into-a-swappable-plugin/)
- [DeepSeek Harness on a VPS: keep it private - SSD Nodes](https://www.ssdnodes.com/learn/deepseek-harness-on-a-vps)
- [DeepSeek Harness Review: Is the Plugin Stack Production-Ready? - Wavect](https://wavect.io/blog/deepseek-harness-enterprise-review/)
## Chapitres

- `0:00` — Architectural Analysis of DeepSeek Harness: A Spatiotempora…
- `0:10` — Awesome Pi Coding Agent - GitHub
- `1:58` — BENCHMARK.md - xuguoliang3/deepseek-harness - GitCode
- `2:08` — CodeWhale/docs/PROVIDERS.md at main - GitHub
- `2:28` — Data Processing Statement - DeepSeek Harness
- `2:38` — Data Processing Statement - DeepSeek Harness
- `2:48` — DeepSeek AI Releases DeepSeek Harness in Developer Preview:…
- `2:58` — DeepSeek Harness - Ollama documentation
- `3:08` — DeepSeek Harness Explained: How Open Agent Runtimes Change…
- `3:18` — DeepSeek Harness Has 4 Modes: Standard, Code, Minimal, and…
- `3:34` — DeepSeek Harness Review: Is the Plugin Stack Production-Rea…
- `3:44` — DeepSeek Harness developer preview: Everything is a plugin
- `3:54` — DeepSeek Harness for OpenHouse - GitCode
- `4:04` — DeepSeek Harness on a VPS: keep it private - SSD Nodes
- `4:14` — DeepSeek Harness turns every part of an agent runtime into…
- `4:24` — DeepSeek Harness vs OpenCode: Which Coding Agent Should You…
- `4:34` — DeepSeek Harness | Safe Use Policy
- `4:44` — DeepSeek Harness: Everything is a Plugin. - GitHub
- `4:54` — DeepSeek Harness: Open-Source Agent Runtime - Eigent AI
- `5:04` — DeepSeek Harness: Why 95,000 GitHub Stars in 2 Days Matters…
- `5:14` — DeepSeek Harness: plugins, core and capability seams - noze
- `5:24` — DeepSeek Open-Sources Harness: Everything Is a Plugin - Dig…
- `5:34` — DeepSeek open sources an agent harness where everything is…
- `5:49` — DeepSeek open sources an agent harness where everything is…
- `5:59` — Deepseek Harnness - why is feels better : r/LocalLLaMA - Re…

## Ressources Wet & Sea Tech

**Chaîne YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Boutique :** https://wetseatech.etsy.com

**Tous les articles IA & Travail :** https://wst-tech.org/tags/ia-travail/
