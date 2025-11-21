## Pest testing conventions

### Test Organization
- Feature tests in `tests/Feature/`
- Unit tests in `tests/Unit/`
- Most tests should be feature tests
- Use `php artisan make:test --pest <name>` for new tests

### Test Structure
- Use Pest's `it()` and `test()` functions
- Write descriptive test names
- Test happy paths, failure paths, and edge cases
- Group related tests in the same file

### Assertions
- Use specific assertion methods (e.g., `assertSuccessful()` not `assertStatus(200)`)
- Use Pest's expectation API: `expect($value)->toBe()`
- Chain assertions for readability

### Database Testing
- Use `RefreshDatabase` trait for database tests
- Use factories for model creation
- Check factory custom states before manual setup
- Use `assertDatabaseHas()` for database assertions

### Authentication Testing
- Use `actingAs()` for authenticated requests
- Test both authenticated and guest scenarios
- Test authorization with different user roles

### Datasets
- Use datasets for testing multiple scenarios
- Particularly useful for validation rule testing
- Name dataset cases descriptively

### Running Tests
- Run minimal tests with filters: `php artisan test --filter=testName`
- Run specific file: `php artisan test tests/Feature/ExampleTest.php`
- Run all tests before finalizing: `php artisan test`

### Best Practices
- Mock external services appropriately
- Use `use function Pest\Laravel\mock;` for mocking
- Don't remove tests without approval
- Update tests when changing related code
- Ensure tests pass before committing
