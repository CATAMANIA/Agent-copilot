---
mode: "agent"
tools: ['search/codebase', 'edit/editFiles', 'usages', 'memory']
description: "Refactor procedural PHP code into an object-oriented class."
---

## Task: Refactor Procedural PHP to an Object-Oriented Class
You are an expert software architect specializing in modernizing legacy code. Analyze the selected procedural PHP code (#selection) and refactor it into a modern, well-structured, object-oriented class.

## User Input:
Provide the procedural PHP code that needs to be refactored into an object-oriented class. This can include:
- Standalone PHP scripts with functions
- Procedural code with global variables
- Legacy PHP code without proper structure
- Functions that work with related data
- Script files that mix logic and presentation

Example format:
```php
// Procedural code here
$users = [];

function addUser($name, $email) {
    global $users;
    $users[] = ['name' => $name, 'email' => $email];
}

function getUserByEmail($email) {
    global $users;
    foreach ($users as $user) {
        if ($user['email'] === $email) {
            return $user;
        }
    }
    return null;
}
```

## Refactoring Guidelines:
- Class Design: Create a new class that encapsulates the logic from the procedural script. The class name should reflect its primary purpose.
- Single Responsibility Principle: Adhere strictly to the Single Responsibility Principle. If the script performs multiple distinct tasks, identify the primary one for this class and note other responsibilities that could be extracted into separate classes.

## State and Behavior:

- Convert global variables and script-level state into private class properties.
- Convert standalone functions into class methods. Logic internal to the class's operation should become private methods.
- Modern PHP: The refactored class MUST use modern PHP 8.x features
- Apply declare(strict_types=1);.
- Add strict type hints to all properties, method arguments, and return types.
- Use constructor property promotion if applicable.
- Documentation: Add complete PHPDoc blocks to the class and all public methods.

## Output: 
- Provide the complete, refactored class code. Follow it with a brief explanation of the changes made and the architectural reasoning behind them.

## Response Format:

### 🔄 Refactored Class Code
```php
<?php

declare(strict_types=1);

// Complete refactored class implementation
```

### 📋 Refactoring Summary
Brief explanation of:
- Main architectural changes made
- How global state was converted to class properties
- How functions were converted to methods
- Modern PHP features applied
- Design patterns or principles followed

### 🎯 Key Improvements
- **Encapsulation**: How data and behavior are now properly encapsulated
- **Type Safety**: Type hints and strict typing implementation
- **Maintainability**: How the code is now easier to maintain and extend
- **Testability**: How the class design improves testability

### 💡 Further Refactoring Opportunities
If applicable, suggest additional improvements:
- Interface extraction opportunities
- Dependency injection possibilities
- Additional classes that could be extracted
- Design patterns that could be applied

## Modern PHP Features to Apply:
- `declare(strict_types=1)`
- Constructor property promotion
- Typed properties and method signatures
- Return type declarations
- Null coalescing and nullsafe operators
- Match expressions (where appropriate)
- Readonly properties (for immutable data)
- Enums (for constants)

## Object-Oriented Principles:
- **Encapsulation**: Bundle data and methods that operate on that data
- **Single Responsibility**: Each class should have one reason to change
- **Composition over Inheritance**: Prefer object composition
- **Dependency Inversion**: Depend on abstractions, not concretions

## Common Procedural to OOP Transformations:
- Global variables → Private class properties
- Functions → Public/private methods
- Include/require → Dependency injection
- Procedural error handling → Exception throwing
- Mixed concerns → Separated responsibilities

## Validation Checklist:
- ✅ All global state converted to class properties
- ✅ All functions converted to appropriate methods
- ✅ Strict typing implemented throughout
- ✅ PHPDoc documentation added
- ✅ Single Responsibility Principle followed
- ✅ Modern PHP features utilized
- ✅ Proper encapsulation achieved