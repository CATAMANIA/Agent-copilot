---
description: 'Laravel-specific development standards and best practices'
applyTo: '**/*.php'
---

# Laravel Development Standards

## Laravel-Specific Conduct
- You are an expert Laravel developer with deep knowledge of the Laravel ecosystem and best practices.
- Follow Laravel conventions and utilize the framework's built-in features effectively.
- Always use Artisan commands for file generation when available.
- Leverage Laravel's service container and dependency injection patterns.

## Laravel Framework Standards
- Use Laravel 10+ features and maintain compatibility with the latest LTS version.
- Follow Laravel naming conventions for all components (models, controllers, migrations, etc.).
- Use Laravel's directory structure and don't fight the framework conventions.
- Leverage Laravel's built-in features instead of reinventing functionality.

## Eloquent ORM Best Practices
- Use proper model relationships (hasMany, belongsTo, belongsToMany, etc.) with clear naming.
- Implement model accessors and mutators for data transformation.
- Use query scopes for reusable query logic and better code organization.
- Apply proper eager loading to prevent N+1 query problems.
- Use database transactions for operations that modify multiple tables.
- Implement soft deletes when data retention is required.
- Use model events and observers for cross-cutting concerns.
- Apply proper fillable and guarded properties for mass assignment protection.

## Controller Standards
- Use resource controllers for RESTful operations with proper HTTP methods.
- Keep controllers thin by moving business logic to service classes.
- Use form request classes for validation instead of inline validation.
- Apply proper middleware for authentication, authorization, and other concerns.
- Use route model binding for automatic model resolution.
- Return consistent response formats using API resources or response macros.
- Handle exceptions gracefully with proper error responses.

## Validation and Form Requests
- Create dedicated form request classes for complex validation rules.
- Use Laravel's built-in validation rules and create custom rules when needed.
- Implement proper error message customization for better user experience.
- Use validation rules that are database-aware (exists, unique) appropriately.
- Apply conditional validation rules based on request context.
- Validate file uploads with proper MIME type and size restrictions.

## API Development with Laravel
- Use API resources for consistent JSON response formatting.
- Implement Laravel Sanctum or Passport for API authentication.
- Apply proper rate limiting using Laravel's built-in throttling.
- Use API versioning strategies (URL or header-based).
- Implement proper CORS configuration for cross-origin requests.
- Use OpenAPI documentation with tools like Laravel OpenAPI.
- Apply proper HTTP status codes and error response formatting.

## Database and Migrations
- Write clear, descriptive migration names with timestamps.
- Use proper column types and constraints in migrations.
- Implement proper foreign key relationships with cascade options.
- Create database seeders for consistent test data.
- Use factory classes for generating test data with relationships.
- Apply proper indexing for query performance optimization.

## Security Best Practices
- Use Laravel's built-in CSRF protection for all forms.
- Implement proper authentication using Laravel's built-in guards.
- Use Laravel's authorization gates and policies for access control.
- Apply input sanitization and validation for all user input.
- Use Laravel's encryption services for sensitive data storage.
- Implement proper session security and cookie protection.
- Apply rate limiting and throttling for API endpoints and forms.

## Testing Standards
- Write feature tests for HTTP endpoints and user workflows.
- Create unit tests for business logic and service classes.
- Use Laravel's testing utilities and database testing features.
- Implement proper test data using factories and seeders.
- Use mocking and stubbing for external dependencies.
- Apply test-driven development practices where appropriate.
- Use PHPUnit assertions and Laravel-specific testing helpers.