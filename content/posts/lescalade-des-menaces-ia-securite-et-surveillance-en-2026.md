---
title: "IA agentique : empoisonnement de données et attaque TeamPCP décryptés"
date: 2026-05-21
slug: "lescalade-des-menaces-ia-sécurité-et-surveillance-en-2026"
youtube_url: "https://youtu.be/DjvfDzHT3RQ"
youtube_video_id: "DjvfDzHT3RQ"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "prospective"
categories: ["Prospective"]
tags: ["prospective", "CyberMenaces", "CybersécuritéIA", "IA2026", "SécuritéNumérique", "TransformationDigitale"]
summary: "Un scanner de sécurité piraté, puis LiteLLM compromis en 8 jours : les clés API de plus de 100 fournisseurs d'IA en jeu. Les nouvelles surfaces d'attaque de l'IA agentique."
cover:
  image: "/covers/DjvfDzHT3RQ.jpg"
  alt: "IA agentique : empoisonnement de données et attaque TeamPCP décryptés"
  caption: "Prospective"
draft: false
catalogue_id: "648b6a48"
translationKey: "648b6a48"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/DjvfDzHT3RQ" title="Voir la vidéo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

L'IA agentique — où les modèles exécutent des actions autonomes sur les systèmes d'information — introduit une nouvelle classe de surfaces d'attaque. Au-delà des risques classiques de sécurité des modèles, les agents opérationnels font face à des vulnérabilités d'empoisonnement de données à chaque étape du cycle de vie, ainsi qu'aux attaques en cascade au sein des chaînes d'approvisionnement logicielles. L'incident TeamPCP de mars 2026, qui a compris le compromis de Trivy puis de LiteLLM en huit jours, a exposé les clés API de plus de 100 fournisseurs d'IA. Parallèlement, les évaluations de sécurité industrielle révèlent un écart structurel entre l'accélération des capacités d'IA et la mise en œuvre de cadres de conformité crédibles. Cette prospective examine les vecteurs d'attaque émergents et les implications de gouvernance associées.

## Principaux points abordés

- **Empoisonnement de données en environnement agentique** : contrairement aux modèles statelesss, les agents agentiques intègrent des boucles d'apprentissage et d'exécution continus, multipliant les points d'injection de données malveillantes (données d'entraînement, requêtes d'utilisateurs, sorties de systèmes externes).

- **Attaque en cascade TeamPCP (mars 2026)** : compromission initiale d'un scanner de sécurité (Trivy), exploitation pour accéder à LiteLLM en huit jours, exposition subséquente des credentials API de plus de 100 fournisseurs d'IA—démonstration que les outils de sécurité eux-mêmes forment des maillons faibles dans la chaîne de confiance.

- **Souveraineté des modèles vs. dépendance API** : les organisations font face à un dilemme entre auto-hébergement (overhead opérationnel et risque de misconfiguration) et délégation à des API distantes (dépendance à des tiers et perte de contrôle des données).

- **Évolution du Top 10 OWASP pour LLM** : mise à jour 2025 intégrant les vecteurs d'attaque spécifiques à l'IA agentique, incluant les injections de prompts indirectes, le détournement d'outils et les exfiltrations de données via les sorties du modèle.

- **Insuffisance des cadres de conformité** : l'AI Safety Index révèle un écart significatif entre l'ambition technologique des entreprises leaders et l'implémentation effective de mécanismes de vérification, audit et isolation des données sensibles.

- **Limite de détection** : les architectures de vérification comme SeGaDev (fingerprinting cryptographique des communications matérielles) restent au stade de propositions conceptuelles et ne s'appliquent pas aux exfiltrations logiques au niveau applicatif ou API.

- **Impact opérationnel** : les équipes DevOps et de cybersécurité doivent redéfinir les chaînes de confiance autour des agents IA, impliquant la segmentation réseau, la rotation des credentials, et l'audit des flux de données en temps réel.

## Références (Golden Sources)

- [TeamPCP and the Cascading AI/ML Supply Chain Campaign - Lab Space](https://labs.cloudsecurityalliance.org/wp-content/uploads/2026/03/CSA_research_note_ai_pypi_supply_chain_campaign_20260329-csa-styled.pdf)

- [Introduction to Data Poisoning: A 2026 Perspective | Lakera – Protecting AI team](https://www.lakera.ai/blog/training-data-poisoning)

- [OWASP Top 10 for LLMs 2025: Key Risks and Mitigation Strategies - Invicti](https://www.invicti.com/blog/web-security/owasp-top-10-risks-llm-security-2025)

- [Fingerprinting All AI Cluster I/O Without Mutually Trusted Processors](https://aigi.ox.ac.uk/wp-content/uploads/2026/04/Fingerprinting_All_AI_Cluster_IO.pdf)

- [AI Safety Index - Future of Life Institute](https://futureoflife.org/wp-content/uploads/2025/12/AI-Safety-Index-Report_131225_Full_Report_Digital.pdf)

- [From Stateless Queries to Autonomous Actions: A Layered Security Framework for A](https://arxiv.org/pdf/2604.23338)
## Chapitres

- `0:00` — Introduction
- `0:31` — Défenses cybersécurité dépassées
- `1:44` — Programme détaillé
- `2:17` — IA agentique moderne
- `3:30` — Évolution modèles langage

## Ressources Wet & Sea Tech

**Chaîne YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Boutique :** https://wetseatech.etsy.com

**Tous les articles Prospective :** https://wst-tech.org/tags/prospective/
