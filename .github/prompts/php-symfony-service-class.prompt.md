---
mode: "agent"
tools: ['search/codebase', 'edit/editFiles', 'usages', 'memory']
description: "Generate a Symfony service class with specified dependencies and methods."
---

## Task: Generate a Symfony Service Class
You are a Symfony framework expert. Your task is to create a new service class based on the name and dependencies provided by the user.

## User Input:
The user will invoke this prompt like /symfony-service-class serviceName=MyNewService dependencies="LoggerInterface,EntityManagerInterface".

## Generation Steps:
- Create Service Class: Generate a new PHP class file in the src/Service/ directory named MyNewService.php.
- Namespace and Imports: The class MUST have the namespace App\Service. It MUST import all specified dependency interfaces.
- Dependency Injection: The dependencies (LoggerInterface, EntityManagerInterface) MUST be injected via the constructor. Use constructor property promotion. The properties should be private readonly.
- Boilerplate Method: Include a public method named execute() as a placeholder for the service's logic.
- PHPDoc: The class and all methods must be fully documented with PHPDoc blocks.

## Output: 
- Provide the complete code for the src/Service/MyNewService.php file in a single code block.

## Symfony Service Structure:
```php
<?php

declare(strict_types=1);

namespace App\Service;

use Doctrine\ORM\EntityManagerInterface;
use Psr\Log\LoggerInterface;

/**
 * MyNewService
 * 
 * Service description here.
 */
class MyNewService
{
    /**
     * MyNewService constructor.
     */
    public function __construct(
        private readonly LoggerInterface $logger,
        private readonly EntityManagerInterface $entityManager,
    ) {
    }

    /**
     * Execute the service logic.
     */
    public function execute(): void
    {
        $this->logger->info('MyNewService::execute() called');
        
        // TODO: Implement service logic here
    }
}
```

## Symfony Best Practices:
- Use constructor property promotion for dependency injection
- Mark injected dependencies as `private readonly`
- Add proper PHPDoc blocks for the class and methods
- Use strict types declaration
- Follow PSR-4 autoloading standard
- Include logging for debugging and monitoring
- Use proper namespacing (App\Service)

## Common Symfony Dependencies:
- `LoggerInterface` for logging
- `EntityManagerInterface` for Doctrine ORM
- `EventDispatcherInterface` for events
- `ParameterBagInterface` for configuration
- `Security` for authentication/authorization
- `TranslatorInterface` for translations
- `Mailer` for sending emails
- `CacheInterface` for caching
- `HttpClientInterface` for HTTP requests
- `ValidatorInterface` for validation

## Service Configuration:
The generated service will be auto-configured by Symfony's dependency injection container. No additional configuration is needed unless you require specific settings.

## Response Format:

### 📄 Generated Service Class
```php
// Complete PHP service class code
```

### 📋 Service Details
- **Class Name**: Name of the generated service class
- **Namespace**: App\Service
- **Dependencies**: List of injected dependencies
- **Methods**: Description of included methods
- **Usage**: How to use this service in controllers or other services

### 🔧 Configuration Notes
- Auto-configuration: The service will be automatically registered
- Dependency Injection: All dependencies will be auto-wired
- Service ID: The service can be injected using the class name

## Usage Examples:
```php
// In a controller
public function someAction(MyNewService $myService): Response
{
    $myService->execute();
    return new Response('Success');
}

// In another service
public function __construct(
    private readonly MyNewService $myService,
) {
}
```