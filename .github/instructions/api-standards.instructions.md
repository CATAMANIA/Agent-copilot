---
description: 'API development standards and best practices'
applyTo: '**/*.php'
---

# API Development Standards

## API Design Philosophy
- Design APIs as products with clear value propositions and user experiences.
- Follow API-first development approach with contract-driven design.
- Prioritize consistency, predictability, and developer experience.
- Design for scale, security, and maintainability from the beginning.
- Apply progressive disclosure principles for API complexity management.

## RESTful API Standards
- Use HTTP methods semantically (GET for retrieval, POST for creation, PUT/PATCH for updates, DELETE for removal).
- Design resource-oriented URLs with consistent naming conventions (nouns, not verbs).
- Use proper HTTP status codes to communicate operation results accurately.
- Implement HATEOAS (Hypermedia as the Engine of Application State) for API discoverability.
- Apply proper resource nesting and relationship representation.
- Use query parameters for filtering, sorting, and pagination consistently.

## HTTP Status Code Usage
- 200 OK: Successful GET, PUT, PATCH operations
- 201 Created: Successful POST operations that create resources
- 204 No Content: Successful DELETE operations or PUT operations with no response body
- 400 Bad Request: Invalid request syntax or parameters
- 401 Unauthorized: Authentication required or failed
- 403 Forbidden: Authenticated but not authorized for the resource
- 404 Not Found: Resource does not exist
- 422 Unprocessable Entity: Valid request syntax but semantic errors
- 429 Too Many Requests: Rate limit exceeded
- 500 Internal Server Error: Unexpected server error

## Request/Response Format Standards
- Use JSON as the primary data format with proper Content-Type headers.
- Implement consistent response structure with data, meta, and error sections.
- Use camelCase for JSON property names for consistency.
- Apply proper null value handling and optional field representation.
- Use ISO 8601 format for timestamps and dates.
- Implement proper boolean value representation (true/false, not 1/0).

## API Versioning Strategies
- Use URL path versioning (api/v1/users) for major version changes.
- Implement header-based versioning for minor changes and feature flags.
- Apply semantic versioning principles (major.minor.patch) for API versions.
- Maintain backward compatibility within major versions.
- Provide proper deprecation notices and migration guides.
- Use API version negotiation for client-specific responses.

## Authentication and Authorization
- Implement OAuth 2.0 or JWT tokens for stateless authentication.
- Use API keys for service-to-service authentication.
- Apply proper token validation and refresh mechanisms.
- Implement role-based access control (RBAC) for fine-grained permissions.
- Use HTTPS everywhere for secure token transmission.
- Apply proper token expiration and revocation strategies.
- Implement rate limiting per user/API key to prevent abuse.

## Input Validation and Sanitization
- Validate all input data against defined schemas and business rules.
- Use whitelist validation approaches rather than blacklist filtering.
- Implement proper type checking and format validation.
- Apply input length limits and character set restrictions.
- Sanitize data appropriately for the intended use context.
- Use framework validation libraries for consistent rule application.

## Error Handling and Responses
- Return consistent error response structures across all endpoints.
- Include meaningful error codes and messages for client debugging.
- Apply proper error logging without exposing internal system details.
- Use appropriate HTTP status codes for different error types.
- Implement proper validation error responses with field-level details.
- Provide correlation IDs for error tracking and support.

## API Documentation Standards
- Use OpenAPI 3.0+ specification for comprehensive API documentation.
- Include detailed parameter descriptions, examples, and constraints.
- Document all possible response codes and their meanings.
- Provide interactive API explorers for developer testing.
- Include authentication and authorization requirements clearly.
- Maintain up-to-date documentation with each API change.
- Include SDK and code examples for common use cases.