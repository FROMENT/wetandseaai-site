---
title: "Mini Shai-Hulud : Le ver qui compromet 160+ packages npm et PyPI"
date: 2026-08-22
youtube_url: "https://youtu.be/dfTns8nBHvc"
youtube_video_id: "dfTns8nBHvc"
youtube_channel: "A"
youtube_channel_handle: "@discover-allin360"
youtube_channel_url: "https://www.youtube.com/@discover-allin360"
youtube_channel_name: "Voyage Discovery 360 · IA & Aventures"
theme: "ia-travail"
categories: ["IA & Travail"]
tags: ["ia-travail"]
summary: "Mini Shai-Hulud exploite GitHub Actions pour infecter massivement l'écosystème open source via des tokens OIDC légitimes."
cover:
  image: "/covers/dfTns8nBHvc.jpg"
  alt: "Mini Shai-Hulud : Le ver qui compromet 160+ packages npm et PyPI"
  caption: "IA & Travail"
draft: false
catalogue_id: "8c4d1af9"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/dfTns8nBHvc" title="Voir la vidéo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Contexte

The provided documents detail a large-scale supply chain attack known as 
**Mini Shai-Hulud**, a self-propagating worm that has compromised over 160 
**npm and PyPI packages**. Orchestrated by the **TeamPCP threat group**, the 
malware exploits **GitHub Actions** misconfigurations, specifically using a 
novel "orphaned commit" technique to bypass branch protections and obtain 
legitimate **OIDC publishing tokens**. Once active, the worm harvests 
extensive credentials—including **cloud provider keys, GitHub tokens, and 
Kubernetes secrets**—from developer workstations and CI/CD runners. It further
ensures its survival through persistence mechanisms in **VS Code** and 
**Claude Code** and includes a destructive "dead man's switch" that wipes data
if stolen tokens are revoked. Security researchers emphasize that affected 
packages carry **valid provenance attestations**, proving that current trust 
frameworks can be subverted by compromised build pipelines. To mitigate the 
threat, organizations must rotate all credentials, remove persistent daemons, 
and tighten the scope of their **OpenID Connect** configurations.

## Références (Golden Sources)

