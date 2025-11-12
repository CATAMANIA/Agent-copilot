# Generic Chatmodes Collection

> **🤖 Modèle Optimisé :** Claude Sonnet 4  
> Cette collection a été spécialement conçue et optimisée pour fonctionner avec Claude Sonnet 4, offrant des performances et une compréhension maximales.

Cette collection de chatmodes génériques a été conçue pour être réutilisée sur plusieurs projets de développement logiciel. Chaque chatmode se concentre sur un aspect spécifique du cycle de développement et peut être utilisé indépendamment ou en combinaison avec d'autres.

## Chatmodes Disponibles

### 🎯 [Plan.chatmode.md](./Plan.chatmode.md)
**Objectif :** Génération de plans d'implémentation structurés pour les nouvelles fonctionnalités ou tâches de refactoring.

**Utilisation :**
- Planification de nouvelles fonctionnalités
- Préparation de tâches de refactoring importantes
- Analyse de requirements et conception

**Outils utilisés :** search/codebase, fetch, search/readFile, edit, findTestFiles, githubRepo, search/listDirectory, search, usages

### 🛠️ [PPO.chatmodes.md](./PPO.chatmode.md)
**Objectif :** Optimisation et refactoring du code en utilisant les meilleures pratiques (Performance, Patterns, Optimization).

**Utilisation :**
- Optimisation des performances
- Implémentation de design patterns
- Amélioration de la qualité du code
- Refactoring technique

**Outils utilisés :** search/codebase, edit/editFiles, search/readFile, usages, problems, runCommands, testFailure, search

### 📋 [Specification.chatmode.md](./Specification.chatmode.md)
**Objectif :** Génération et mise à jour de documents de spécification pour les fonctionnalités nouvelles ou existantes.

**Utilisation :**
- Création de spécifications techniques
- Documentation d'architecture
- Définition de requirements
- Standards de développement

