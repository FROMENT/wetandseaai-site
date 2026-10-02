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

L'évaluation des modèles de langage repose historiquement sur des approches informelles et fragmentées. Une étude empirique portant sur 57 bancs d'essai d'évaluation et 16 560 incidents GitHub révèle que ces outils produisent systématiquement des scores plausibles mais erronés, compromettant la fiabilité des déploiements en production. La transition vers une ingénierie rigoureuse de l'évaluation s'articule autour de trois éléments critiques : la construction de jeux de données de référence (golden datasets), l'implémentation de pipelines CI/CD strictes pour les systèmes LLM, et l'établissement de traces d'audit traçables pour les agents autonomes. Cette mutation méthodologique s'impose comme prérequis opérationnel pour garantir la conformité réglementaire et la performance prévisible des systèmes d'IA en environnements critiques (finance, conformité, sécurité).

## Principaux points abordés

- **Défaillances silencieuses dans les harnesses d'évaluation** : Les outils d'évaluation actuels présentent des failles structurelles générant des résultats faussement positifs. L'approche "Looks Good To Me" (LGTM) n'offre plus de garantie suffisante pour valider le déploiement de modèles spécialisés.

- **Golden datasets comme fondation du contrôle qualité** : L'établissement de jeux de données curatisés et représentatifs constitue la base d'une évaluation reproductible. Ces ensembles servent de référentiel immuable pour mesurer les régressions et les dérives de performance entre versions.

- **Traçabilité et attribution des erreurs dans les systèmes mémoire** : Les agents autonomes long-running présentent des challenges d'audit irrésolus par audits manuels. L'implémentation de mécanismes de traçabilité permet d'identifier précisément l'origine des défaillances (hallucinations, erreurs d'indexation, dégradation du contexte).

- **Pipelines CI/CD strict pour LLM vs agency**  : La transition du paradigme "LLM agency" (autonomie du modèle) vers "code agency" (autonomie du système de contrôle) implique des mécanismes de validation à chaque étape : scoring local, validation cross-model, gates de conformité automatisés.

- **Limitation : coût de maintenance des golden datasets** : La création et la maintenance de jeux de données de référence représentent un investissement humain significatif, particulièrement dans les domaines spécialisés (finance, santé). L'automatisation partielle via modèles de récompense reste en phase exploratoire.

- **Impact opérationnel en environnements réglementés** : Les institutions financières (HSBC, sandbox HKMA) expérimentent ces frameworks pour valider des modèles spécialisés en détection de fraude et conformité. L'absence de processus d'évaluation rigoureux expose directement à des violations réglementaires et des pertes opérationnelles.

## Références (Golden Sources)

- [Towards Evaluation Engineering: An Empirical Study of ML Evaluation Harnesses in the Wild](https://www.researchgate.net/publication/405263894_Towards_Evaluation_Engineering_An_Empirical_Study_of_ML_Evaluation_Harnesses_in_the_Wild/download)

- [Tracing and Attributing Errors in Large Language Model Memory Systems](https://arxiv.org/html/2605.28732v1)

- [Building a Golden Dataset for Model Evaluation](https://www.twine.net/blog/building-a-golden-dataset-for-model-evaluation/)

- [From production traces to better AI agents: Automating the LLMOps feedback loop](https://arize.com/blog/from-production-traces-to-better-ai-agents-automating-the-llmops-feedback-loop/)

- [Golden datasets: Evaluating fine-tuned large language models](https://sigma.ai/golden-datasets/)

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
