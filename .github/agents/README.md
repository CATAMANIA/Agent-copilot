# Generic Agents Collection

> **🤖 Modèle Optimisé :** Claude Sonnet 4  
> Cette collection a été spécialement conçue et optimisée pour fonctionner avec Claude Sonnet 4, offrant des performances et une compréhension maximales.

Cette collection d'agents génériques a été conçue pour être réutilisée sur plusieurs projets de développement logiciel. Chaque agent se concentre sur un aspect spécifique du cycle de développement et peut être utilisé indépendamment ou en combinaison avec d'autres.

## 🔄 Migration depuis Chatmodes

Cette collection d'agents est la nouvelle version des chatmodes, utilisant le format moderne `.agent.md`. Les principales différences sont :

| Aspect | Chatmodes (Legacy) | Agents (Nouveau) |
|--------|-------------------|------------------|
| Extension | `.chatmode.md` | `.agent.md` |
| Front-matter | `description:`, `model:`, `tools:[]` | `name:`, `description:`, `model:`, `tools:[{name, description}]` |
| Terminologie | "Mode" | "Agent" |
| Emplacement | `.github/chatmodes/` | `.github/agents/` |

## Agents Disponibles

### 🎯 Agents Méthodologiques

#### [Plan.agent.md](./Plan.agent.md)
**Objectif :** Génération de plans d'implémentation structurés pour les nouvelles fonctionnalités ou tâches de refactoring.

#### [PPO.agent.md](./PPO.agent.md)
**Objectif :** Optimisation et refactoring du code en utilisant les meilleures pratiques (Performance, Patterns, Optimization).

#### [Specification.agent.md](./Specification.agent.md)
**Objectif :** Génération et mise à jour de documents de spécification pour les fonctionnalités nouvelles ou existantes.

#### [Debug.agent.md](./Debug.agent.md)
**Objectif :** Debug et résolution systématique de problèmes dans le code.

#### [CodeReview.agent.md](./CodeReview.agent.md)
**Objectif :** Conduite de revues de code complètes axées sur la qualité, sécurité et meilleures pratiques.

#### [Documentation.agent.md](./Documentation.agent.md)
**Objectif :** Création, mise à jour et maintenance de documentation complète pour les projets et fonctionnalités.

#### [Testing.agent.md](./Testing.agent.md)
**Objectif :** Conception, implémentation et maintenance de suites de tests complètes.

#### [Security.agent.md](./Security.agent.md)
**Objectif :** Analyse et implémentation de mesures de sécurité, identification de vulnérabilités.

#### [Maintenance.agent.md](./Maintenance.agent.md)
**Objectif :** Maintenance, refactoring et modernisation de bases de code existantes.

#### [Cahier-Des-Charges-Analyst.agent.md](./Cahier-Des-Charges-Analyst.agent.md)
**Objectif :** Analyse critique et validation des cahiers des charges avec challenge systématique des besoins.

### ⚙️ Agents Technologiques

#### Backend

##### [Developpeur-Java.agent.md](./Developpeur-Java.agent.md)
**Objectif :** Développement Java enterprise avec écosystème Spring, patterns modernes et meilleures pratiques.

##### [Developpeur-Java-SpringBoot.agent.md](./Developpeur-Java-SpringBoot.agent.md)
**Objectif :** Développement Spring Boot spécialisé avec architecture microservices et cloud-native.

##### [Developpeur-Java-Quarkus.agent.md](./Developpeur-Java-Quarkus.agent.md)
**Objectif :** Développement Quarkus cloud-native avec compilation native GraalVM et programmation réactive.

##### [Developpeur-CSharp.agent.md](./Developpeur-CSharp.agent.md)
**Objectif :** Développement C# moderne avec .NET, fonctionnalités récentes et patterns enterprise.

##### [PHP-Expert.agent.md](./PHP-Expert.agent.md)
**Objectif :** Architecture PHP senior avec focus sur la sécurité et les meilleures pratiques modernes.

##### [Laravel-Expert.agent.md](./Laravel-Expert.agent.md)
**Objectif :** Développement Laravel expert avec écosystème complet et développement rapide.

