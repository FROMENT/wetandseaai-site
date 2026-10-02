---
title: "Déployer une app IA avec Firebase App Hosting et Cloud Run"
date: 2026-05-28
slug: "déploiement-full-stack-avec-firebase-guide-complet-devops-cloud"
youtube_url: "https://youtu.be/hIKA0FIdWlQ"
youtube_video_id: "hIKA0FIdWlQ"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "devops-cloud"
categories: ["DevOps & Cloud"]
tags: ["devops-cloud", "CloudRun", "DevOps", "Firebase", "GoogleCloud", "VertexAI"]
summary: "Firebase App Hosting, Cloud Run, Vertex AI, Cloud Build : comment ces briques s'assemblent pour déployer une app IA full stack ? Architecture et bonnes pratiques DevOps."
cover:
  image: "/covers/hIKA0FIdWlQ.jpg"
  alt: "Déployer une app IA avec Firebase App Hosting et Cloud Run"
  caption: "DevOps & Cloud"
draft: false
catalogue_id: "1586919a"
translationKey: "1586919a"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/hIKA0FIdWlQ" title="Voir la vidéo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

Le déploiement d'applications d'intelligence artificielle sur Google Cloud et Firebase requiert l'orchestration de plusieurs briques technologiques : Firebase App Hosting offre une couche d'abstraction pour les frameworks dynamiques (Next.js, etc.), tandis que Cloud Run fournit l'environnement d'exécution serverless containerisé. Cette architecture décentralisée combine Vertex AI pour l'inférence, Cloud Build pour l'automatisation CI/CD et Secret Manager pour la sécurisation des variables sensibles. Les équipes DevOps doivent évaluer le positionnement stratégique entre hébergement natif (App Hosting) et déploiement conteneurisé (Cloud Run), en tenant compte des contraintes de scalabilité, de latence et de gestion des modèles IA.

## Principaux points abordés

- **Firebase App Hosting versus Hosting classique** : App Hosting cible spécifiquement les applications dynamiques et les frameworks modernes (Next.js, Nuxt, SvelteKit), alors que Hosting traditionnel privilégie le contenu statique. Cette distinction conditionne le choix d'infrastructure et les capacités de déploiement continu.

- **Cloud Run comme socle d'exécution IA** : La plateforme offre un environnement de conteneurs sans état, optimisé pour les workloads d'inférence avec support GPU, permettant le scaling automatique des modèles Gemini ou des pipelines personnalisés via Vertex AI.

- **Pipeline CI/CD avec Cloud Build** : L'intégration native autorise la construction, les tests et le déploiement automatisés depuis les dépôts sources, avec possibilité de sécuriser les identifiants via Secret Manager plutôt que des variables d'environnement en clair.

- **Intégration Firestore et authentification** : Google AI Studio peut être augmentée avec Firestore pour la persistance et Firebase Authentication, créant un écosystème cohérent de données et d'identité sans fragmentation d'outils tiers.

- **Limitation : couplage écosystème Google** : L'approche favorise une dépendance croissante aux services Google Cloud (Vertex AI, Firestore, Secret Manager), réduisant l'interopérabilité avec des stacks multi-cloud ou open source.

- **Enjeu opérationnel de gouvernance des modèles** : La multiplication des points de déploiement (App Hosting, Cloud Run, Vertex AI) complique le suivi des versions de modèles, des coûts d'inférence et de l'audit des requêtes sensibles.

## Références (Golden Sources)

- [App Hosting vs. the original Hosting: Which one do I use? - The Firebase Blog](https://firebase.blog/posts/2024/05/app-hosting-vs-hosting/)
- [Configure and manage App Hosting backends | Firebase App Hosting](https://firebase.google.com/docs/app-hosting/configure)
- [Building an automated serverless deployment pipeline with Cloud Build - Google Cloud](https://cloud.google.com/blog/topics/developers-practitioners/building-automated-serverless-deployment-pipeline-cloud-build)
- [Cloud Run AI Cookbook - Google Cloud Documentation](https://docs.cloud.google.com/run/docs/ai/cookbook)
- [Configure secrets with Secret Manager | Vertex AI - Google Cloud Documentation](https://docs.cloud.google.com/vertex-ai/docs/pipelines/secret-manager)
- [Add Cloud Firestore and Authentication to your Google AI Studio app | Develop with Firebase](https://firebase.google.com/docs/ai-assistance/ai-studio-integration)
## Chapitres

- `0:00` — Introduction Firebase
- `0:33` — Problématique du déploiement moderne
- `1:45` — Firebase App Hosting expliqué
- `2:19` — Architecture dynamique vs statique
- `3:31` — Différences avec hébergement classique

## Ressources Wet & Sea Tech

**Chaîne YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Boutique :** https://wetseatech.etsy.com

**Tous les articles DevOps & Cloud :** https://wst-tech.org/tags/devops-cloud/
