---
applyTo: "**/*"
---

# Java best practices

## Code Quality Expectations

- Use Maven as build tool.
- Follow SOLID principles.
- Use our coding conventions (naming, formatting, error handling).
- Use Zero Trust Architecture principles.
- Use Lombok to reduce boilerplate code.
- Use Java 17 features where applicable (e.g., records, sealed classes).
- Use Domain Driven Development method:
    - limit to the maximum the use of technology associated annotation (serialisation, persistence, etc..).
    - only lombok's annotations are allowed.
    - for HATEOAS implementation, the field `_links:` will be defined by the REST Controller.
- Follow our architecture (e.g., layered services, DTOs, repositories, controllers).
- Write for any feature tests (unit + integration):
    - Tests should cover edge case (malformed values, limit values, etc..)
    - Document with Javadoc: Every public method and class should have meaningful documentation.
- Prefer explicitness over hidden behavior: Avoid unnecessary abstractions that make the code harder to audit.
- Never create Utils classes.
- No dockerisation for the moment
- H2 database in local only
- Integration Test Classes name must end with "IT" (like existing AdminControllerIT.java class)
- If a class has to be annotated with @SpringbootTest, it is considered as an integration test, no need to duplicate it in the package for unit tests.

## Folder Structure
- `src/main/java`: Contains the main application code.
- `src/test/java`: Contains unit and integration tests.
- `src/main/resources`: Contains configuration files and other resources.
- IntegrationTest are defined in src/test/java and executed in a task `integTest`.