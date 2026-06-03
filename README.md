# BusinessDigital — AI Agents Framework

Comment [BusinessDigital.fr](https://businessdigital.fr) orchestre une équipe d'agents IA spécialisés avec Claude Code pour exécuter ses opérations (veille, contenu, réseaux sociaux) de façon reproductible.

Ce dépôt est la version **publique et générique** de notre framework : la méthode et des templates de rôles, sans aucune donnée interne. Il sert à montrer comment on travaille, pas à exposer nos données.

## L'idée

Une mission = un chef d'orchestre (vous, dans Claude Code) + des agents-rôles spécialisés, chacun défini par un fichier `agents/<rôle>.md` (frontmatter + responsabilités + process). Pour une mission, le chef d'orchestre crée les tâches, lance les bons agents **en parallèle**, coordonne, et trace les résultats.

Inspiré du pattern « équipe d'agents » de Claude Code, adapté à des missions métier plutôt qu'à du développement logiciel.

## Structure

```
agents/
  research.md   # veille / recherche en éventail (lecture seule, sortie structurée)
  content.md    # génération de contenu unique de masse (pages, SEO, IndexNow)
  social.md     # multidiffusion réseaux, un contenu différent par canal
ORCHESTRATION.md # le rôle du chef d'orchestre
```

## Principes

- **Parallélisme** : plusieurs agents du même rôle peuvent tourner en parallèle pour couvrir vite un large périmètre.
- **Process documenté (SOP)** : chaque rôle a un process écrit, mis à jour au fil du temps.
- **Sortie structurée** : un agent rend des données exploitables, pas un essai.
- **Coût maîtrisé** : génération sur des modèles ouverts/gratuits quand c'est possible.

## À propos

BusinessDigital.fr est un organisme de formation à l'intelligence artificielle pour les entreprises. On forme les équipes à piloter l'IA et les agents, et on applique ces méthodes à nos propres opérations.

Licence MIT.
