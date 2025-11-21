## Blade template conventions

### Component Organization
- Use Blade components for reusable UI elements
- Follow existing component patterns in project
- Keep components small and focused
- Use slots for flexible content injection

### Naming Conventions
- Component files: kebab-case (e.g., `user-card.blade.php`)
- Component usage: `<x-user-card />`
- Prefix project-specific components appropriately

### TailwindCSS Integration
- Use Tailwind utility classes directly in Blade
- Follow TailwindCSS 4.0+ conventions
- Extract repeated patterns into Blade components
- Use `@apply` sparingly - prefer utility classes

### Data Passing
- Use named parameters for component props
- Type-hint component properties when possible
- Use `@props` directive for component attributes
- Provide sensible defaults for optional props

### Directives
- Use `@auth`, `@guest` for authentication checks
- Use `@can` for authorization checks
- Use `@error` for validation error display
- Prefer Blade directives over inline PHP where available

### Asset Management
- Reference assets using `@vite` directive
- Use named routes with `route()` helper
- Generate URLs with `url()` or `asset()` helpers

### Performance
- Use `@once` directive to prevent duplicate asset loading
- Minimize inline JavaScript - prefer separate files
- Lazy load images below the fold
