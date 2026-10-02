---
title: "watsonx Code Assistant : coder avec l'IA sans exposer votre code"
date: 2026-05-22
slug: "guide-complet-protéger-votre-propriété-intellectuelle-en-2024"
youtube_url: "https://youtu.be/wZWDGa3wVK4"
youtube_video_id: "wZWDGa3wVK4"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "cybersecurity"
categories: ["Cybersécurité"]
tags: ["cybersecurity", "Cybersécurité", "DataSecurity", "DevSecOps", "IBM", "PropriétéIntellectuelle"]
summary: "Les assistants de code IA font gagner du temps, mais peuvent exposer votre code source. Bonnes pratiques et erreurs à éviter avec IBM watsonx Code Assistant."
cover:
  image: "/covers/wZWDGa3wVK4.jpg"
  alt: "watsonx Code Assistant : coder avec l'IA sans exposer votre code"
  caption: "Cybersécurité"
draft: false
catalogue_id: "308d6488"
translationKey: "308d6488"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/wZWDGa3wVK4" title="Voir la vidéo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

IBM watsonx Code Assistant offre des gains de productivité dans le développement logiciel en intégrant l'intelligence artificielle directement dans les environnements de codage. Cependant, cette accélération du cycle de développement introduit des risques de sécurité majeurs : exposition involontaire de code source propriétaire, fuite de secrets d'authentification et transmission de données sensibles vers des serveurs externes. La vidéo documente les mécanismes de protection disponibles — configuration sécurisée, filtrage des suggestions basées sur du code public, responsabilité partagée entre développeur et IBM — et met en évidence les compromis entre efficacité opérationnelle et gouvernance de la propriété intellectuelle. L'enjeu pour les organisations est de mettre en place des garde-fous techniques et procéduraux avant de généraliser ces outils au sein des équipes.

## Principaux points abordés

- **Configuration requise et points d'exposition** : watsonx Code Assistant s'intègre via des extensions VS Code ou Eclipse et nécessite une clé API IBM Cloud. Les logs locaux ne sont pas chiffrés par défaut, créant un vecteur de risque si la machine de développement est compromise.

- **Paramétrage de sécurité critique** : une option de filtrage bloque les suggestions trop proches de code public identifié par analyse de similarité, réduisant les risques de plagiat involontaire ou de réutilisation de dépendances sensibles.

- **Responsabilité partagée dans la chaîne DevSecOps** : IBM s'engage sur la non-réutilisation des données de code des clients pour l'entraînement de modèles, mais les organisations doivent implémenter elles-mêmes les politiques de vérification des artefacts générés et de détection des secrets en amont du commit.

- **Gitleaks et prévention de fuites de secrets** : l'utilisation d'outils comme Gitleaks en pré-commit permet d'identifier et bloquer les clés d'API, tokens et credentials avant qu'ils ne soient saisis dans les suggestions IA ou envoyés dans les dépôts.

- **Conformité réglementaire et architecture multi-couches** : les solutions IBM Cloud Pak for Data implémentent des contrôles de sécurité aux niveaux réseau, compte utilisateur et collaborateurs, essentiels pour respecter GDPR, HIPAA et ISO certifications dans des secteurs hautement régulés.

- **Limite structurelle** : aucun outil IA ne peut garantir une isolation totale du code ; les développeurs restent responsables de la validation manuelle des suggestions avant intégration, particulièrement en présence de données confidentielles ou propriétaires.

## Références (Golden Sources)

- [Announcing IBM Project Bob: Your AI partner for faster, smarter software develop](https://www.ibm.com/new/announcements/ibm-project-bob)
- [Best practices in continuous compliance toolchain - IBM Cloud Docs](https://cloud.ibm.com/docs/devsecops?topic=devsecops-practices-cc-toolchain)
- [Find secrets with Gitleaks - GitHub](https://github.com/gitleaks/gitleaks)
- [IBM watsonx Code Assistant for Z: Installation and Usage](https://www.ibm.com/docs/en/SSK5UBS_2.0/pdf/watsonx_code_assistant_for_z_2.4.20.pdf)
- [IBM's principles of trust and transparency](https://www.ibm.com/policy/trust-transparency)
- [Sécurité pour Cloud Pak for Data as a Service sur IBM Cloud - Docs](https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/security-overview.html?pos=2%3Fcontext%3Dcpdaas&locale=fr&context=cpdaas)
## Chapitres

- `0:00` — Introduction
- `0:32` — Le dilemme développeur
- `1:07` — Risques et précautions
- `1:39` — Configuration sécurisée
- `2:11` — Responsabilité partagée
- `2:43` — Gestion des logs

## Ressources Wet & Sea Tech

**Chaîne YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Boutique :** https://wetseatech.etsy.com

**Tous les articles Cybersécurité :** https://wst-tech.org/tags/cybersecurity/
