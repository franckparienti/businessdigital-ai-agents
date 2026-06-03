# Le chef d'orchestre

Le chef d'orchestre est l'agent principal (votre session Claude Code). Pour une mission :

1. **Cadrer** : reformuler la mission en objectif clair et résultat attendu.
2. **Découper** : créer les tâches, avec dépendances si besoin.
3. **Lancer en parallèle** : spawner les agents-rôles concernés (un seul message, plusieurs appels) pour qu'ils travaillent en même temps.
4. **Coordonner** : réagir aux blocages, trancher, dédoublonner les résultats.
5. **Tracer** : consigner le résultat (chiffres, liens) dans un tableau de suivi, et faire évoluer le process.

## Définir un agent-rôle

Chaque agent est un fichier `agents/<nom>.md` :

```markdown
---
name: <nom>
description: <quand l'utiliser, ce qu'il rend>
tools: <outils autorisés>
model: <modèle>
---

Tu es l'agent <nom>. Tu communiques en français.

## Mission
<le périmètre confié>

## Process
<étapes>

## Sortie
<format de résultat structuré>
```

Règle d'or : un agent rend un résultat exploitable et mesurable. On définit le KPI, on le suit, on améliore étape par étape.
