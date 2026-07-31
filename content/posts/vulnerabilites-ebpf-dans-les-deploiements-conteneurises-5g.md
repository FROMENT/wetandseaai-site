---
title: "Vulnérabilités eBPF dans les déploiements conteneurisés 5G"
date: 2026-05-28
publishDate: "2026-05-30T09:00:00"
youtube_url: "https://youtu.be/2nfiZZwFpNg"
youtube_video_id: "2nfiZZwFpNg"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "cybersecurity"
categories: ["Cybersécurité"]
tags: ["cybersecurity"]
summary: "🔐 Les déploiements conteneurisés des réseaux cœur 5G exposent de nouvelles vulnérabilités critiques via eBPF qui menacent la sécurité des infrastructures télécom."
cover:
  image: "/covers/2nfiZZwFpNg.jpg"
  alt: "Vulnérabilités eBPF dans les déploiements conteneurisés 5G"
  caption: "Cybersécurité"
draft: false
catalogue_id: "b2a3f893"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/2nfiZZwFpNg" title="Voir la vidéo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

Les déploiements conteneurisés des réseaux cœur 5G intègrent eBPF (Extended Berkeley Packet Filter) comme mécanisme de monitoring et de sécurité au niveau du noyau. Cette intégration expose une surface d'attaque nouvelle : les vulnérabilités eBPF peuvent contourner les isolations de conteneurs Kubernetes et Docker, permettant une escalade de privilèges vers l'hôte physique. L'analyse porte sur l'intersection critique entre trois domaines : les systèmes ICS/SCADA conteneurisés, les failles d'architecture des environnements Kubernetes, et les vecteurs d'exploitation via les sockets Docker non sécurisés. Les opérateurs télécom doivent adapter leurs stratégies de segmentation réseau et de contrôle d'accès pour anticiper ces risques avant leur exploitation en production.

## Principaux points abordés

- **eBPF comme surface d'attaque dans les architectures 5G** — eBPF s'exécute en mode noyau avec accès direct à la mémoire physique ; les vulnérabilités eBPF en environnement conteneurisé permettent de contourner les namespaces Linux et les cgroups, élément critique pour les réseaux cœur où l'isolation des fonctions VNF (Virtual Network Functions) repose sur ces mécanismes.

- **Vulnérabilités structurelles des sockets Docker** — L'accès non restreint à `/var/run/docker.sock` depuis un conteneur compromis équivaut à un accès root sur l'hôte ; cette faille affecte directement les déploiements ICS/SCADA conteneurisés où les systèmes de contrôle critique coexistent avec des charges de travail moins fiabilisées.

- **Escalade de privilèges via runc et CRI** — Les vulnérabilités dans runc (Container Runtime Interface) peuvent être enchaînées avec les expositions eBPF pour échapper au contexte conteneurisé ; cet enchaînement est particulièrement grave en environnement 5G où plusieurs conteneurs exécutent des fonctions interdépendantes (AMF, SMF, UPF).

- **RBAC et segmentation par namespaces : protection insuffisante contre eBPF** — Bien que le contrôle d'accès basé sur les rôles et la segmentation réseau Kubernetes limitent la mobilité latérale, elles ne neutralisent pas les exploit eBPF ; cet écart entre les contrôles applicatifs et les vulnérabilités noyau crée un déficit de sécurité dans les architectures actuelles.

- **Impact opérationnel critique** — Les opérateurs doivent implémenter une défense en profondeur combinant : durcissement d'images (image scanning avec Trivy, Grype, Checkov), attestations de signature Docker, telemetry continue du noyau via eBPF même, et segmentation réseau stricte entre les domaines ICS et les composants 5G non critiques.

## Références (Golden Sources)

- [Containerized Security for ICS/SCADA Systems: From PLC Simulation to Kubernetes](https://www.iiis.org/CDs2025/CD2025Summer//papers/SA545CT.pdf)

- [Docker socket security: why /var/run/docker.sock is root access | Netdata](https://www.netdata.cloud/guides/docker/docker-socket-security/)

- [New runC Vulnerabilities Enable Container Escape | Orca Security](https://orca.security/resources/blog/new-runc-vulnerabilities-allow-container-escape/)

- [Vulnerability Analysis of eBPF-enabled Containerized Deployments of 5G Core Netw](https://arxiv.org/pdf/2603.19867)

- [CLI Command Reference - checkov](https://www.checkov.io/2.Basics/CLI%20Command%20Reference.html)

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
