---
title: "Your AI Evals Are Broken: Golden Datasets & Strict LLM CI/CD"
date: 2026-06-06
slug: "leffondrement-de-lévaluation-ia-vers-des-golden-datasets-robustes"
youtube_url: "https://youtu.be/A6_FKm3qxWQ"
youtube_video_id: "A6_FKm3qxWQ"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "prospective"
categories: ["Prospective"]
tags: ["prospective", "DeepEval", "EvaluationIA", "GoldenDataset", "MLOps", "TransformationDigitale"]
summary: "A study of 57 AI evaluation harnesses and 16,560 GitHub issues found that the tools grading your models are often broken. Here's how to build evals you can trust."
cover:
  image: "/covers/A6_FKm3qxWQ.jpg"
  alt: "Your AI Evals Are Broken: Golden Datasets & Strict LLM CI/CD"
  caption: "Prospective"
draft: false
catalogue_id: "d1089859"
translationKey: "d1089859"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/A6_FKm3qxWQ" title="Voir la vidéo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

Les systèmes d'évaluation des modèles de langage présentent des défaillances structurelles massives : une étude empirique de 57 bancs d'essai et 16 560 problèmes GitHub révèle que les outils de notation produisent régulièrement des résultats plausibles mais incorrects. Cette fragmentation évaluative crée un risque opérationnel majeur pour les organisations déployant des agents autonomes en production. La transition vers une ingénierie de l'évaluation systématique — fondée sur des datasets d'or (golden datasets) et des pipelines CI/CD stricts — devient indispensable pour garantir la fiabilité des systèmes critiques, notamment en finance ou en cybersécurité où les hallucinations et erreurs de traçabilité sont inacceptables.

## Principaux points abordés

- **Défaillances silencieuses des harnesses d'évaluation** — Les métriques courantes (BLEU, ROUGE) produisent des scores validant des réponses techniquement fausses, particulièrement lorsque les modèles génèrent du contenu syntaxiquement correct mais sémantiquement erroné. Cette limite s'accentue avec les agents mémoire de longue durée, impossibles à auditer manuellement à l'échelle.

- **Construction de datasets d'or comme fondation évaluative** — Les organisations (HSBC, secteur financier) structurent des ensembles de test annotés manuellement, validés en environnement contrôlé, pour isoler la performance réelle des modèles spécialisés. Cette approche exige une curatelle rigoureuse et une mise à jour itérative basée sur les cas d'échec en production.

- **Pipeline CI/CD en couches pour les LLM** — Une architecture multi-niveaux combine tests unitaires (conformité des sorties), intégration (cohérence agent-code), et déploiement progressif avec golden datasets comme référentiel de vérité. DeepEval 4.0 et outils similaires automatisent cette validation.

- **Transition du "LLM agency" au "code agency"** — Le paradigme évolue : au lieu de déléguer la logique métier au modèle (approche fragile), les LLM sont confinés à des tâches discrètes, validées par des couches de code déterministe. Cette réduction du champ d'agentivité améliore la traçabilité et la reproductibilité.

- **Traçabilité et attribution des erreurs** — L'identification précise des sources de défaillance (hallucination du modèle, bogue d'intégration, instabilité de la mémoire) nécessite une instrumentation complète des systèmes et une cartographie des dépendances. Les systèmes mémoire long-terme rendent cette traçabilité critique mais techniquement complexe.

- **Limite : coût d'adoption et expertise requise** — La construction et la maintenance de golden datasets exigent une expertise en annotation, une gouvernance stricte, et des ressources significatives. Les petites équipes DevOps risquent de repousser cette rigueur, prolongeant la phase dangereuse du déploiement sans évaluation fiable.

## Références (Golden Sources)

- [Towards Evaluation Engineering: An Empirical Study of ML Evaluation Harnesses in the Wild](https://www.researchgate.net/publication/405263894_Towards_Evaluation_Engineering_An_Empirical_Study_of_ML_Evaluation_Harnesses_in_the_Wild/download)
- [Building a Golden Dataset for Model Evaluation](https://www.twine.net/blog/building-a-golden-dataset-for-model-evaluation/)
- [Building a "Golden Dataset" for AI Evaluation: A Step-by-Step Guide](https://www.getmaxim.ai/articles/building-a-golden-dataset-for-ai-evaluation-a-step-by-step-guide/)
- [Tracing and Attributing Errors in Large Language Model Memory Systems](https://arxiv.org/html/2605.28732v1)
- [From production traces to better AI agents: Automating the LLMOps feedback loop](https://arize.com/blog/from-production-traces-to-better-ai-agents-automating-the-llmops-feedback-loop/)
- [HKMA GenAI Sandbox Use Cases Summary](https://www.about.hsbc.com.hk/-/media/hong-kong/en/news-and-media/251024-hsbc-hkma-genai-sandbox-use-cases-summary.pdf?sc_lang=en-GB)
## Chapitres

- `0:00` — Introduction et contexte
- `1:07` — Fin du développement LGTM
- `2:15` — Vers des pipelines automatisés
- `2:48` — Effondrement de l'infrastructure d'évaluation
- `6:30` — Pièges des traces mémoire
- `7:30` — CI/CD strict pour les LLMs
- `8:15` — L'ère des agents de code

## Ressources Wet & Sea Tech

**Chaîne YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Boutique :** https://wetseatech.etsy.com

**Tous les articles Prospective :** https://wst-tech.org/tags/prospective/
