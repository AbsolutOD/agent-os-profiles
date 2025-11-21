## Tech stack

Laravel-specific technical stack preferences. Inherits from default profile and adds Laravel-specific conventions.

### Framework & Runtime
- **Application Framework:** Laravel 12+ (unless project uses older version)
- **Language/Runtime:** PHP 8.4+
- **Package Manager:** Composer (PHP), npm/bun (frontend, project dependent)
- **Build Tool:** Vite with Laravel plugin

### Frontend
- **CSS Framework:** TailwindCSS 4.0+

### Database & Storage
- **Database:** PostgreSQL 17+ (if no database configured)
- **ORM:** Laravel Eloquent
- **Caching:** Redis (project dependent)

### Testing & Quality
- **Test Framework:** Pest 4+
- **Code Formatting:** Laravel Pint
- **Type Safety:** Laravel Boost

### Deployment & Infrastructure
- **Hosting:** Laravel Forge on Digital Ocean
- **Database Hosting:** Digital Ocean Managed PostgreSQL
- **Database Backups:** Daily automated
- **Asset Storage:** Cloudflare R2
- **CDN:** Cloudflare
- **Production Environment:** main branch
- **Staging Environment:** staging branch

### Third-Party Services
- **Authentication:** Laravel Fortify or Breeze (project dependent)
- **Monitoring:** Laravel Pulse, Flare (project dependent)
r:** Eloquent
- **Caching:** Redis

### Testing & Quality
- **Test Framework:** Pest
- **Linting/Formatting:** ESLint, Typescript-ESLint, Prettier

### Deployment & Infrastructure
- **Hosting:** AWS
- **CI/CD:** GitHub Actions

### Third-Party Services
- **Authentication:** WorkOS
- **Email:** Mailgun
- **Monitoring:** Nightwatch
