---
title: "OpenClaw : Vulnérabilités Critiques des Agents IA Autonomes"
date: 2026-04-16
youtube_url: "https://youtu.be/MG7lIGDPeuU"
youtube_video_id: "MG7lIGDPeuU"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "cybersecurity"
categories: ["Cybersécurité"]
tags: ["cybersecurity"]
summary: "These sources describe **OpenClaw**, an open-source autonomous AI assistant designed to execute complex workflows across messaging platforms like **WhatsApp**, **Slack**, and **Discord**. Originally…"
cover:
  image: "/covers/MG7lIGDPeuU.jpg"
  alt: "OpenClaw : Vulnérabilités Critiques des Agents IA Autonomes"
  caption: "Cybersécurité"
draft: false
catalogue_id: "a606f4d0"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/MG7lIGDPeuU" title="Voir la vidéo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

OpenClaw, assistant autonome open-source conçu pour automatiser des workflows complexes sur WhatsApp, Slack et Discord, a connu une adoption virale début 2026 avant de révéler des vulnérabilités critiques. L'architecture du système repose sur des fichiers Markdown éditables et des bases de données vectorielles pour la persistance mémoire, caractéristique initialement perçue comme avantage en termes de transparence. Les recherches en sécurité ont cependant identifié des vecteurs d'attaque majeurs : injection de prompts, exécution de code à distance et distribution de malware via la marketplace ClawHub. Ces failles exposent les entreprises exploitant des agents IA autonomes à des risques de compromission d'identité, d'exfiltration de tokens d'authentification et d'accès non autorisé aux données sensibles. L'incident soulève des questions structurelles sur le chaînage de sécurité des composants tiers dans les écosystèmes d'agents IA.

## Principaux points abordés

- **CVE-2026-25253 et exécution de code distant** — vulnérabilité permettant l'exécution de code via exfiltration de tokens d'authentification, exploitable en un clic selon les analyses de sécurité.

- **Centaines de composants malveillants dans ClawHub** — la marketplace officielle héberge des "skills" compromises distribuant du malware MacOS (Atomic Stealer) et autres charge utiles persistantes.

- **Injection de prompts et contournement de contrôles** — l'architecture à mémoire transparente permet aux attaquants de manipuler les directives système via les fichiers Markdown, contournant les garde-fous de sécurité.

