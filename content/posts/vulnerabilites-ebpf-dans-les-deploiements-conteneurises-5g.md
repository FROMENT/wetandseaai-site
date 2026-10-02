---
title: "eBPF et 5G : comment un conteneur peut compromettre ses voisins"
date: 2026-05-28
slug: "vulnérabilités-ebpf-dans-les-déploiements-conteneurisés-5g"
youtube_url: "https://youtu.be/2nfiZZwFpNg"
youtube_video_id: "2nfiZZwFpNg"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "cybersecurity"
categories: ["Cybersécurité"]
tags: ["cybersecurity", "CybersecuritéConteneurs", "InfrastructureCritique", "Sécurité5G", "VulnérabilitésDocker", "eBPF"]
summary: "Dans un cœur de réseau 5G conteneurisé, eBPF peut devenir la porte qui casse l'isolation entre conteneurs. Mécanismes, exploitation et contre-mesures."
cover:
  image: "/covers/2nfiZZwFpNg.jpg"
  alt: "eBPF et 5G : comment un conteneur peut compromettre ses voisins"
  caption: "Cybersécurité"
draft: false
catalogue_id: "b2a3f893"
translationKey: "b2a3f893"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/2nfiZZwFpNg" title="Voir la vidéo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

L'intégration d'eBPF dans les architectures 5G conteneurisées introduit un vecteur d'attaque critique : l'isolation mémoire insuffisante entre conteneurs colocalisés permet une compromission inter-conteneurs exploitant les privilèges kernel d'eBPF. Ce risque s'intensifie avec les vecteurs adjacents — sockets Docker exposées, vulnérabilités runC, systèmes ICS/SCADA conteneurisés — où une unique défaillance d'isolation offre au attaquant un accès latéral au cœur de réseau ou à l'infrastructure critique. Les contre-mesures reposent sur une triple approche : segmentation logique (RBAC, namespaces), validation d'intégrité des images et télémétrie continue pour détecter les écarts d'exécution.

## Principaux points abordés

- **Mécanisme d'exploitation eBPF** : Les programmes eBPF s'exécutent en kernel space avec accès direct à la mémoire; l'absence de cloisonnement strict entre conteneurs colocalisés permet de franchir les frontières logiques et d'accéder aux données ou d'exécuter du code dans le contexte d'un conteneur voisin.

- **Sockets Docker et accès root implicite** : L'exposition de `/var/run/docker.sock` sur le système hôte confère un accès administrateur au démon Docker; tout conteneur obtenant ce socket acquiert la capacité de piloter l'infrastructure conteneurisée entière, court-circuitant l'isolation.

- **Vulnérabilités runC et évasion conteneur** : Les défauts de sécurité identifiés dans runC permettent à un attaquant privilégié au sein d'un conteneur de rompre l'isolation du runtime et d'accéder au système hôte; les cœurs 5G et systèmes ICS/SCADA conteneurisés demeurent particulièrement exposés faute de mises à jour régulières.

- **Insuffisance des configurations par défaut** : Les déploiements Kubernetes et Docker tirent rarement parti des capacités de segmentation avancées (namespaces, AppArmor, SELinux); cette configuration minimale crée des zones grises où les privilèges kernel et l'accès mémoire restent insuffisamment cloisonnés.

- **Riposte multi-couches requise** : Le durcissement doit combiner le contrôle d'accès basé sur les rôles (RBAC), l'isolation par namespaces au niveau kernel, la vérification d'intégrité des images (signatures d'attestation) et la surveillance active des anomalies d'exécution pour valider la chaîne de construction.

## Références (Golden Sources)

- [Vulnerability Analysis of eBPF-enabled Containerized Deployments of 5G Core Network](https://arxiv.org/pdf/2603.19867)
- [Containerized Security for ICS/SCADA Systems: From PLC Simulation to Kubernetes](https://www.iiis.org/CDs2025/CD2025Summer//papers/SA545CT.pdf)
- [Docker socket security: why /var/run/docker.sock is root access](https://www.netdata.cloud/guides/docker/docker-socket-security/)
- [New runC Vulnerabilities Enable Container Escape](https://orca.security/resources/blog/new-runc-vulnerabilities-allow-container-escape/)
- [Verify a Docker Hardened Image or chart](https://docs.docker.com/dhi/how-to/verify/)
## Chapitres

- `0:00` — Introduction
- `0:37` — Mécanismes techniques eBPF
- `1:13` — Infrastructure 5G conteneurisée
- `1:50` — Défaillance isolation mémoire
- `2:25` — Exploitation inter-conteneurs

## Ressources Wet & Sea Tech

**Chaîne YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Boutique :** https://wetseatech.etsy.com

**Tous les articles Cybersécurité :** https://wst-tech.org/tags/cybersecurity/
