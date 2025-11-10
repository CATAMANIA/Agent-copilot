---
applyTo: "**"
---

# OWASP Security Standards

Cette instruction couvre les vulnérabilités de sécurité OWASP Top 10 et les meilleures pratiques pour les prévenir et les résoudre.

## OWASP Top 10 2021 - Résolutions et Préventions

### A01:2021 – Broken Access Control (Contrôle d'Accès Défaillant)

#### Vulnérabilités Communes
- Violation du principe de moindre privilège
- Contournement des vérifications d'autorisation
- Manipulation d'URL pour accéder à des ressources non autorisées
- Élévation de privilèges

#### Solutions et Préventions
```java
// ❌ MAUVAIS - Pas de vérification d'autorisation
@GetMapping("/users/{userId}")
public User getUser(@PathVariable Long userId) {
    return userService.findById(userId);
}

// ✅ BON - Vérification d'autorisation appropriée
@GetMapping("/users/{userId}")
@PreAuthorize("hasRole('ADMIN') or authentication.name == @userService.findById(#userId).username")
public User getUser(@PathVariable Long userId, Authentication auth) {
    return userService.findById(userId);
}
```

**Règles de mise en œuvre :**
- Implémenter un contrôle d'accès centralisé et cohérent
- Utiliser l'annotation `@PreAuthorize` ou `@Secured` pour chaque endpoint
- Vérifier les autorisations côté serveur, jamais uniquement côté client
- Appliquer le principe de moindre privilège par défaut
- Journaliser tous les échecs d'authentification et d'autorisation

### A02:2021 – Cryptographic Failures (Défaillances Cryptographiques)

#### Vulnérabilités Communes
- Données sensibles transmises en clair
- Algorithmes de chiffrement faibles ou obsolètes
- Clés de chiffrement faibles ou mal gérées
- Absence de chiffrement des données sensibles

#### Solutions et Préventions
```java
// ❌ MAUVAIS - Stockage de mot de passe en clair
public void saveUser(String password) {
    user.setPassword(password); // Stockage en clair
}

// ✅ BON - Hashage sécurisé avec BCrypt
@Autowired
private PasswordEncoder passwordEncoder;

public void saveUser(String password) {
    String hashedPassword = passwordEncoder.encode(password);
    user.setPassword(hashedPassword);
}
```

**Configuration sécurisée :**
```properties
# Configuration Spring Security pour chiffrement
spring.security.password.encoder=bcrypt
spring.security.password.encoder.strength=12

# Configuration HTTPS obligatoire
server.ssl.enabled=true
server.ssl.protocol=TLS
server.ssl.enabled-protocols=TLSv1.2,TLSv1.3
```

**Règles de mise en œuvre :**
- Utiliser uniquement des algorithmes cryptographiques approuvés (AES-256, RSA-2048+)
- Implémenter HTTPS partout avec TLS 1.2+
- Utiliser BCrypt ou Argon2 pour le hashage des mots de passe
- Ne jamais stocker de clés de chiffrement dans le code source
- Chiffrer toutes les données sensibles en base et en transit

## Règles Générales de Sécurité

### Validation d'Entrée
- Toujours valider côté serveur, jamais uniquement côté client
- Utiliser le principe de liste blanche (allowlist) plutôt que blacklist
- Encoder les sorties selon le contexte (HTML, JavaScript, SQL)
- Limiter la taille et le format des données d'entrée

Cette instruction doit être appliquée à tous les développements pour garantir un niveau de sécurité conforme aux standards OWASP.