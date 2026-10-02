---
title: "Agents IA : pourquoi les enfermer dans un bac à sable noyau"
date: 2026-08-22
slug: "sécurité-des-agents-ia-bacs-à-sable-mcp-défense-en-profondeur"
youtube_url: "https://youtu.be/J1sc_kWU4Xk"
youtube_video_id: "J1sc_kWU4Xk"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "cybersecurity"
categories: ["Cybersécurité"]
tags: ["cybersecurity", "Cybersécurité", "MCP", "ai agents", "bedrock agents", "ia agents", "mcp explained", "mcp ia", "artificial intelligence", "mcp tutorial", "what is mcp", "ai business", "google gemini"]
summary: "Un agent IA qui peut lire vos fichiers, ouvrir le réseau et exécuter du code : comment limiter les dégâts ? La réponse d'Anthropic et d'Always Further : l'isolation au niveau du noyau."
cover:
  image: "/covers/J1sc_kWU4Xk.jpg"
  alt: "Agents IA : pourquoi les enfermer dans un bac à sable noyau"
  caption: "Cybersécurité"
draft: false
catalogue_id: "b07058a6"
translationKey: "b07058a6"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/J1sc_kWU4Xk" title="Voir la vidéo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

Les agents d'intelligence artificielle ouvrent de nouvelles surfaces de risque en cybersécurité : accès non autorisé aux fichiers, exécution de code incontrôlée et mouvements latéraux sur les réseaux. Pour limiter ces risques, Anthropic et Always Further préconisent une stratégie d'isolation au niveau du noyau du système d'exploitation. Cette approche combine des bacs à sable kernel (implémentés par des outils comme nono), une gestion granulaire des permissions IAM, et l'utilisation du protocole MCP pour cadrer l'exécution de code. L'enjeu opérationnel consiste à maintenir la fonctionnalité des agents autonomes tout en réduisant la surface d'attaque lors du déploiement en environnement sensible.

## Principaux points abordés

- **Isolation au niveau kernel** : les bacs à sable noyau (kernel sandboxing) contiennent une compromission en limitant l'accès aux ressources système, indépendamment de l'authentification applicative. L'outil nono incarne cette approche en restricting l'accès aux fichiers et au réseau au plus bas niveau du système.

- **MCP (Model Context Protocol) pour l'exécution de code** : ce protocole encadre l'exécution de code à travers une architecture modulaire qui réduit simultanément la consommation de tokens et centralise le contrôle des opérations. Les serveurs MCP agissent comme intermédiaires de confiance entre l'agent et les ressources.

- **Défense en profondeur par permissions IAM** : au-delà de l'isolation technique, l'attribution de droits minimaux (least privilege) aux identités AWS, via IAM Identity Center et les API keys, constitue un deuxième étage de défense. Ceci limite les dégâts même en cas de contournement du bac à sable.

- **Déploiement sécurisé de Claude Code** : Amazon Bedrock propose des patterns de déploiement validés incluant l'authentification, la gestion des secrets et l'audit cryptographique. Les équipes doivent configurer ces paramètres au niveau entreprise, pas par défaut.

- **Contradiction potentielle** : l'isolation kernel augmente la complexité opérationnelle et peut réduire les performances en comparaison d'une exécution non contrôlée. Le trade-off entre sécurité et latence nécessite une évaluation contextuelle par cas d'usage.

- **Impact gouvernance et infrastructure** : cette approche impose une architecture d'isolation implicite dès la phase de conception, non comme correctif post-déploiement. Elle exige également un audit continu des logs et des permissions IAM pour détecter les écarts.

## Références (Golden Sources)

- [Code execution with MCP: building more efficient AI agents](https://www.anthropic.com/engineering/code-execution-with-mcp)
- [AI Agent Security & Kernel Sandboxing](https://alwaysfurther.ai/)
- [Claude Code deployment patterns and best practices with Amazon Bedrock](https://aws.amazon.com/blogs/machine-learning/claude-code-deployment-patterns-and-best-practices-with-amazon-bedrock/)
- [Authentication - Claude Code Docs](https://docs.anthropic.com/en/docs/claude-code/iam)
- [Connect Claude Code to tools via MCP - Claude Code Docs](https://docs.anthropic.com/en/docs/claude-code/mcp)
- [Enterprise deployment overview - Claude Code Docs](https://docs.anthropic.com/en/docs/claude-code/enterprise-setup)
## Chapitres

- `0:00` — Introduction & contexte
- `1:04` — Illusion des autorisations humaines
- `2:04` — Fatigue d'approbation & risques
- `2:46` — Cas réel : exfiltration AWS

## Ressources Wet & Sea Tech

**Chaîne YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Boutique :** https://wetseatech.etsy.com

**Tous les articles Cybersécurité :** https://wst-tech.org/tags/cybersecurity/