- **Gestion des dépendances tiers critique** — contrairement aux assistants gérés centralement (Claude Computer Use d'Anthropic), OpenClaw délègue la validation des composants à des contributeurs externes sans chaînage de confiance formalisé.

- **Impact sur la sécurité d'identité d'entreprise** — l'accès des agents autonomes aux systèmes d'authentification (tokens, credentials) amplifie les risques en cas de compromission, transformant chaque agent en point d'accès privilégié.

## Références (Golden Sources)

Sources :
- https://socradar.io/blog/cve-2026-25253-rce-openclaw-auth-token/
- https://www.esecurityplanet.com/threats/hundreds-of-malicious-skills-found-in-openclaws-clawhub/
- https://www.trendmicro.com/en_us/research/26/b/openclaw-skills-used-to-distribute-atomic-macos-stealer.html
- https://www.cyberark.com/resources/agentic-ai-security/how-autonomous-ai-agents-like-openclaw-are-reshaping-enterprise-identity-security/
- https://github.com/slowmist/openclaw-security-practice-guide
## Chapitres

- `0:00` — Introduction d'OpenClaw
- `0:35` — Distinction des projets
- `1:09` — Popularité virale chaotique
- `2:15` — Système de mémoire innovant

## Références (Golden Sources)

- [A frightening OpenClaw vulnerability has been discovered | Mashable](https://mashable.com/article/new-frightening-openclaw-vulnerability-has-been-discovered)
- [Anthropic Ends OpenClaw Access: It's Not Just the Bill](https://blog.cyberdesserts.com/anthropic-openclaw/)
- [Anthropic's Claude Computer use vs OpenClaw (Moltbot) Comparison](https://aiagentstore.ai/compare-ai-agents/anthropic-s-claude-computer-use-vs-openclaw-moltbot)
- [CVE-2026-25253: 1-Click RCE in OpenClaw Through Auth Token Exfiltration](https://socradar.io/blog/cve-2026-25253-rce-openclaw-auth-token/)
- [Claw (video game) - Wikipedia](https://en.wikipedia.org/wiki/Claw_(video_game))
- [Cloud AI Agents vs. Local AI Agents: Why the OpenClaw Explosion Proves Cloud Is the Smarter Choice](https://www.ninjatech.ai/blog/cloud-ai-agents-vs-local-ai-agents)
- [Earn 40,000 Stars in a Frenzy: Replacing OpenClaw Is Satisfying, Get an AI Worker for Just $5](https://eu.36kr.com/en/p/3759493153653253)
- [GitHub - pjasicek/OpenClaw: Reimplementation of Captain Claw (1997) platformer · GitHub](https://github.com/pjasicek/OpenClaw)
- [GitHub - slowmist/openclaw-security-practice-guide: This guide is designed for OpenClaw itself (Agent-facing), not as a traditional human-only hardening checklist. · GitHub](https://github.com/slowmist/openclaw-security-practice-guide)
- [How autonomous AI agents like OpenClaw are reshaping enterprise identity security](https://www.cyberark.com/resources/agentic-ai-security/how-autonomous-ai-agents-like-openclaw-are-reshaping-enterprise-identity-security)
- [How to Install OpenClaw Locally: A Comprehensive Technical Guide - H3sync](https://h3sync.com/blog/how-to-install-openclaw-locally-a-comprehensive-technical-guide/)
- [Hundreds of Malicious Skills Found in OpenClaw's ClawHub | eSecurity Planet](https://www.esecurityplanet.com/threats/hundreds-of-malicious-skills-found-in-openclaws-clawhub/)
- [Introducing OpenClaw — OpenClaw Blog](https://openclaw.ai/blog/introducing-openclaw)
- [Malicious OpenClaw Skills Used to Distribute Atomic MacOS Stealer | Trend Micro (US)](https://www.trendmicro.com/en_us/research/26/b/openclaw-skills-used-to-distribute-atomic-macos-stealer.html)
- [OpenAI: Latest news and insights – Computerworld](https://www.computerworld.com/article/4015023/openai-latest-news-and-insights.html)

<details>
<summary>Voir les 14 sources restantes</summary>

- [OpenClaw - Wikipedia](https://en.wikipedia.org/wiki/OpenClaw)
- [OpenClaw Complete Tutorial 2026: Setup, Skills, Memory, and Architecture Explained | Towards AI](https://pub.towardsai.net/openclaw-complete-guide-setup-tutorial-2026-14dd1ae6d1c2)
- [OpenClaw Evolution: 142K Stars, ESG Workflows & Critical Risks](https://vertu.com/ar/ai-tools/from-clawdbot-to-openclaw-142k-stars-three-names-and-how-this-lobster-ai-transforms-esg-work/)
- [OpenClaw Launches Version 2026.4.9 with 'Dreaming' Feature for AI Agent Memory | KuCoin](https://www.kucoin.com/news/flash/openclaw-launches-version-2026-4-9-with-dreaming-feature-for-ai-agent-memory)
- [OpenClaw Open Source AI Agent Application Attack Surface and Security Risk System Analysis - NSFOCUS, Inc., a global network and cyber security leader, protects enterprises and carriers from advanced cyber attacks.](https://nsfocusglobal.com/openclaw-open-source-ai-agent-application-attack-surface-and-security-risk-system-analysis/)
- [OpenClaw Prompt Attacks and How to Protect Your AI Applications - Alibaba Cloud Community](https://www.alibabacloud.com/blog/openclaw-prompt-attacks-and-how-to-protect-your-ai-applications_602853)
- [OpenClaw Security Guide 2026 | Contabo Blog](https://contabo.com/blog/openclaw-security-guide-2026/)
- [OpenClaw Version 2026.4.7 Released with New Features | Phemex News](https://phemex.com/news/article/openclaw-launches-version-202647-with-enhanced-features-71603)
- [OpenClaw Vulnerability Allowed Websites to Hijack AI Agents - SecurityWeek](https://www.securityweek.com/openclaw-vulnerability-allowed-malicious-websites-to-hijack-ai-agents/)
- [OpenClawd Releases Major Platform Update as OpenClaw Surpasses React With 250,000 GitHub Stars](https://www.accessnewswire.com/newsroom/en/computers-technology-and-internet/openclawd-releases-major-platform-update-as-openclaw-surpasses-re-1143535)
- [Openclaw Release Notes - April 2026 Latest Updates - Releasebot](https://releasebot.io/updates/openclaw)
- [Overnight Change, Anthropic Officially Bans OpenClaw! Global Developers Collapse in 24 Hours | ME News on Binance Square](https://www.binance.com/en/square/post/308749699730466)
- [Releases · openclaw/openclaw](https://github.com/openclaw/openclaw/releases)
- [Snyk Finds Prompt Injection in 36%, 1467 Malicious Payloads in a ToxicSkills Study of Agent Skills Supply Chain Compromise | Snyk](https://snyk.io/blog/toxicskills-malicious-ai-agent-skills-clawhub/)

</details>

## Ressources Wet & Sea Tech

**Chaîne YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Boutique :** https://wetseatech.etsy.com

**Tous les articles Cybersécurité :** https://wetandseaai.pascal-froment.workers.dev/tags/cybersecurity/
