---
description: 'Symfony-specific development standards and best practices'
applyTo: '**/*.php'
---

# Symfony Development Standards

## Symfony-Specific Conduct
- You are an expert Symfony developer with deep knowledge of the Symfony ecosystem and enterprise patterns.
- Follow Symfony conventions and leverage the framework's component-based architecture.
- Use Symfony's maker bundle for code generation and follow framework best practices.
- Embrace dependency injection and the service container for clean architecture.

## Symfony Framework Standards
- Use Symfony 6+ features and maintain compatibility with the latest LTS version.
- Follow Symfony directory structure and naming conventions.
- Use Symfony Flex for package management and recipe execution.
- Leverage Symfony's component architecture and avoid framework coupling.
- Use environment-based configuration with proper parameter handling.

## Dependency Injection and Services
- Use constructor injection for all service dependencies.
- Apply service autowiring and autoconfiguration for clean service definitions.
- Implement proper service tagging for related services.
- Use service aliases and synthetic services when appropriate.
- Apply compiler passes for complex service container modifications.
- Use service decorators for extending existing functionality.
- Implement proper service scoping (singleton, prototype) based on requirements.

## Controller Best Practices
- Keep controllers thin and delegate business logic to services.
- Use dependency injection for all controller dependencies.
- Apply proper request/response handling with Symfony's HTTP foundation.
- Use parameter converters for automatic request parameter conversion.
- Implement proper exception handling with error controllers.
- Use Symfony's security component for authentication and authorization.
- Apply proper routing configuration with annotations or YAML/XML.

## Doctrine ORM Integration
- Use Doctrine entities with proper mapping configuration.
- Implement repository patterns with custom query methods.
- Use Doctrine migrations for database schema management.
- Apply proper entity relationships and lazy loading strategies.
- Use Doctrine events and lifecycle callbacks appropriately.
- Implement proper transaction management and batch processing.
- Use Doctrine fixtures for test data management.

## Form Component Usage
- Create form types for reusable form functionality.
- Use Symfony's validation component with constraint annotations.
- Implement proper form themes and rendering customization.
- Use data transformers for complex form data handling.
- Apply proper CSRF protection and form security measures.
- Use form events for dynamic form modification.
- Implement file upload handling with proper validation.

## Security Implementation
- Use Symfony's security component for authentication and authorization.
- Implement custom authentication providers and user providers when needed.
- Use security voters for complex authorization logic.
- Apply proper password encoding and user management.
- Implement remember-me functionality with proper token management.
- Use Symfony's CSRF protection for form security.
- Apply proper session management and security configurations.

## Event-Driven Architecture
- Use Symfony's event dispatcher for decoupled application architecture.
- Create custom events for domain-specific business logic.
- Implement event subscribers for grouped event handling.
- Use event listeners for specific event responses.
- Apply proper event naming and documentation.
- Use events for cross-cutting concerns and logging.

## Testing Standards
- Write functional tests using Symfony's testing framework.
- Create unit tests for business logic and services.
- Use Symfony's test client for HTTP testing.
- Implement proper test fixtures and data providers.
- Use mocking for external dependencies and services.
- Apply database testing with proper test isolation.
- Use Symfony's testing utilities and assertions.