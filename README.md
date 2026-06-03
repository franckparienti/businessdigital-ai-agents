# BusinessDigital — AI Agents Framework

> Comment on orchestre une équipe d'agents IA spécialisés avec Claude Code — la méthode, en open source.

![status](https://img.shields.io/badge/status-active-success)
![claude--code](https://img.shields.io/badge/built%20for-Claude%20Code-blue)
![license](https://img.shields.io/badge/license-MIT-green)

Quelques fichiers `.md` suffisent à orchestrer toute une production : veille, contenu, réseaux sociaux. Voici comment [BusinessDigital.fr](https://businessdigital.fr) le fait, et le squelette pour le reproduire.

Ce dépôt est la version **publique et générique** du framework : la méthode et des templates de rôles, sans aucune donnée interne.

## L'idée en une image

```
                 ┌─────────────────────────┐
   Mission  ───▶ │   Chef d'orchestre       │
                 │  (votre session Claude)  │
                 └───────────┬──────────────┘
            cadre, découpe, lance EN PARALLÈLE, coordonne, trace
        ┌────────────┬───────┴───────┬────────────┐
        ▼            ▼               ▼            ▼
   research.md   content.md      social.md     (vos rôles)
   veille        pages uniques   multidiffusion
   structurée    + IndexNow      + visuels
```

Une mission = un chef d'orchestre + des agents-rôles spécialisés, chacun défini par un `agents/<rôle>.md`. Pour une mission, le chef d'orchestre crée les tâches, lance les bons agents **en parallèle**, coordonne, et trace les résultats.

## Démarrage

1. Copiez le dossier `agents/` dans votre projet, sous `.claude/agents/`.
2. Adaptez chaque rôle à votre métier (les templates sont génériques).
3. Dans Claude Code, confiez une mission : *« lance research + content sur X »*. Le chef d'orchestre s'occupe du reste.

```
.claude/
  agents/
    research.md
    content.md
    social.md
ORCHESTRATION.md
```

## Les rôles fournis

| Rôle | Ce qu'il fait | Sortie mesurable |
|------|---------------|------------------|
| `research` | Veille en éventail (lecture seule) | Liste structurée et vérifiée |
| `content` | Génération de pages uniques (anti duplicate-content) + IndexNow | Nb de pages/jour |
| `social` | Multidiffusion, un contenu différent par canal | Nb de publications/jour |

## Principes

- **Parallélisme** : plusieurs agents en même temps pour couvrir vite.
- **Process documenté (SOP)** : chaque rôle a un process écrit, amélioré au fil du temps.
- **Sortie structurée et mesurable** : un agent rend des données et un KPI, pas un essai.
- **Coût maîtrisé** : modèles ouverts/gratuits quand c'est possible.

## À propos

BusinessDigital.fr forme les entreprises à piloter l'IA et les agents — et applique ces méthodes à ses propres opérations. Ce dépôt en partage le squelette.

MIT.