**Outils utilisés :** changes, search/codebase, edit/editFiles, extensions, fetch, githubRepo, new, openSimpleBrowser, problems, runCommands, runTasks, search, search/searchResults, runCommands/terminalLastCommand, runCommands/terminalSelection, testFailure, usages, vscodeAPI, github/*

### 🐛 [Debug.chatmode.md](./Debug.chatmode.md)
**Objectif :** Debug et résolution systématique de problèmes dans le code.

**Utilisation :**
- Investigation d'erreurs et bugs
- Analyse de problèmes de performance
- Diagnostic de problèmes d'intégration
- Résolution de problèmes de déploiement

**Outils utilisés :** search/codebase, search/readFile, problems, testFailure, runCommands, usages, search, extensions, changes

### 👁️ [CodeReview.chatmode.md](./CodeReview.chatmode.md)
**Objectif :** Conduite de revues de code complètes axées sur la qualité, sécurité et meilleures pratiques.

**Utilisation :**
- Revue de pull requests
- Analyse de qualité de code
- Vérification des standards de développement
- Évaluation de sécurité

**Outils utilisés :** search/codebase, search/readFile, usages, problems, changes, testFailure, extensions, search

### 📚 [Documentation.chatmode.md](./Documentation.chatmode.md)
**Objectif :** Création, mise à jour et maintenance de documentation complète pour les projets et fonctionnalités.

**Utilisation :**
- Documentation d'API
- Guides utilisateur
- Documentation technique
- Guides de contribution

**Outils utilisés :** search/codebase, search/readFile, edit/editFiles, search, usages, new, fetch

### 🧪 [Testing.chatmode.md](./Testing.chatmode.md)
**Objectif :** Conception, implémentation et maintenance de suites de tests complètes.

**Utilisation :**
- Stratégie de tests
- Tests unitaires et d'intégration
- Tests end-to-end
- Automatisation de tests

**Outils utilisés :** search/codebase, search/readFile, edit/editFiles, usages, testFailure, runCommands, problems, search

### 🔒 [Security.chatmode.md](./Security.chatmode.md)
**Objectif :** Analyse et implémentation de mesures de sécurité, identification de vulnérabilités.

**Utilisation :**
- Audit de sécurité
- Implémentation de contrôles de sécurité
- Analyse de vulnérabilités
- Conformité sécuritaire

**Outils utilisés :** search/codebase, search/readFile, usages, problems, edit/editFiles, extensions, runCommands, search

### 🔧 [Maintenance.chatmode.md](./Maintenance.chatmode.md)
**Objectif :** Maintenance, refactoring et modernisation de bases de code existantes.

**Utilisation :**
- Réduction de la dette technique
- Modernisation de frameworks
- Optimisation de performance
- Refactoring d'architecture

**Outils utilisés :** search/codebase, search/readFile, edit/editFiles, usages, problems, testFailure, runCommands, changes, search

### 📋 [Cahier-Des-Charges-Analyst.chatmode.md](./Cahier-Des-Charges-Analyst.chatmode.md)
**Objectif :** Analyse critique et validation des cahiers des charges avec challenge systématique des besoins.

**Utilisation :**
- Validation et challenge de périmètres fonctionnels
- Analyse multi-niveaux (surface et approfondie)
- Questionnement structuré pour affiner les besoins
- Identification des contradictions et ambiguïtés
- Priorisation des fonctionnalités avec matrices d'analyse

**Outils utilisés :** search/codebase, edit/editFiles, search/readFile, usages, problems, runCommands, testFailure, search, extensions

## Chatmodes Spécialisés par Technologie

### ☕ [Developpeur-Java.chatmode.md](./Developpeur-Java.chatmode.md)
**Objectif :** Développement Java enterprise avec écosystème Spring, patterns modernes et meilleures pratiques.

**Utilisation :**
- Applications Java enterprise avec Spring
- Microservices et APIs REST
- Intégration de bases de données avec JPA/Hibernate
- Tests avancés et patterns architecturaux

### 🚀 [Developpeur-Java-SpringBoot.chatmode.md](./Developpeur-Java-SpringBoot.chatmode.md)
**Objectif :** Développement Spring Boot spécialisé avec architecture microservices et cloud-native.

**Utilisation :**
- Applications Spring Boot modernes
- Configuration avancée et auto-configuration
- Architecture microservices avec Spring Cloud
- Sécurité JWT et observabilité

### ⚡ [Developpeur-Java-Quarkus.chatmode.md](./Developpeur-Java-Quarkus.chatmode.md)
**Objectif :** Développement Quarkus cloud-native avec compilation native GraalVM et programmation réactive.

**Utilisation :**
- Applications Quarkus supersonic et subatomic
- Compilation native avec GraalVM
- Programmation réactive avec SmallRye Mutiny
- Optimisation pour conteneurs et Kubernetes

### 🅰️ [Developpeur-Angular.chatmode.md](./Developpeur-Angular.chatmode.md)
**Objectif :** Développement Angular moderne avec TypeScript, composants standalone et patterns réactifs.

**Utilisation :**
- Applications Angular avec architecture moderne
- Composants standalone et signals
- Programmation réactive avec RxJS
- Tests avec Angular Testing Utilities

### ⚛️ [Developpeur-React.chatmode.md](./Developpeur-React.chatmode.md)
**Objectif :** Développement React moderne avec hooks, TypeScript et optimisation des performances.

**Utilisation :**
- Applications React avec hooks modernes
- Gestion d'état avec Context API et useReducer
- Optimisation des performances et lazy loading
- Tests avec React Testing Library

### #️⃣ [Developpeur-CSharp.chatmode.md](./Developpeur-CSharp.chatmode.md)
**Objectif :** Développement C# moderne avec .NET, fonctionnalités récentes et patterns enterprise.

**Utilisation :**
- Applications .NET avec C# moderne (8-12+)
- APIs Web avec ASP.NET Core
- Entity Framework Core et patterns CQRS
- Tests avancés et sécurité

### 🐘 [PHP-Expert.chatmode.md](./PHP-Expert.chatmode.md)
**Objectif :** Architecture PHP senior avec focus sur la sécurité et les meilleures pratiques modernes.

**Utilisation :**
- Architecture PHP 8+ avec patterns avancés
- Sécurité et audit de code PHP
- Standards PSR et développement moderne
- Planification et refactoring d'applications PHP

### 🎼 [Laravel-Expert.chatmode.md](./Laravel-Expert.chatmode.md)
**Objectif :** Développement Laravel expert avec écosystème complet et développement rapide.

**Utilisation :**
- Applications Laravel 10+ modernes
- Eloquent ORM et relations complexes
- APIs Laravel avec Sanctum/Passport
- Tests Laravel et architecture MVC

### 🎯 [Symfony-Expert.chatmode.md](./Symfony-Expert.chatmode.md)
**Objectif :** Développement Symfony enterprise avec architecture robuste et composants avancés.

**Utilisation :**
- Applications Symfony 6+ enterprise
- Doctrine ORM et DDD patterns
- Dependency Injection et services
- API Platform et architecture hexagonale

### 🔗 [API-Expert.chatmode.md](./API-Expert.chatmode.md)
**Objectif :** Conception et développement d'APIs modernes REST/GraphQL avec microservices.

**Utilisation :**
- APIs REST et GraphQL modernes
- Microservices et architecture distribuée
- Sécurité API et authentification
- Documentation OpenAPI et tests d'intégration

**Tous ces chatmodes spécialisés sont optimisés pour Claude Sonnet 4**

## Comment Utiliser les Chatmodes

### 1. Sélection du Chatmode
Choisissez le chatmode qui correspond le mieux à votre objectif actuel :

**Chatmodes Génériques :**
- **Planification** → Plan.chatmode.md
- **Optimisation/Refactoring** → PPO.chatmodes.md ou Maintenance.chatmode.md
- **Documentation** → Documentation.chatmode.md ou Specification.chatmode.md
- **Problèmes** → Debug.chatmode.md
- **Qualité** → CodeReview.chatmode.md
- **Tests** → Testing.chatmode.md
- **Sécurité** → Security.chatmode.md

**Chatmodes Spécialisés par Technologie :**
- **Java Enterprise** → Developpeur-Java.chatmode.md
- **Spring Boot** → Developpeur-Java-SpringBoot.chatmode.md
- **Quarkus Cloud-Native** → Developpeur-Java-Quarkus.chatmode.md
- **Angular** → Developpeur-Angular.chatmode.md
- **React** → Developpeur-React.chatmode.md
- **C#/.NET** → Developpeur-CSharp.chatmode.md
- **PHP Architecture** → PHP-Expert.chatmode.md
- **Laravel Framework** → Laravel-Expert.chatmode.md
- **Symfony Enterprise** → Symfony-Expert.chatmode.md
- **API Development** → API-Expert.chatmode.md

### 2. Activation du Chatmode
Dans VS Code avec GitHub Copilot, activez le chatmode choisi en référençant le fichier approprié.

### 3. Utilisation Combinée
Les chatmodes peuvent être utilisés en séquence pour un workflow complet :
1. **Plan** → Planifier la fonctionnalité
2. **Testing** → Définir la stratégie de tests
3. **PPO/Maintenance** → Implémenter et optimiser
4. **CodeReview** → Réviser le code
5. **Security** → Vérifier la sécurité
6. **Documentation** → Documenter la solution

## Personnalisation

### Adaptation aux Technologies
Les chatmodes génériques incluent des sections pour différentes technologies, tandis que les chatmodes spécialisés se concentrent sur :

**Chatmodes Génériques :**
- **.NET/C#**
- **JavaScript/TypeScript**
- **Bases de données**
- **APIs REST**
- **Cloud/Infrastructure**

**Chatmodes Spécialisés :**
- **Java/Spring/Quarkus** → Écosystème Java complet
- **Angular** → Framework Angular et TypeScript
- **React** → Bibliothèque React et écosystème
- **C#/.NET** → Plateforme .NET moderne
- **PHP/Laravel/Symfony** → Écosystème PHP moderne
- **APIs REST/GraphQL** → Développement d'APIs universelles

### Modification des Outils
Vous pouvez adapter la liste d'outils dans chaque chatmode selon les outils disponibles dans votre environnement.

### Extension des Chatmodes
Les chatmodes peuvent être étendus avec :
- Standards spécifiques à votre organisation
- Processus métier particuliers
- Technologies spécialisées
- Réglementations sectorielles

## Meilleures Pratiques

### 1. Cohérence
- Utilisez les mêmes chatmodes pour des tâches similaires
- Maintenez la cohérence dans l'équipe
- Documentez les adaptations locales

### 2. Évolution
- Mettez à jour les chatmodes selon les retours d'expérience
- Adaptez aux nouvelles technologies et pratiques
- Partagez les améliorations avec l'équipe

### 3. Formation
- Formez l'équipe à l'utilisation des chatmodes
- Partagez les cas d'usage et exemples
- Établissez des bonnes pratiques d'équipe

## Structure des Chatmodes

Chaque chatmode suit une structure standardisée :

```yaml
---
description: Description claire de l'objectif
model: Claude Sonnet 4
tools: [liste des outils utilisés]
---

# Instructions du Mode
- Principes fondamentaux
- Processus détaillé
- Bonnes pratiques
- Exemples et cas d'usage
- Livrables attendus
```

### Champs du Front-Matter
- **description** : Explication concise du rôle du chatmode
- **model** : Modèle d'IA recommandé (Claude Sonnet 4)
- **tools** : Liste des outils VS Code/GitHub Copilot utilisés

Cette structure assure la cohérence et facilite la maintenance et l'extension des chatmodes.

## Optimisation pour Claude Sonnet 4

### Pourquoi Claude Sonnet 4 ?
Cette collection a été spécialement optimisée pour **Claude Sonnet 4** en raison de ses capacités avancées :

- **📊 Analyse de Code Sophistiquée** : Compréhension approfondie des patterns et architectures complexes
- **🔍 Raisonnement Contextuel** : Capacité à maintenir le contexte sur de longs workflows de développement
- **⚡ Performance Optimale** : Temps de réponse rapides pour les tâches de développement courantes
- **🎯 Précision Technique** : Génération de code et suggestions plus précises et pertinentes
- **🔗 Intégration Multi-Outils** : Utilisation efficace des outils VS Code et GitHub Copilot

### Configuration Recommandée
```yaml
model: Claude Sonnet 4
temperature: 0.1  # Pour la consistance dans le code
max_tokens: 8192  # Pour les réponses détaillées
```

### Compatibilité avec d'Autres Modèles
Bien qu'optimisés pour Claude Sonnet 4, ces chatmodes restent compatibles avec d'autres modèles IA avancés. Cependant, les performances et la précision peuvent varier.

## Contribution

Pour contribuer à cette collection de chatmodes :
1. Suivez la structure standard
2. Documentez clairement les cas d'usage
3. Testez sur différents types de projets avec Claude Sonnet 4
4. Partagez les retours d'expérience
5. Proposez des améliorations spécifiques au modèle

## Support et Évolution

Cette collection est conçue pour évoluer avec les besoins des projets et les nouvelles pratiques de développement. N'hésitez pas à adapter, étendre et améliorer ces chatmodes selon vos besoins spécifiques.

---

## 📊 Statistiques de la Collection

**Total : 20 chatmodes** optimisés pour Claude Sonnet 4  
**Total : 9 fichiers d'instructions** pour les standards et bonnes pratiques

### Répartition par Catégorie

#### 🔄 Chatmodes Méthodologiques (10)
- **Plan.chatmode.md** - Planification et architecture
- **Specification.chatmode.md** - Documentation et spécifications  
- **Debug.chatmode.md** - Debug et résolution de problèmes
- **Testing.chatmode.md** - Stratégies et implémentation de tests
- **CodeReview.chatmode.md** - Revue de code et qualité
- **Security.chatmode.md** - Analyse et sécurité
- **Maintenance.chatmode.md** - Maintenance et refactoring
- **Documentation.chatmode.md** - Documentation technique
- **PPO.chatmode.md** - Performance, Patterns, Optimization
- **Cahier-Des-Charges-Analyst.chatmode.md** - Analyse de requirements

#### ⚙️ Chatmodes Technologiques (10)
**Backend (7) :**
- **Developpeur-Java.chatmode.md** - Java Enterprise et Spring
- **Developpeur-Java-SpringBoot.chatmode.md** - Spring Boot spécialisé
- **Developpeur-Java-Quarkus.chatmode.md** - Quarkus cloud-native
- **Developpeur-CSharp.chatmode.md** - C# et .NET moderne
- **PHP-Expert.chatmode.md** - Architecture PHP avancée
- **Laravel-Expert.chatmode.md** - Framework Laravel
- **Symfony-Expert.chatmode.md** - Framework Symfony enterprise

**Frontend (2) :**
- **Developpeur-React.chatmode.md** - React moderne avec hooks
- **Developpeur-Angular.chatmode.md** - Angular avec TypeScript

**API/Architecture (1) :**
- **API-Expert.chatmode.md** - APIs REST/GraphQL et microservices

### 📋 Instructions et Standards (9)
- **security-owasp.instructions.md** - Standards de sécurité OWASP Top 10
- **rgaa-accessibility.instructions.md** - Accessibilité RGAA 4.1
- **pci-ssc.instructions.md** - Conformité PCI-SSC
- **api-standards.instructions.md** - Standards de développement d'APIs
- **php-standards.instructions.md** - Standards PHP modernes
- **laravel-standards.instructions.md** - Bonnes pratiques Laravel
- **symfony-standards.instructions.md** - Standards Symfony enterprise
- **java-spring-boot.instructions.md** - Développement Spring Boot
- **dependency-manager.instructions.md** - Gestion des dépendances

### Technologies Couvertes
- **Backend :** Java (Spring Boot, Quarkus), PHP (Laravel, Symfony), C# (.NET)
- **Frontend :** React, Angular, TypeScript
- **Architecture :** APIs REST/GraphQL, Microservices, DDD, Cloud-Native
- **Standards :** Sécurité OWASP, Accessibilité RGAA, PCI-SSC
- **Processus :** Analyse CDC, Tests, Documentation, Code Review

*Dernière mise à jour : 10 novembre 2025*