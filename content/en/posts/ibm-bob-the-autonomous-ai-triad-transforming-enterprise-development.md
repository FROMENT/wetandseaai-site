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

AI coding agents operating in enterprise environments inherit full system permissions by default—SSH keys, cloud credentials, and administrative access are all exposed to the agent's execution context. This architectural vulnerability requires a layered security model. IBM Bob addresses governance and policy enforcement at the orchestration level, Claude Code provides the coding execution velocity, and nono introduces kernel-level process isolation to contain agent actions within restricted filesystem and capability boundaries. The three-layer approach—governance, execution, and containment—represents the operational necessity for deploying autonomous coding agents in production environments without catastrophic credential exposure or lateral movement risk.

## Key Points

- **Credential exposure at execution**: AI coding agents running in local terminals inherit parent process permissions, including SSH keys, AWS/Azure tokens, and environment variables, creating a direct attack surface if the agent or its dependencies are compromised.

- **IBM Bob governance layer**: Routes agentic requests through policy engines, enforces approval workflows, maintains immutable audit trails, and orchestrates specialized model routing for different development tasks—from greenfield feature development to legacy modernization (Java, COBOL).

- **Claude Code execution velocity**: Optimized for inline code generation and terminal execution; trades off isolation for development speed. Without containment, this velocity becomes a liability when handling untrusted input or executing in permissioned environments.

- **nono kernel-level isolation**: Implements Landlock-based sandboxing on Linux and Seatbelt confinement on macOS, restricting filesystem access, network egress, and system capabilities at the OS level. Operates independently of application-layer controls.

- **Layering complexity trade-off**: Stacking governance, execution, and containment layers introduces operational overhead (policy configuration, audit log management, sandbox rule tuning) versus monolithic "all-or-nothing" agent deployment. Enterprises must balance security hardening against DevOps velocity.

- **Audit trail continuity**: Multi-layer architectures create distributed logging surfaces; maintaining correlatable audit trails across Bob's governance decisions, Claude Code's execution logs, and nono's syscall interception requires centralized observability infrastructure.

## References (Golden Sources)

- [AI coding agent | IBM](https://www.ibm.com/products/ai-coding-agent)
- [Introducing nono: A Secure Sandbox for AI Agents](https://huggingface.co/blog/lukehinds/nono-agent-sandbox)
- [From 'oh no' to nono - building apps on OpenShift with nono and Claude Code](https://www.stb.id.au/blog/openshift-claude-nono)
- [IBM Bob Takes AI Coding Assistants to the Next Level - DevOps.com](https://devops.com/ibm-bob-takes-ai-coding-assistants-to-the-next-level/)
- [Overview - Claude Code Docs](https://docs.claude.com/en/docs/claude-code/overview)
## Wet & Sea Tech Resources

**YouTube (@wetseatech) :** https://www.youtube.com/@wetseatech

**Shop :** https://wetseatech.etsy.com

**More articles — AI & Work :** https://wst-tech.org/tags/ia-travail/
