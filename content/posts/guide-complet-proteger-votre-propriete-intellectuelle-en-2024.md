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

Les assistants de code alimentés par l'IA offrent des gains de productivité significatifs, mais leur utilisation expose des risques de sécurité majeurs pour la propriété intellectuelle et la confidentialité du code source. IBM watsonx Code Assistant adresse ce dilemme en intégrant des mécanismes de protection au niveau architectural : isolation des données, contrôles de transmission, et configuration locale des logs non chiffrés. La vidéo explore le modèle de responsabilité partagée entre fournisseur et client, les paramètres de filtrage des suggestions (notamment le blocage du code public similaire), et les engagements contractuels d'IBM concernant la rétention et l'utilisation des données. Cette approche illustre l'évolution des meilleures pratiques en DevSecOps pour concilier efficacité développeur et gouvernance de sécurité.

## Principaux points abordés

- **Configuration sécurisée d'un assistant IA** : installation via extension VS Code ou Eclipse, authentification par clé API IBM Cloud, et isolation de l'environnement d'exécution pour limiter les fuites de données
- **Modèle de responsabilité partagée** : IBM gère la sécurité de l'infrastructure cloud, tandis que le client conserve la propriété des données générées et des insights IA
- **Gestion des logs et chiffrement** : les logs sont stockés localement en clair, imposant au client un contrôle strict de la conformité locale (GDPR, HIPAA)
- **Filtrage intelligent des suggestions** : paramètre de configuration permettant de bloquer les suggestions similaires à du code public, réduisant le risque de contamination involontaire
- **Engagements contractuels et transparence** : IBM détaille les conditions d'utilisation, les normes de conformité globale (GDPR, ISO, HIPAA), et la non-utilisation du code client pour l'entraînement de modèles
- **Limitation opérationnelle** : l'absence de chiffrement natif des logs exige une gestion manuelle de la confidentialité, déléguant la responsabilité au client plutôt que de la centraliser architecturalement

## Références (Golden Sources)

- [IBM watsonx Code Assistant for Z: Installation and Usage](https://www.ibm.com/docs/en/SSK5UBS_2.0/pdf/watsonx_code_assistant_for_z_2.4.20.pdf)
- [Best practices in continuous compliance toolchain - IBM Cloud Docs](https://cloud.ibm.com/docs/devsecops?topic=devsecops-practices-cc-toolchain)
- [IBM's principles of trust and transparency](https://www.ibm.com/policy/trust-transparency)
- [Find secrets with Gitleaks - GitHub](https://github.com/gitleaks/gitleaks)
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
