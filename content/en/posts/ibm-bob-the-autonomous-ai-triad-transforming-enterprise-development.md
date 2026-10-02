---
title: "IBM Bob, Claude Code & nono: 3 Layers to Secure AI Coding Agents"
date: 2026-09-07
slug: "ibm-bob-the-autonomous-ai-triad-transforming-enterprise-development"
youtube_url: "https://youtu.be/qdf1E_v5JQo"
youtube_video_id: "qdf1E_v5JQo"
youtube_channel: "B"
youtube_channel_handle: "@wetseatech"
youtube_channel_url: "https://www.youtube.com/@wetseatech"
youtube_channel_name: "Wet & Sea Tech"
theme: "ia-travail"
categories: ["IA & Travail"]
tags: ["ia-travail", "AIAgents", "EnterpriseAI", "IBMBob", "LegacyModernization", "SoftwareDevelopment"]
summary: "What happens when an AI coding agent finds an AWS key in plain text? Bob governs, Claude Code executes, nono contains: why you need all three. 🇫🇷 Version française : https://youtu.be/HfjJLktQSNE"
cover:
  image: "/covers/qdf1E_v5JQo.jpg"
  alt: "IBM Bob, Claude Code & nono: 3 Layers to Secure AI Coding Agents"
  caption: "IA & Travail"
draft: false
catalogue_id: "1637e3ba"
translationKey: "793aec8b"
---

<div class="video-embed" style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;margin:1.5em 0">
  <iframe src="https://www.youtube.com/embed/qdf1E_v5JQo" title="Watch the video" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%"></iframe>
</div>

## Executive Summary

AI coding agents executing in terminal environments inherit unrestricted access to sensitive credentials—SSH keys, cloud tokens, administrative directories—by default. This video examines the three-layer security model addressing this risk: Claude Code as the execution layer prioritizing developer velocity, nono as kernel-level containment using Landlock (Linux) and Seatbelt (macOS) sandboxing, and IBM Bob as the governance orchestration platform enforcing policy, audit trails, and request routing. The layered approach reflects enterprise requirements to balance automation gains against credential exposure and unauthorized infrastructure access during AI-assisted development workflows.

## Key Points

- **Claude Code execution risk**: AI coding agents running terminal commands inherit full user permissions, creating exposure vectors for leaked credentials and unauthorized access to protected resources without explicit containment mechanisms.

- **Kernel-level sandboxing with nono**: Open-source sandbox framework implements OS-level isolation (Landlock on Linux, Seatbelt on macOS) to restrict file system and network access from agentic processes, preventing credential exfiltration at the kernel boundary.

- **IBM Bob governance layer**: Enterprise platform orchestrates multi-agent workflows with integrated policy enforcement, audit logging of all agentic actions, and cost optimization—enabling legacy modernization (Java, COBOL systems) while maintaining compliance and traceability across development lifecycle.

- **Absence of single-layer sufficiency**: Neither velocity (Claude Code alone), nor containment (nono in isolation), nor governance (Bob without runtime isolation) adequately addresses the complete threat model—all three layers operate in complementary rather than redundant fashion.

- **Operational tradeoff**: Comprehensive sandboxing reduces agent flexibility and may require architecture changes to OpenShift/container deployments; governance overhead increases with audit scope, demanding infrastructure investment proportional to deployment scale and regulatory requirements.

## References (Golden Sources)

- [AI coding agent | IBM](https://www.ibm.com/products/ai-coding-agent)
- [From 'oh no' to nono - building apps on OpenShift with nono and Claude Code](https://www.stb.id.au/blog/openshift-claude-nono)
- [Introducing nono: A Secure Sandbox for AI Agents](https://huggingface.co/blog/lukehinds/nono-agent-sandbox)
- [IBM Bob: Enterprise AI Coding Assistant Complete Guide (2026) | WOWHOW](https://wowhow.cloud/blogs/ibm-bob-enterprise-ai-coding-assistant-complete-guide-2026)
- [Overview - Claude Code Docs](https://docs.claude.com/en/docs/claude-code/overview)
## Wet & Sea Tech Resources

**YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Shop :** https://wetseatech.etsy.com

**More articles — AI & Work :** https://wst-tech.org/tags/ia-travail/
