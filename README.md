# WST — Wet & Sea Tech — Site

Site compagnon des chaînes YouTube [@wetseatech](https://www.youtube.com/@wetseatech) (Cyber/DevOps)
et [@discover-allin360](https://www.youtube.com/@discover-allin360) (IA & Travail).
Articles auto-générés depuis le pipeline vidéo `~/Documents/Media/Videos/_cowork/`.

**URL prod** : https://wst-tech.org
**URL staging Cloudflare** : https://wetandseaai-site.pascal-froment.workers.dev

---

## Stack

| Composant | Détail |
|---|---|
| Générateur | Hugo `0.164.0+extended` (binaire unique, Go) |
| Thème | [PaperMod](https://github.com/adityatelange/hugo-PaperMod) (submodule Git) |
| Hébergement | Cloudflare Workers + Static Assets |
| Build CI | Cloudflare automatique sur `git push origin main` |
| Domaine | `wst-tech.org` |
| Repo | https://github.com/FROMENT/wetandseaai-site |

---

## Setup local

Cloner avec submodule (theme PaperMod) :

```bash
git clone --recursive https://github.com/FROMENT/wetandseaai-site.git ~/Sites/wetandseaai-site
cd ~/Sites/wetandseaai-site
```

Si déjà cloné sans `--recursive` :

```bash
git submodule update --init --recursive
```

Installer Hugo et Node 20+ (Wrangler requirement) :

```bash
brew install hugo node@20
export PATH="/opt/homebrew/opt/node@20/bin:$PATH"
hugo version           # 0.160.1 ou plus récent
node --version         # v20.x.x
```

Preview locale :

```bash
hugo server            # http://localhost:1313
```

Build production :

```bash
hugo --gc --minify     # génère ./public/
```

---

## Configuration Hugo

Tout dans `hugo.yaml` :

| Paramètre | Valeur |
|---|---|
| `baseURL` | `https://wst-tech.org/` (URL canonique pour SEO/RSS/og) |
| `defaultContentLanguage` | `fr` |
| `theme` | `PaperMod` |
| `permalinks.posts` | `/:year/:month/:slug/` |
| Multilangue | FR (`content/posts/`) + EN (`content/en/posts/`) |
| Output formats | HTML, RSS, JSON (recherche client-side) |

---

## Configuration Cloudflare

`wrangler.toml` à la racine :

```toml
name = "wetandseaai-site"
compatibility_date = "2025-04-01"

[assets]
directory = "./public"
not_found_handling = "404-page"
```

Variables d'environnement build (à définir dans le dashboard Cloudflare) :

| Nom | Valeur |
|---|---|
| `HUGO_VERSION` | `0.160.1` |

---

## Workflow publication

### 1. Génération depuis le pipeline vidéo

Les articles sont générés automatiquement depuis `catalogue.json` du pipeline vidéo :

```bash
cd ~/Documents/Media/Videos
python3 ./_cowork/article_publish.py --filter <id>     # un article
python3 ./_cowork/article_publish.py --all             # tous (hors private_duplicate)
```

L'output est écrit dans `~/Sites/wetandseaai-site/content/posts/<slug>.md` (FR)
ou `content/en/posts/<slug>.md` (EN selon `video_language`).

Les fichiers générés sont en `chmod 444` (read-only) pour éviter
qu'un éditeur Markdown auto-format casse le YAML frontmatter.

### 2. Commit + push

```bash
cd ~/Sites/wetandseaai-site
git add -A
git commit -m "publish: <description>"
git push origin main
```

### 3. Déploiement automatique

Cloudflare détecte le push et déclenche un build :

```
1. Clone repo
2. Installe Hugo 0.160.1
3. Exécute `hugo --gc --minify` → génère public/
4. Exécute `npx wrangler deploy` → upload public/ vers edge
5. Site live en ~30 secondes
```

### 4. Déploiement manuel via Wrangler CLI

Pour un deploy direct sans passer par Git :

```bash
hugo --gc --minify
npx wrangler deploy
```

---

## Structure du repo

```
wetandseaai-site/
├── hugo.yaml              # Configuration Hugo
├── wrangler.toml          # Configuration Cloudflare Workers
├── .editorconfig          # Anti-auto-format pour Hugo MD
├── .vscode/
│   └── settings.json      # VSCode workspace : désactive auto-format MD
├── archetypes/
│   └── default.md         # Template par défaut
├── content/
│   ├── about/             # Page À propos
│   ├── posts/             # Articles FR (générés)
│   └── en/posts/          # Articles EN (générés)
├── data/
├── layouts/partials/      # Overrides PaperMod si besoin
├── static/
│   ├── covers/            # (vide — covers servies via img.youtube.com)
│   └── uploads/
└── themes/PaperMod/       # Submodule Git
```

---

## Convention articles

Frontmatter YAML attendu (généré par `article_publish.py`) :

```yaml
---
title: "Titre de l'article"
date: 2026-04-15
youtube_url: "https://youtu.be/<videoid>"
youtube_video_id: "<videoid>"
theme: "ia-travail"
categories: ["IA & Travail"]
tags: ["ia-travail"]
summary: "Résumé court (200 chars)"
cover:
  image: "https://img.youtube.com/vi/<videoid>/maxresdefault.jpg"
  alt: "Titre"
  caption: "Catégorie"
  relative: false
draft: false
catalogue_id: "<id>"
---
```

Sections corps :
1. Iframe YouTube embed responsive
2. `## Contexte` (résumé NLM)
3. `## Chapitres` (depuis `start_sec` du catalogue)
4. `## Sources` (top 15 + collapsible reste)

---

## URLs admin

| Service | URL |
|---|---|
| **Dashboard Cloudflare** | https://dash.cloudflare.com/b9a839dbd21aa26dc8e50a35c57187d8/home |
| **Projet Workers** | https://dash.cloudflare.com/b9a839dbd21aa26dc8e50a35c57187d8/workers/services/view/wetandseaai-site/production |
| **Builds** | https://dash.cloudflare.com/b9a839dbd21aa26dc8e50a35c57187d8/workers/services/view/wetandseaai-site/production/builds |
| **Settings (custom domain)** | https://dash.cloudflare.com/b9a839dbd21aa26dc8e50a35c57187d8/workers/services/view/wetandseaai-site/production/settings |
| **Repo GitHub** | https://github.com/FROMENT/wetandseaai-site |
| **Panel o2switch (DNS wetandseaai.fr)** | https://www.o2switch.fr/clients/ |
| **YouTube Studio** | https://studio.youtube.com/ |

---

## Pièges connus

| Piège | Solution |
|---|---|
| Ouvrir un `.md` dans Obsidian/Typora/VSCode-MD-Auto → frontmatter cassé | Fichiers `chmod 444` après génération + `.vscode/settings.json` désactive auto-format MD |
| Wrangler exige Node 20+ | `brew install node@20 && export PATH="/opt/homebrew/opt/node@20/bin:$PATH"` |
| `lang:` dans frontmatter | Déprécié Hugo 0.144+, géré par placement `content/<lang>/` |
| 404 sur `/posts/<slug>/` | Permalink `/:year/:month/:slug/` actif → URL = `/<year>/<month>/<slug>/` |
| Vidéo YT « non disponible » sur le site | `embeddable=true` requis sur YT Studio. Batch via `_cowork/tools/youtube_enable_embed.py --apply` |

---

## Voir aussi

- Pipeline vidéo : `~/Documents/Media/Videos/_cowork/CLAUDE.md`
- État pipeline : `~/Documents/Media/Videos/_cowork/STATUS.md`
- Cycles passés : `~/Documents/Media/Videos/_cowork/ETAT_PIPELINE.md`
- Script de génération : `~/Documents/Media/Videos/_cowork/article_publish.py`
- Tests harness : `~/Documents/Media/Videos/_cowork/tests/run_tests.sh` (G12)

---

*Dernière mise à jour : 2026-04-26*
