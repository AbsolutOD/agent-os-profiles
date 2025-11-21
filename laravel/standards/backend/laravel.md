## Laravel conventions

### Code Organization
- Follow Laravel's MVC pattern
- Use Service classes for complex business logic
- Keep controllers thin - delegate to services or actions
- Use Form Requests for validation
- Use Eloquent relationships with proper type hints

### Database & Models
- Always use proper Eloquent relationship methods with return type hints
- Prefer relationship methods over raw queries or manual joins
- Avoid `DB::`; prefer `Model::query()`
- Generate code that prevents N+1 query problems by using eager loading
- Use database migrations for all schema changes
- Model casts should be defined in `casts()` method (Laravel 11+)

### Routing
- Group related routes logically
- Use route model binding where applicable
- Name all routes for easier maintenance
- Use resource controllers for CRUD operations

### Validation
- Always create Form Request classes for validation
- Include both validation rules and custom error messages
- Check sibling Form Requests to see if project uses array or string based validation rules

### Queue & Jobs
- Use queued jobs for time-consuming operations with `ShouldQueue` interface
- Always implement proper error handling in jobs
- Use job batching for related operations

### Authentication & Authorization
- Use Laravel's built-in authentication features
- Implement authorization using Gates and Policies
- Use middleware for route protection

### Configuration
- Use environment variables only in configuration files
- Never use `env()` function directly outside of config files
- Always use `config('app.name')`, not `env('APP_NAME')`

### Artisan Commands
- Use `php artisan make:` commands to create new files
- Pass `--no-interaction` to all Artisan commands in scripts
- For generic PHP classes, use `artisan make:class`

### Laravel 11/12 Structure
- No middleware files in `app/Http/Middleware/`
- Use `bootstrap/app.php` to register middleware, exceptions, and routing
- `bootstrap/providers.php` contains application-specific service providers
- No `app/Console/Kernel.php` - use `bootstrap/app.php` or `routes/console.php`
- Commands auto-register from `app/Console/Commands/`

### API Development
- Use Eloquent API Resources for API responses
- Implement API versioning for public APIs
- Follow REST conventions for endpoints
- Use rate limiting on API routes

### Laravel Boost
- Use Laravel Boost to add recommended type declarations to your codebase
- Run `php artisan boost` to add types to models, controllers, and other classes
- Boost adds property types, return types, and parameter types automatically
- Use `--class` flag to target specific classes: `php artisan boost --class=User`
- Use `--dirty` flag to only check uncommitted changes: `php artisan boost --dirty`
- Run Boost before committing to maintain type safety
- Review Boost changes before committing to ensure accuracy
