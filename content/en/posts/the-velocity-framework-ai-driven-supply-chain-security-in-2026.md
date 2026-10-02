---
title: "Dependency Pinning vs Freshness: Securing Your Software Supply Chain"
date: 2026-09-20
slug: "the-velocity-framework-ai-driven-supply-chain-security-in-2026"
publishDate: "2026-09-28T09:00:00"
youtube_url: "https://youtu.be/B_JSx88HG5k"
youtube_video_id: "B_JSx88HG5k"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "cybersecurity"
categories: ["Cybersécurité"]
tags: ["cybersecurity", "AISecurityRisks", "CICDSecurity", "DevSecOps", "SoftwareSupplyChain", "VulnerabilityManagement"]
summary: "Pin every dependency and your code slowly rots. Update everything and you drown in alerts. Here is the two-speed model that fixes both. 🇫🇷 Version française : https://youtu.be/AlQe-rrPnuE"
cover:
  image: "/covers/B_JSx88HG5k.jpg"
  alt: "Dependency Pinning vs Freshness: Securing Your Software Supply Chain"
  caption: "Cybersécurité"
draft: false
catalogue_id: "6adc89de"
translationKey: "6adc89de"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/B_JSx88HG5k" title="Watch the video" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

Modern software supply chains face a critical tension: strict dependency pinning prevents unexpected breaks but allows security decay, while continuous updates expose teams to alert fatigue and reproducibility loss. The two-speed dependency management model addresses this by separating routine updates from security-critical patches. AI-driven infrastructure code generation and registry flooding with vulnerabilities demand governance structures—SBOMs, provenance verification, and policy-as-code—to maintain both build stability and security posture without sacrificing operational velocity.

## Key Points

- **Pinning creates stability debt**: Locking dependencies to known versions prevents build rot and reproducibility issues, but components age without security updates, accumulating hidden vulnerabilities over time.

- **Freshness measurement via libyears**: The libyear metric quantifies dependency age by counting how many years behind the latest release a component sits; combined with EPSS scores, it enables risk-stratified update scheduling rather than blanket policies.

- **Two-speed update cadence**: Batch routine updates on a cool-down schedule (e.g., monthly) while fast-tracking patches addressing active exploits, detected via Exploit Prediction Scoring System or vulnerability advisories, balances alert fatigue against rapid response.

- **AI agents amplify supply chain risk**: Automated infrastructure code generation now dominates deployments; Sonatype data shows approximately half of AI-generated code contains security flaws by default, requiring upstream policy enforcement and SBOM generation at commit time.

- **Provenance and policy gaps**: SLSA levels, OpenSSF Scorecard, and Open Policy Agent enable control, but governance adoption remains inconsistent; NIST.SP.800-218 and OWASP CI/CD risks outline frameworks, yet manual verification bottlenecks still exist in most teams.

- **Limitation of libyears alone**: Freshness scores ignore severity distribution and false positives in vulnerability databases; complementary signals (EPSS, scorecard checks, transitive dependency risk) are necessary to avoid either premature or delayed patching.

## References (Golden Sources)

- [2026 State of the Software Supply Chain Report | Sonatype](https://www.sonatype.com/state-of-the-software-supply-chain/introduction)
- [AI Agents Are Writing Your Infrastructure Code. Is Anyone Governing It? - DevOps](https://devops.com/ai-agents-are-writing-your-infrastructure-code-is-anyone-governing-it/)
- [Tame Dependabot: Group your updates, slow the cadence, keep security fast - The GitHub Blog](https://github.blog/security/supply-chain-security/tame-dependabot-group-your-updates-slow-the-cadence-keep-security-fast/)
- [Exploit Prediction Scoring System (EPSS)](https://www.first.org/epss/)
- [SLSA • Security levels](https://slsa.dev/spec/v1.0/levels)
- [libyear](https://libyear.com/)
## Chapters

- `0:00` — Introduction & Overview
- `0:34` — Dependency Pinning Explained
- `1:09` — Lib Years & Technical Debt
- `2:16` — Alert Fatigue & Batched Updates
- `2:49` — Cooldown Periods & Grouping
- `3:29` — Critical Vulnerability Fast Track

## Wet & Sea Tech Resources

**YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Shop :** https://wetseatech.etsy.com

**More articles — Cybersecurity :** https://wst-tech.org/tags/cybersecurity/