- [#5 — Anthropic Mythos Finds Thousands of Zero-Days, Axios Reaches OpenAI, Cisco Buys Galileo - AppSec Santa](https://appsecsanta.com/newsletter/2026-w16)
- ['Mini Shai-Hulud' malware compromises hundreds of open-source packages in sprawling supply-chain attack | CyberScoop](https://cyberscoop.com/mini-shai-hulud-supply-chain-malware-attack/)
- [A Mini Shai-Hulud Has Appeared: Obfuscated Bun Runtime Payloads Hit SAP-Related npm Packages - StepSecurity](https://www.stepsecurity.io/blog/a-mini-shai-hulud-has-appeared)
- [BETA DETECTION: Mini Shai-Hulud C2 and Exfiltration Infrastructure Connection Analytic](https://connect.securonix.com/threat-research-intelligence-62/beta-detection-mini-shai-hulud-c2-and-exfiltration-infrastructure-connection-analytic-312)
- [Cache Poisoning Through pull_request_target: The TanStack Incident - SafeDep](https://safedep.io/tanstack-github-actions-cache-poisoning/)
- [GitHub Actions Security - OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/cheatsheets/GitHub_Actions_Security_Cheat_Sheet.html)
- [Help Us Improve GitHub Actions Cache Isolation · community · Discussion #194493](https://github.com/orgs/community/discussions/194493)
- [Keeping your GitHub Actions and workflows secure Part 1 ...](https://securitylab.github.com/research/github-actions-preventing-pwn-requests/)
- [Mass Supply-Chain Attack Slams npm and PyPi, Hits Mistral AI - GovInfoSecurity](https://www.govinfosecurity.com/mass-supply-chain-attack-slams-npm-pypi-hits-mistral-ai-a-31672)
- [Mini Shai-Hulud Is Back: npm Worm Hits over 160 Packages, including Mistral and Tanstack - Aikido Security](https://www.aikido.dev/blog/mini-shai-hulud-is-back-tanstack-compromised)
- [Mini Shai-Hulud Strikes Again: TanStack + more npm Packages Compromised | Wiz Blog](https://www.wiz.io/blog/mini-shai-hulud-strikes-again-tanstack-more-npm-packages-compromised)
- [Mini Shai-Hulud Worm Compromises TanStack, Mistral AI, Guardrails AI & More Packages](https://thehackernews.com/2026/05/mini-shai-hulud-worm-compromises.html)
- [Mini Shai-Hulud Worm: 170+ npm & PyPI Packages Compromised - Qualysec Technologies](https://qualysec.com/cybersecurity-news/mini-shai-hulud-worm-compromises/)
- [Mini Shai-Hulud npm Supply Chain Worm: TanStack and Multi-Ecosystem Compromise](https://hivepro.com/threat-advisory/mini-shai-hulud-npm-supply-chain-worm-tanstack-and-multi-ecosystem-compromise/?utm_sr=(direct)&utm_cmd=(none)&utm_ccn=(not%20set))
- [Mini Shai-Hulud npm Worm: Dissecting a Multi-Vector Supply Chain ...](https://www.upwind.io/feed/mini-shai-hulud-npm-supply-chain-worm)

<details>
<summary>Voir les 15 sources restantes</summary>

- [Mini Shai-Hulud: Supply Chain Malware Attack | Arctic Wolf](https://arcticwolf.com/resources/blog/mini-shai-hulud-supply-chain-malware-attack/)
- [Mini Shai-Hulud: The NPM Supply Chain Worm Hitting TanStack, Mistral, UiPath, and More - ArmorCode](https://www.armorcode.com/blog/mini-shai-hulud-the-npm-supply-chain-worm-hitting-tanstack-mistral-uipath-and-more)
- [Mini Shai-Hulud: The Self-Replicating npm Worm That Turned Software Development Against Itself | Community - Securonix Connect!](https://connect.securonix.com/topic/show?tid=307&fid=62)
- [Mini Shai-Hulud: The Worm Returns and Goes Public | Akamai](https://www.akamai.com/blog/security-research/mini-shai-hulud-worm-returns-goes-public)
- [Monthly Threat Report: Stay Ahead of Cybersecurity Trends (May 2026) - Hornetsecurity](https://www.hornetsecurity.com/en/blog/monthly-threat-report/)
- [New Actors Deploy Shai-Hulud Clones: TeamPCP Copycats Are Here - OX Security](https://www.ox.security/blog/new-actors-deploy-shai-hulud-clones-teampcp-copycats-are-here/)
- [OpenAI Confirms Breach After TanStack npm Supply Chain Attack Hit Two Employee Devices - Secure.com](https://www.secure.com/news/openai-tanstack-supply-chain-attack)
- [OpenAI Data Breach? No User Info Stolen in Library Attack - The Silicon Review](https://thesiliconreview.com/2026/05/openai-data-breach-no-user-info-stolen-tanstack)
- [OpenAI hit by supply chain attack linked to malicious TanStack packages - Security Affairs](https://securityaffairs.com/192222/hacking/openai-hit-by-supply-chain-attack-linked-to-malicious-tanstack-packages.html)
- [Our response to the TanStack npm supply chain attack | OpenAI](https://openai.com/index/our-response-to-the-tanstack-npm-supply-chain-attack/)
- [Security advisories | Mistral Docs - Mistral AI Documentation](https://docs.mistral.ai/resources/security-advisories)
- [Shai-Hulud Strikes Again | Guardz.com](https://guardz.com/blog/shai-hulud-strikes-again/)
- [Shai-Hulud compromises the @tanstack ecosystem - Endor Labs](https://www.endorlabs.com/learn/shai-hulud-compromises-the-tanstack-ecosystem-80-packages-compromised)
- [TanStack Npm Packages Compromised Inside The Mini Shai Hulud Supply Chain Attack - Osint Advisory IBM X-Force Report](https://exchange.xforce.ibmcloud.com/osint/guid:6f4e76f7af9c49caaff737d8b4a55e55)
- [TanStack Supply Chain Attack Hits Two OpenAI Employee Devices, Forces macOS Updates](https://thehackernews.com/2026/05/tanstack-supply-chain-attack-hits-two.html)

</details>

## Ressources Wet & Sea Tech

**Chaîne YouTube (@discover-allin360) :** https://www.youtube.com/@discover-allin360

**Boutique :** https://wetseatech.etsy.com

**Tous les articles IA & Travail :** https://wst-tech.org/tags/ia-travail/
