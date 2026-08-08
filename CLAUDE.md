# CLAUDE.md — wetandseaai-site (WST — Wet & Sea Tech)

Blog Hugo + PaperMod, bilingue FR/EN, déployé sur Cloudflare Workers.
Pas de dossier `specs/` : les règles spec-driven du CLAUDE.md utilisateur ne
s'appliquent pas ici. Détail complet dans `@README.md`.

## Commandes

```bash
hugo server                 # preview locale — FR sur /, EN sur /en/
hugo --gc --minify          # build production (identique à la CI)
```

## Builder depuis un sandbox Claude Code

`hugo` échoue à la racine : trois articles dont le nom contient « secret » sont
illisibles (règle de deny). Builder sur une copie amputée :

```bash
rsync -a --exclude='public' --exclude='resources' --exclude='.git' \
      --exclude='*secret*' ./ "$TMPDIR/wstb/"
cd "$TMPDIR/wstb" && hugo
```

**`hugo --quiet` renvoie 0 même quand le build échoue** — toujours lire la sortie
verbeuse. Ne pas ajouter `--gc` sur la copie : la purge du cache échoue en
écriture et pollue la sortie d'une ERROR sans rapport.

## Déploiement

- Push sur `main` → build et déploiement automatiques. **Aucun build de preview
  sur les autres branches** : il n'y a pas de filet, valider avant de pousser.
- Le Worker s'appelle **`wetandseaai`** ; seul le dépôt GitHub s'appelle
  `wetandseaai-site`. Une URL dashboard avec `-site` renvoie « Failed to find Worker ».
- `HUGO_VERSION` (`extended_0.164.0`) vit dans **Settings → section `Build` →
  Variables and secrets**, pas dans le bloc homonyme du haut de page, qui est le
  runtime et ignore la variable en silence. Impossible à mettre dans git.

## Pièges

- **Articles générés en `chmod 444`** : un éditeur Markdown qui auto-formate
  casse le frontmatter YAML. Ne pas retirer la protection.
- **`params.goatcounterCode`** : toute valeur non vide active le tracking sur
  chaque page. Jamais de placeholder — il serait truthy et pointerait vers un
  sous-domaine inexistant.
- **Front matter `youtube_channel_handle`** : deux canaux volontaires
  (`@discover-allin360` IA & Travail, `@wetseatech` Cyber/DevOps). Ce n'est pas
  du branding périmé, ne pas uniformiser.
- **Surcharges de thème** dans `layouts/` (dont `partials/header.html` et
  `index.html`, appliqués à tout le site). La home est paginée : le bloc
  éditorial ne se rend que sur la page 1, sinon `/page/2/`…`/page/N/`
  disparaissent des URL indexées.
- **Palette** : les tokens `--wst-*` de la charte sont partagés avec les pages
  `/tags/`. Les couleurs de la maquette vivent dans `--wst-ink*` /
  `--wst-cyan-bright`, à part.
