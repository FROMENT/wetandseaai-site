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

Les agents d'intelligence artificielle capables d'exécuter du code, d'accéder aux fichiers et de se connecter aux réseaux représentent une surface de risque critique en cybersécurité. Anthropic et Always Further proposent une stratégie d'isolation au niveau du noyau via des bacs à sable (sandbox) pour contenir les compromissions potentielles. Cette approche technique combine plusieurs couches : isolation des processus au niveau système, gestion granulaire des permissions via IAM, et vérification cryptographique. L'enjeu opérationnel porte sur la nécessité de limiter l'exposition des agents sans sacrifier leur capacité d'action légitime, particulièrement en environnement d'entreprise où les accès non autorisés aux données critiques constituent une menace directe.

## Principaux points abordés

- **Isolation au niveau du noyau via l'outil nono** : les bacs à sable noyau contiennent les exfiltrations de données et les exécutions de code malveillantes en créant une frontière système imperméable, isolant les processus de l'agent de l'accès direct aux ressources hôte.

- **Architecture MCP (Model Context Protocol) pour l'exécution sandboxée** : le protocole MCP encadre l'exécution de code dans des conteneurs ou environnements isolés, tout en réduisant la consommation de tokens par une architecture modulaire et l'appel sélectif de fonctions.

- **Gestion stricte des permissions IAM** : l'authentification et les droits d'accès doivent être configurés au niveau grain fin (API keys, SSO, Identity Center) pour limiter la portée des agents aux ressources absolument nécessaires, avec audit cryptographique.

- **Déploiement sécurisé de Claude via Amazon Bedrock** : les patterns de déploiement en entreprise impliquent une authentification forte (IAM, SSO), une configuration explicite des outils accessibles et une séparation nette entre développement et production.

- **Limite majeure : le contrôle n'est jamais absolu** : même avec bacs à sable, les chaînes d'approvisionnement logicielles (dépendances, plugins MCP) et les erreurs de configuration des droits demeurent des vecteurs d'attaque. La défense en profondeur est obligatoire, pas optionnelle.

- **Impact opérationnel** : les entreprises doivent arbitrer entre l'automatisation (agents autonomes) et la sécurité. L'adoption d'agents IA nécessite une révision des architectures de sécurité existantes et une gouvernance stricte des accès, sous peine d'augmenter de façon exponentielle la surface d'attaque.

## Références (Golden Sources)

- [AI Agent Security & Kernel Sandboxing | Always Further](https://alwaysfurther.ai/)
- [Code execution with MCP: building more efficient AI agents \ Anthropic](https://www.anthropic.com/engineering/code-execution-with-mcp)
- [Claude Code deployment patterns and best practices with Amazon Bedrock | Artific](https://aws.amazon.com/blogs/machine-learning/claude-code-deployment-patterns-and-best-practices-with-amazon-bedrock/)
- [Connect Claude Code to tools via MCP - Claude Code Docs](https://docs.anthropic.com/en/docs/claude-code/mcp)
- [Authentication - Claude Code Docs](https://docs.anthropic.com/en/docs/claude-code/iam)
- [AWS IAM Identity Center concepts for the AWS CLI - AWS Command Line Interface](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-sso-concepts.html)
## Chapitres

- `0:00` — Introduction & contexte
- `1:04` — Illusion des autorisations humaines
- `2:04` — Fatigue d'approbation & risques
- `2:46` — Cas réel : exfiltration AWS

## Ressources Wet & Sea Tech

**Chaîne YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Boutique :** https://wetseatech.etsy.com

**Tous les articles Cybersécurité :** https://wst-tech.org/tags/cybersecurity/
