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

Le déploiement d'applications d'IA modernes nécessite une orchestration précise entre plusieurs composants Google Cloud : Firebase App Hosting offre une couche d'abstraction pour les frameworks dynamiques (Next.js, React), tandis que Cloud Run assure l'exécution serverless de conteneurs. Cette architecture découple l'infrastructure statique de la logique métier exécutée sur GPU ou CPU selon les besoins. La vidéo traite de l'assemblage fonctionnel de ces briques — intégration Vertex AI pour l'inférence, pipeline CI/CD via Cloud Build, et gestion des secrets — essentiel pour les équipes DevOps gérant des workloads IA en production. L'enjeu principal réside dans la configuration sécurisée et la scalabilité des déploiements sans surcoût d'infrastructure.

## Principaux points abordés

- **Firebase App Hosting vs. Hosting classique** : App Hosting supporte les frameworks fullstack avec backend dynamique intégré, contrairement à l'offre Hosting historique limitée au contenu statique et aux fonctions Cloud de seconde génération. Cette distinction détermine le choix architectural pour une application IA interactive.

- **Séparation frontend/backend et orchestration** : le frontend (Next.js, React) s'exécute sur App Hosting tandis que les modèles IA et traitements intensifs délégués à Cloud Run offrent isolation des ressources et facturation décorrélée de la complexité côté client.

- **Intégration Vertex AI et inférence** : la plateforme Vertex AI fournit les modèles entraînés et l'inférence ; Cloud Run invoque ces services via API REST/gRPC, permettant l'implémentation de patterns comme Retrieval-Augmented Generation (RAG) sans gérer les serveurs de modèles.

- **Pipeline CI/CD sécurisé avec Cloud Build** : automatisation du build, test et déploiement depuis un dépôt Git ; Secret Manager stocke les variables sensibles (clés API, tokens d'authentification) en dehors du code, injecées au runtime dans l'environnement de conteneur.

- **Coûts et gouvernance** : Firebase App Hosting facture à l'usage (requêtes dynamiques), Cloud Run facture au temps d'exécution (100 ms minimum). L'absence de serveur dédié réduit les dépenses idle, mais demande une tuning fin du provisioning et de la mémoire allouée pour éviter les dépassements lors de pics d'inférence.

- **Limite : complexité d'observabilité** : l'architecture distribuée requiert une instrumentation coordonnée (Cloud Logging, Cloud Trace) ; les dépannages de latence IA impliquent de croiser les traces de plusieurs services. Vertex AI et Cloud Run offrent des métriques natives, mais l'absence d'APM unifié peut compliquer le diagnostique en production.

## Références (Golden Sources)

- [App Hosting vs. the original Hosting: Which one do I use? - The Firebase Blog](https://firebase.blog/posts/2024/05/app-hosting-vs-hosting/)
- [Configure and manage App Hosting backends | Firebase App Hosting](https://firebase.google.com/docs/app-hosting/configure)
- [Cloud Run AI Cookbook - Google Cloud Documentation](https://docs.cloud.google.com/run/docs/ai/cookbook)
- [Building an automated serverless deployment pipeline with Cloud Build - Google Cloud](https://cloud.google.com/blog/topics/developers-practitioners/building-automated-serverless-deployment-pipeline-cloud-build)
- [Configure secrets with Secret Manager | Vertex AI - Google Cloud Documentation](https://docs.cloud.google.com/vertex-ai/docs/pipelines/secret-manager)
- [Cloud Build serverless CI/CD platform | Google Cloud](https://cloud.google.com/build)
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
