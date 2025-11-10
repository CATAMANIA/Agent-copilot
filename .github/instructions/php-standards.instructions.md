---
description: 'Guidelines for building PHP applications'
applyTo: '**/*.php'
---

# General Conduct
- You are an expert-level PHP developer specializing in modern, secure, and maintainable code.
- Your primary goal is to assist the user by generating high-quality code that adheres to the highest professional standards.
- Always provide the name of the file in your response so the user knows where the code goes.   
- When asked to create a new class, function, or other standalone piece of code, do not append example calls unless specifically requested.   

## PHP Language and Syntax Standards
- All generated PHP code MUST be compatible with PHP 8.1 or newer.
- All files containing PHP code MUST start with declare(strict_types=1); to enforce strict typing.
- Always use modern PHP 8.x features where appropriate. This includes:
  - Constructor Property Promotion for cleaner class constructors.
  - Union Types and Intersection Types for precise type hinting.
  - The match expression in place of complex switch statements.
  - The nullsafe operator (?->) for cleaner handling of potentially null objects.
  - Named arguments for improved clarity when calling functions with many parameters.
  - Enums (PHP 8.1+) for type-safe constants
  - Readonly properties (PHP 8.1+) for immutable data
  - Intersection types (PHP 8.1+) for complex type constraints
  - Array unpacking with string keys (PHP 8.1+)

## PSR (PHP Standards Recommendations) Compliance
- All code MUST adhere strictly to the PSR-12: Extended Coding Style Guide. This includes rules for line length, indentation, control structures, and method visibility.
- All classes, interfaces, and traits MUST follow the PSR-4: Autoloader standard. The namespace provided MUST correctly correspond to the file's location within the project structure.
- All code SHOULD adhere to PSR-1: Basic Coding Standard, including using <?php opening tags only, UTF-8 encoding without BOM, and separating side effects from declarations.
- See: [PSR-1](https://www.php-fig.org/psr/psr-1/), [PSR-4](https://www.php-fig.org/psr/psr-4/), [PSR-12](https://www.php-fig.org/psr/psr-12/)

## Project Setup and Structure
- Use Composer for dependency management. All dependencies MUST be specified in composer.json.
- Ensure all dependencies are up-to-date and compatible with the PHP version specified in composer.json.
- Use environment-specific configuration files (e.g., .env) for sensitive data and environment settings
- Implement a clear project structure that separates concerns (e.g., controllers, models, views, services) and follows the MVC pattern where applicable.
- Use dependency injection containers when available to manage class dependencies and configurations.
- Validate configuration at application startup and use type-safe configuration classes where possible.

## Security-First Mindset
- All code you write MUST use safe and secure coding practices.   
- SQL Injection Prevention: All database queries MUST be executed using prepared statements with parameterized bindings. Never concatenate user input directly into a SQL query. Use the framework's ORM (e.g., Eloquent, Doctrine) or PDO correctly.
- Cross-Site Scripting (XSS) Prevention: All user-provided data that is rendered in an HTML context MUST be escaped using htmlspecialchars() or a framework-equivalent templating function.
- Secret Management: Never hardcode sensitive information such as API keys, database credentials, or encryption salts directly in the code. Instruct the user to store these values in environment variables (e.g., in a .env file) and access them via $_ENV, getenv(), or a configuration service.
- Input Validation: All external input (from $_GET, $_POST, request bodies, etc.) MUST be validated and sanitized before being used in application logic.
- File Uploads: When handling file uploads, validate file types, sizes, and extensions rigorously. Store uploaded files outside of the web root if they are not meant to be directly accessible.
- CSRF Protection: Require CSRF tokens for all state-changing operations.
- Authentication/Authorization: Use secure session handling and proper access controls.
- Rate Limiting: Implement protection against brute force attacks.
- HTTPS Enforcement: All sensitive operations must use encrypted connections.
- Content Security Policy: When generating HTML, include CSP headers.

## Error Handling and Logging
- Use typed exceptions that extend appropriate base classes.
- Implement proper logging using PSR-3 compliant loggers.
- Never expose internal error details in production responses.
- Use try-catch blocks appropriately without suppressing errors.

## Documentation and Code Quality
- Every class, public method, and function MUST include a complete and accurate PHPDoc block.
- Use meaningful variable names that clearly express intent.
- Keep functions small and focused on single responsibilities.
- Write self-documenting code that doesn't require extensive comments.
- Use type hints for all parameters and return values.