##### [Symfony-Expert.agent.md](./Symfony-Expert.agent.md)
**Objectif :** Développement Symfony enterprise avec architecture robuste et composants avancés.

#### Frontend

##### [Developpeur-React.agent.md](./Developpeur-React.agent.md)
**Objectif :** Développement React moderne avec hooks, TypeScript et optimisation des performances.

##### [Developpeur-Angular.agent.md](./Developpeur-Angular.agent.md)
**Objectif :** Développement Angular moderne avec TypeScript, composants standalone et patterns réactifs.

#### API/Architecture

##### [API-Expert.agent.md](./API-Expert.agent.md)
**Objectif :** Conception et développement d'APIs modernes REST/GraphQL avec microservices.

## Comment Utiliser les Agents

### 1. Sélection de l'Agent
Choisissez l'agent qui correspond le mieux à votre objectif actuel :

**Agents Méthodologiques :**
- **Planification** → Plan.agent.md
- **Optimisation/Refactoring** → PPO.agent.md ou Maintenance.agent.md
- **Documentation** → Documentation.agent.md ou Specification.agent.md
- **Problèmes** → Debug.agent.md
- **Qualité** → CodeReview.agent.md
- **Tests** → Testing.agent.md
- **Sécurité** → Security.agent.md

**Agents Technologiques :**
- **Java Enterprise** → Developpeur-Java.agent.md
- **Spring Boot** → Developpeur-Java-SpringBoot.agent.md
- **Quarkus Cloud-Native** → Developpeur-Java-Quarkus.agent.md
- **Angular** → Developpeur-Angular.agent.md
- **React** → Developpeur-React.agent.md
- **C#/.NET** → Developpeur-CSharp.agent.md
- **PHP Architecture** → PHP-Expert.agent.md
- **Laravel Framework** → Laravel-Expert.agent.md
- **Symfony Enterprise** → Symfony-Expert.agent.md
- **API Development** → API-Expert.agent.md

### 2. Activation de l'Agent
Dans VS Code avec GitHub Copilot, activez l'agent choisi en référençant le fichier approprié.

### 3. Utilisation Combinée
Les agents peuvent être utilisés en séquence pour un workflow complet :
1. **Plan** → Planifier la fonctionnalité
2. **Testing** → Définir la stratégie de tests
3. **PPO/Maintenance** → Implémenter et optimiser
4. **CodeReview** → Réviser le code
5. **Security** → Vérifier la sécurité
6. **Documentation** → Documenter la solution

## Structure des Agents

Chaque agent suit une structure standardisée :

```yaml
---
name: Agent Name
description: Description claire de l'objectif
model: Claude Sonnet 4
tools:
  - name: toolName
    description: Description de l'outil
---

# Instructions de l'Agent
- Principes fondamentaux
- Processus détaillé
- Bonnes pratiques
- Exemples et cas d'usage
- Livrables attendus
```

### Champs du Front-Matter
- **name** : Nom de l'agent
- **description** : Explication concise du rôle de l'agent
- **model** : Modèle d'IA recommandé (Claude Sonnet 4)
- **tools** : Liste des outils avec nom et description

## 📊 Statistiques de la Collection

**Total : 20 agents** optimisés pour Claude Sonnet 4  
**Total : 9 fichiers d'instructions** pour les standards et bonnes pratiques

### Répartition par Catégorie

#### 🔄 Agents Méthodologiques (10)
- Plan, Specification, Debug, Testing, CodeReview
- Security, Maintenance, Documentation, PPO
- Cahier-Des-Charges-Analyst

#### ⚙️ Agents Technologiques (10)
- **Backend (7):** Java, Spring Boot, Quarkus, C#, PHP, Laravel, Symfony
- **Frontend (2):** React, Angular
- **API/Architecture (1):** API-Expert

## Contribution

Pour contribuer à cette collection d'agents :
1. Suivez la structure standard avec le nouveau format
2. Documentez clairement les cas d'usage
3. Testez sur différents types de projets avec Claude Sonnet 4
4. Partagez les retours d'expérience
5. Proposez des améliorations spécifiques au modèle

---

*Dernière mise à jour : Novembre 2025*
