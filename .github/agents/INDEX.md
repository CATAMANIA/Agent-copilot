# 🎯 Agent Copilot - Index des Agents

Cette collection comprend **20 agents spécialisés** optimisés pour Claude Sonnet 4, couvrant l'ensemble du cycle de développement logiciel.

## 📋 Agents Méthodologiques

| Agent | Description | Objectif |
|-------|-------------|----------|
| **Cahier-Des-Charges-Analyst** | Analyse et validation de périmètre de cahiers des charges | Challenger et valider les spécifications fonctionnelles |
| **Plan** | Planification d'implémentation de fonctionnalités | Structurer et organiser le développement |
| **Specification** | Génération et mise à jour de documents de spécification | Créer des specs techniques complètes |
| **Debug** | Investigation systématique et résolution de problèmes | Diagnostiquer et résoudre bugs et erreurs |
| **Testing** | Conception et implémentation de suites de tests | Assurance qualité et tests complets |
| **CodeReview** | Revue de code axée qualité et sécurité | Validation et amélioration du code |
| **Security** | Analyse de sécurité et audit des vulnérabilités | Protection et conformité sécuritaire |
| **Maintenance** | Maintien, refactoring et modernisation | Améliorer la maintenabilité du code |
| **PPO** | Performance, Patterns, Optimization | Optimisation et meilleures pratiques |
| **Documentation** | Création et maintenance de documentation | Documentation complète projets et APIs |

## 🚀 Agents Technologiques

### Backend & Enterprise
| Agent | Technologie | Spécialisation |
|-------|-------------|----------------|
| **API-Expert** | REST/GraphQL | APIs modernes et microservices |
| **Developpeur-Java** | Java 8-21+ | Développement Java moderne avec Spring |
| **Developpeur-Java-SpringBoot** | Spring Boot | Applications enterprise avec DDD |
| **Developpeur-Java-Quarkus** | Quarkus/GraalVM | Supersonic subatomic Java cloud-native |
| **Developpeur-CSharp** | .NET/C# 8-12+ | Applications .NET avec patterns modernes |

### Frontend & Web
| Agent | Technologie | Spécialisation |
|-------|-------------|----------------|
| **Developpeur-React** | React/TypeScript | Applications React modernes avec hooks |
| **Developpeur-Angular** | Angular 15+ | Applications Angular enterprise |

### PHP & Frameworks
| Agent | Technologie | Spécialisation |
|-------|-------------|----------------|
| **PHP-Expert** | PHP 8.x | Architecture PHP moderne et sécurisée |
| **Laravel-Expert** | Laravel 10+ | Développement rapide avec Eloquent |
| **Symfony-Expert** | Symfony 6+ | Applications PHP d'entreprise |

## 🏗️ Architecture du Projet

```
Agent-copilot/
├── 📁 .github/
│   ├── 📁 agents/              # 20 agents spécialisés (nouveau format)
│   ├── 📁 chatmodes/           # 21 chatmodes (format legacy)
│   └── 📁 instructions/        # Standards et bonnes pratiques
├── 📁 documentations/          # Documentation structurée
│   ├── 📁 analyse/
│   │   ├── 📁 cdc/            # Analyses cahiers des charges
│   │   └── 📁 security/       # Analyses sécurité
│   ├── 📁 cahier_des_charges/ # Spécifications projets
│   ├── 📁 code_review/        # Rapports de revue
│   ├── 📁 plan_implementation/ # Plans techniques
│   └── 📁 spec/               # Spécifications techniques
└── 📄 README.md               # Documentation principale
```

## 🛡️ Standards et Conformité

- **Sécurité** : Conformité OWASP Top 10 2021
- **Accessibilité** : Standards RGAA 4.1
- **Conformité** : Exigences PCI-SSC
- **Qualité** : Meilleures pratiques par technologie

## 🎯 Format des Agents

Chaque agent suit le nouveau format avec :
- **name** : Nom de l'agent
- **description** : Description claire de l'objectif
- **model** : Claude Sonnet 4
- **tools** : Liste des outils avec nom et description

### Exemple de Structure
```yaml
---
name: Agent Name
description: Agent description
model: Claude Sonnet 4
tools:
  - name: toolName
    description: Tool description
---

# Agent Instructions
...
```

## 🔄 Migration depuis Chatmodes

Les agents remplacent progressivement les chatmodes avec :
- Extension `.agent.md` au lieu de `.chatmode.md`
- Ajout du champ `name:` dans le front-matter
- Format `tools:` avec nom et description
- Terminologie "Agent" au lieu de "Mode"

---
*Usine Logicielle complète pour un développement professionnel avec Claude Sonnet 4*
