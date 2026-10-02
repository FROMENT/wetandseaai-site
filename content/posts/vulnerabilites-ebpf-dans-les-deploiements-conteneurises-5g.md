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

L'intégration croissante d'eBPF dans les architectures 5G conteneurisées introduit un vecteur d'attaque méconnu : la compromission inter-conteneurs via défaillance d'isolation mémoire. Une étude récente documente comment l'accès direct au kernel par eBPF peut contourner les barrières logiques entre conteneurs colocalisés. Combinée à des expositions classiques comme les sockets Docker non sécurisées et les vulnérabilités runC, cette faille impacte directement la robustesse des cœurs de réseau 5G. Les systèmes ICS/SCADA conteneurisés présentent des risques similaires. Les contre-mesures reposent sur une segmentation stricte (RBAC, namespaces), le durcissement d'images et la vérification d'attestations en continu.

## Principaux points abordés

- **eBPF comme surface d'attaque en 5G** : Les programmes eBPF bénéficiant d'accès kernel pour des raisons de performance réseau créent une faille d'isolation mémoire entre conteneurs voisins, contournant les protections par namespace.

- **Socket Docker exposée : vecteur de persistance** : L'accès non contrôlé à `/var/run/docker.sock` confère des droits root sur l'hôte ; une exposition fréquente dans les architectures cloud-natives faiblement configurées.

- **Chaîne d'exploitation multi-vecteurs** : Une compromission eBPF initiale peut se combiner avec des vulnérabilités runC pour réaliser une évasion de conteneur complète vers l'hôte ou les conteneurs voisins.

- **Criticalité accrue en environnement ICS/SCADA** : Les systèmes de contrôle conteneurisés amplifieront l'impact d'une telle défaillance, passant d'une compromission logique à une dégradation de disponibilité critique.

- **Limite des seuls contrôles d'accès** : RBAC et namespaces seuls ne bloquent pas les attaques eBPF au niveau mémoire ; une approche en couches (image durcies, vérification d'attestations, telémétrie) reste indispensable.

- **Impact opérationnel** : Les équipes DevOps 5G doivent basculer d'un modèle « conteneurs = isolés par défaut » à un modèle « vérification continue de l'intégrité des couches kernel et de l'image ».

## Références (Golden Sources)

- [Vulnerability Analysis of eBPF-enabled Containerized Deployments of 5G Core Networks](https://arxiv.org/pdf/2603.19867)
- [Containerized Security for ICS/SCADA Systems: From PLC Simulation to Kubernetes](https://www.iiis.org/CDs2025/CD2025Summer//papers/SA545CT.pdf)
- [Docker socket security: why /var/run/docker.sock is root access](https://www.netdata.cloud/guides/docker/docker-socket-security/)
- [New runC Vulnerabilities Enable Container Escape](https://orca.security/resources/blog/new-runc-vulnerabilities-allow-container-escape/)
- [Verify a Docker Hardened Image or chart](https://docs.docker.com/dhi/how-to/verify/)
- [CLI Command Reference - checkov](https://www.checkov.io/2.Basics/CLI%20Command%20Reference.html)
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
