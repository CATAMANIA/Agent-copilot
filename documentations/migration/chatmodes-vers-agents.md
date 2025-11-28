# Guide de Migration : Chatmodes vers Agents

> **Document de référence** pour la migration des fichiers `.chatmode.md` vers le nouveau format `.agent.md` de GitHub Copilot.

## 📋 Table des Matières

1. [Introduction](#introduction)
2. [Différences entre Chatmodes et Agents](#différences-entre-chatmodes-et-agents)
3. [Structure des Fichiers](#structure-des-fichiers)
4. [Guide de Migration Étape par Étape](#guide-de-migration-étape-par-étape)
5. [Exemples de Conversion](#exemples-de-conversion)
6. [Bonnes Pratiques](#bonnes-pratiques)
7. [FAQ](#faq)

---

## Introduction

### Contexte

GitHub Copilot évolue constamment et introduit régulièrement de nouvelles fonctionnalités. Le passage des **chatmodes** aux **agents** représente une évolution majeure dans la façon dont les assistants IA spécialisés sont définis et utilisés dans VS Code.

### Qu'est-ce qu'un Chatmode ?

Un **chatmode** (`.chatmode.md`) est un fichier de configuration qui définit :
- Un contexte spécialisé pour l'assistant IA
- Des outils disponibles pour l'exécution de tâches
- Des instructions comportementales spécifiques

### Qu'est-ce qu'un Agent ?

Un **agent** (`.agent.md`) est la nouvelle génération de chatmodes avec :
- Une capacité d'exécution autonome plus avancée
- Un système de permissions et d'outils enrichi
- Une meilleure intégration avec l'écosystème VS Code

---

## Différences entre Chatmodes et Agents

### Comparaison des Formats

| Aspect | Chatmode (`.chatmode.md`) | Agent (`.agent.md`) |
|--------|---------------------------|---------------------|
| **Extension de fichier** | `.chatmode.md` | `.agent.md` |
| **Emplacement** | `.github/chatmodes/` | `.github/agents/` |
| **Format Front-Matter** | YAML standard | YAML enrichi |
| **Outils disponibles** | Liste simple | Configuration détaillée |
| **Modèle IA** | Paramètre `model` | Paramètre `model` (inchangé) |
| **Capacités d'exécution** | Limitées | Étendues (autonomie) |
| **Gestion des erreurs** | Basique | Avancée avec retry |

### Changements Clés dans le Front-Matter

#### Format Chatmode (Ancien)
```yaml
---
description: Description du mode
model: Claude Sonnet 4
tools: ["search/codebase", "edit", "search/readFile"]
---
```

#### Format Agent (Nouveau)
```yaml
---
name: Nom de l'Agent
description: Description détaillée de l'agent
model: Claude Sonnet 4
tools:
  - name: codebase
    description: Recherche dans le code
  - name: editFiles
    description: Édition de fichiers
  - name: readFile
    description: Lecture de fichiers
---
```

### Nouvelles Capacités des Agents

1. **Exécution Autonome** : Les agents peuvent enchaîner des actions sans intervention utilisateur
2. **Gestion du Contexte** : Meilleure conservation du contexte entre les interactions
3. **Outils Avancés** : Accès à des outils supplémentaires pour l'automatisation
4. **Permissions Granulaires** : Contrôle fin sur ce que l'agent peut faire
5. **Intégration GitHub** : Meilleure intégration avec les workflows GitHub

---

## Structure des Fichiers

### Organisation Recommandée

```
📂 .github/
├── 📂 agents/                     # Nouveau dossier pour les agents
│   ├── 📄 Plan.agent.md
│   ├── 📄 CodeReview.agent.md
│   ├── 📄 Security.agent.md
│   ├── 📄 Debug.agent.md
│   ├── 📄 Testing.agent.md
│   ├── 📄 Documentation.agent.md
│   ├── 📄 Developpeur-Java.agent.md
│   ├── 📄 Developpeur-React.agent.md
│   └── ...
├── 📂 chatmodes/                  # Ancien dossier (à conserver pour compatibilité)
│   ├── 📄 Plan.chatmode.md
│   └── ...
├── 📂 instructions/               # Instructions partagées (inchangé)
│   └── ...
└── 📂 prompts/                    # Prompts réutilisables (inchangé)
    └── ...
```

### Structure d'un Fichier Agent

```markdown
---
name: Nom de l'Agent
description: Description concise de l'objectif de l'agent
model: Claude Sonnet 4
tools:
  - name: codebase
  - name: editFiles
  - name: readFile
  - name: terminal
  - name: browser
---

# Instructions de l'Agent

## Contexte et Objectif

[Description détaillée du rôle de l'agent]

## Directives Principales

[Instructions comportementales]

## Processus de Travail

[Étapes et méthodologie]

## Livrables

[Résultats attendus]
```

---

## Guide de Migration Étape par Étape

### Étape 1 : Préparer l'Environnement

```bash
# Créer le nouveau dossier agents
mkdir -p .github/agents

# Copier les chatmodes existants comme base
cp .github/chatmodes/*.chatmode.md .github/agents/
```

### Étape 2 : Renommer les Fichiers

```bash
# Renommer les extensions de fichiers
cd .github/agents
for file in *.chatmode.md; do
  mv "$file" "${file%.chatmode.md}.agent.md"
done
```

### Étape 3 : Mettre à Jour le Front-Matter

Pour chaque fichier `.agent.md`, convertir le front-matter :

**Avant (Chatmode) :**
```yaml
---
description: Debug et résolution systématique de problèmes
model: Claude Sonnet 4
tools: ["search/codebase", "search/readFile", "problems", "testFailure"]
---
```

**Après (Agent) :**
```yaml
---
name: Debug Expert
description: Agent spécialisé dans le debug et la résolution systématique de problèmes dans le code
model: Claude Sonnet 4
tools:
  - name: codebase
    description: Recherche dans la base de code
  - name: readFile
    description: Lecture de fichiers
  - name: problems
    description: Détection de problèmes
  - name: testFailure
    description: Analyse des échecs de tests
  - name: terminal
    description: Exécution de commandes
---
```

### Étape 4 : Adapter le Contenu

1. **Titre** : Remplacer "Mode Instructions" par "Agent Instructions"
2. **Introduction** : Actualiser le texte d'introduction
3. **Références** : Mettre à jour les chemins vers les instructions

**Avant :**
```markdown
# Debug Mode Instructions

You are in **Debug Mode**. Your objective is...
```

**Après :**
```markdown
# Debug Agent Instructions

You are the **Debug Agent**. Your objective is...
```

### Étape 5 : Tester les Agents

1. Ouvrir VS Code avec l'extension GitHub Copilot
2. Utiliser la commande `@agent-name` pour invoquer l'agent
3. Vérifier que les outils sont correctement disponibles
4. Tester les fonctionnalités principales

### Étape 6 : Mettre à Jour la Documentation

- Mettre à jour le README.md principal
- Actualiser l'INDEX.md dans le dossier agents
- Documenter les nouvelles capacités

---

## Exemples de Conversion

### Exemple 1 : Agent Plan

#### Avant (Plan.chatmode.md)
```yaml
---
description: Generate a structured implementation plan for new features or refactoring tasks.
model: Claude Sonnet 4
tools: ["search/codebase", "fetch", "search/readFile", "edit", "findTestFiles", "githubRepo", "search/listDirectory", "search", "usages"]
---

# Planning mode instructions

You are in **Planning Mode**. Your objective is to create a comprehensive and actionable implementation plan...
```

#### Après (Plan.agent.md)
```yaml
---
name: Planning Agent
description: Agent spécialisé dans la génération de plans d'implémentation structurés pour les nouvelles fonctionnalités ou tâches de refactoring
model: Claude Sonnet 4
tools:
  - name: codebase
    description: Recherche dans la base de code
  - name: fetch
    description: Récupération de ressources externes
  - name: readFile
    description: Lecture de fichiers
  - name: editFiles
    description: Édition de fichiers
  - name: findTestFiles
    description: Recherche de fichiers de test
  - name: githubRepo
    description: Interactions avec le repository GitHub
  - name: listDirectory
    description: Liste le contenu des répertoires
  - name: search
    description: Recherche avancée
  - name: usages
    description: Recherche d'usages dans le code
---

# Planning Agent Instructions

You are the **Planning Agent**. Your objective is to create a comprehensive and actionable implementation plan...
```

### Exemple 2 : Agent Security

#### Avant (Security.chatmode.md)
```yaml
---
description: Analyze and implement security measures, identify vulnerabilities
model: Claude Sonnet 4
tools: ["search/codebase", "search/readFile", "usages", "problems", "edit/editFiles", "extensions", "runCommands", "search"]
---
```

#### Après (Security.agent.md)
```yaml
---
name: Security Agent
description: Agent expert en analyse de sécurité, identification de vulnérabilités et implémentation de mesures de protection
model: Claude Sonnet 4
tools:
  - name: codebase
    description: Recherche dans la base de code pour identifier les vulnérabilités
  - name: readFile
    description: Lecture de fichiers pour analyse de sécurité
  - name: usages
    description: Recherche d'usages potentiellement dangereux
  - name: problems
    description: Détection de problèmes de sécurité
  - name: editFiles
    description: Modification de fichiers pour corrections de sécurité
  - name: terminal
    description: Exécution de commandes de scan de sécurité
  - name: search
    description: Recherche avancée de patterns de sécurité
---
```

---

## Bonnes Pratiques

### Nommage des Agents

| Convention | Exemple | Description |
|------------|---------|-------------|
| **Nom descriptif** | `Security-Expert.agent.md` | Indique clairement la spécialisation |
| **CamelCase ou Kebab** | `CodeReview.agent.md` | Format cohérent |
| **Suffixe Agent** | `Java-Developer.agent.md` | Distingue des autres fichiers |

### Configuration des Outils

```yaml
tools:
  # ✅ BON - Description explicite
  - name: codebase
    description: Recherche dans le code source du projet

  # ❌ MAUVAIS - Pas de description
  - name: codebase
```

### Structure du Contenu

1. **Introduction claire** : Définir le rôle et l'objectif de l'agent
2. **Directives principales** : Lister les principes fondamentaux
3. **Processus détaillé** : Expliquer la méthodologie étape par étape
4. **Références aux instructions** : Lier aux fichiers d'instructions partagés
5. **Livrables** : Définir les résultats attendus

### Références Croisées

```markdown
## Core Directives

For all tasks, you MUST adhere to the guidelines in:
- **Reference:** [OWASP Security Standards](../instructions/security-owasp.instructions.md)
- **Reference:** [API Standards](../instructions/api-standards.instructions.md)
```

---

## FAQ

### Q: Dois-je supprimer les chatmodes existants ?

**R:** Non, il est recommandé de conserver les chatmodes pour la compatibilité avec les anciennes versions de VS Code et GitHub Copilot. Les deux formats peuvent coexister.

### Q: Les agents sont-ils rétrocompatibles ?

**R:** Les agents utilisent un format légèrement différent. Les anciennes versions de l'extension GitHub Copilot pourraient ne pas les reconnaître. Vérifiez la version minimale requise.

### Q: Comment invoquer un agent dans VS Code ?

**R:** Les agents sont invoqués via le chat GitHub Copilot en utilisant leur nom. La syntaxe exacte peut varier selon la version de l'extension. Consultez la documentation officielle de GitHub Copilot pour la syntaxe d'invocation actuelle.

### Q: Puis-je utiliser les mêmes instructions pour les deux formats ?

**R:** Oui, les fichiers d'instructions (`.instructions.md`) sont compatibles avec les deux formats et peuvent être référencés de la même manière.

### Q: Comment gérer les agents technologiques (Java, React, etc.) ?

**R:** Créez des agents spécialisés qui héritent des instructions communes et ajoutent des capacités spécifiques à la technologie :

```yaml
---
name: Java Developer Agent
description: Agent expert en développement Java avec Spring Boot
model: Claude Sonnet 4
tools:
  - name: codebase
    description: Recherche dans la base de code
  - name: editFiles
    description: Édition de fichiers
  - name: terminal
    description: Exécution de commandes (utilisé pour Maven, Gradle, etc.)
---
```

> **Note :** Les outils disponibles dépendent de la configuration de GitHub Copilot. Consultez la documentation officielle pour la liste complète des outils supportés.

### Q: Quelle est la différence de performance entre chatmodes et agents ?

**R:** Les agents offrent généralement de meilleures performances car :
- Ils peuvent enchaîner des actions de manière autonome
- La gestion du contexte est optimisée
- Les outils sont mieux intégrés

---

## Ressources Additionnelles

- [Documentation officielle GitHub Copilot](https://docs.github.com/en/copilot)
- [VS Code Extension API](https://code.visualstudio.com/api)
- [Index des Chatmodes existants](../../.github/chatmodes/INDEX.md)

---

*Dernière mise à jour : 28 novembre 2025*  
*Optimisé pour : Claude Sonnet 4 et GitHub Copilot*
