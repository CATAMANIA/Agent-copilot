---
mode: "agent"
tools: ['search/codebase', 'edit/editFiles', 'usages', 'memory']
description: "Generate a complete Laravel CRUD controller for a specified resource."
---

## Task: Generate Laravel CRUD Controller
You are a Laravel expert. Your task is to generate a complete CRUD controller for the specified resource with all standard operations.

## User Input:
The user will invoke this prompt like `/laravel-crud resourceName=Product`. Generate the complete CRUD controller with all methods.

## Generation Steps:
- Create Controller: Generate a new Laravel resource controller in the app/Http/Controllers/ directory named ProductController.php.
- Include Methods: The controller MUST include all CRUD operations: index(), create(), store(), show(), edit(), update(), destroy().
- Form Requests: Reference appropriate form request classes for validation (e.g., StoreProductRequest, UpdateProductRequest).
- Resource Response: Use Laravel API resources for JSON responses when applicable.
- Authorization: Include policy checks using the authorize() method where appropriate.
- Eloquent Best Practices: Use proper Eloquent methods and relationships.

## Output:
- Provide the complete code for the app/Http/Controllers/ProductController.php file in a single code block.
- Include proper imports, namespace, and PHPDoc documentation.
- Follow Laravel conventions and best practices.

## Laravel Features to Include:
- Route model binding
- Form request validation
- Eloquent relationships
- API resource responses
- Proper HTTP status codes
- Exception handling
- Policy authorization checks

## Example Structure:
```php
<?php

namespace App\Http\Controllers;

use App\Http\Requests\StoreProductRequest;
use App\Http\Requests\UpdateProductRequest;
use App\Http\Resources\ProductResource;
use App\Models\Product;
use Illuminate\Http\Request;
use Illuminate\Http\Response;

/**
 * Class ProductController
 * 
 * Handles CRUD operations for Product resources.
 * 
 * @package App\Http\Controllers
 */
class ProductController extends Controller
{
    /**
     * Display a listing of the resource.
     */
    public function index(): Response
    {
        // Implementation
    }
    
    // ... other methods
}
```

## Validation and Security:
- Include proper validation using Form Requests
- Add authorization checks using policies
- Implement proper error handling
- Use mass assignment protection
- Include CSRF protection where needed