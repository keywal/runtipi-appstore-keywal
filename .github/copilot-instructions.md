# Copilot Instructions for RunTipi AppStore

## Project Overview
This is a custom app store for RunTipi that provides additional applications not available in the standard Tipi Store. The project follows RunTipi's app store specification and is built using TypeScript/Bun.

## Key Components and Structure

### Apps Directory (`/apps/`)
- Each subdirectory represents a single application (e.g., `autokuma`, `gomft`, etc.)
- Required files for each app:
  - `config.json`: App metadata and configuration schema
  - `docker-compose.json`: Container configuration
  - `metadata/`: Contains `logo.jpg` and `description.md`

### Configuration Structure
- App configurations (`config.json`) must follow the `appInfoSchema` from `@runtipi/common/schemas`
- Key fields:
  ```json
  {
    "name": "App Name",
    "id": "unique-id",
    "port": 1234,
    "categories": ["category"],
    "tipi_version": 2,
    "form_fields": [
      {
        "type": "text|password|number",
        "label": "Field Label",
        "env_variable": "ENV_VAR_NAME"
      }
    ]
  }
  ```

## Development Workflow

### Testing
- Run tests with `bun test`
- Tests verify:
  1. Required files exist for each app
  2. Valid `config.json` schema
  3. Valid `docker-compose.json` schema

### Adding New Apps
1. Create app directory in `/apps/`
2. Include required files following existing apps as templates
3. Ensure logo.jpg and description.md are present in metadata/
4. Test configuration validity before committing

## Common Patterns
- Use environment variables for configuration (`form_fields.env_variable`)
- Support both amd64 and arm64 architectures when possible
- Include clear descriptions and source URLs in config.json
- Follow semantic versioning for app versions

## Integration Points
- Integrates with RunTipi's app management system
- Each app must expose its main service on a configurable port
- Docker labels used for service discovery (see AutoKuma implementation)

## Reference Examples
- `apps/autokuma/`: Example of form field configuration
- `apps/tsdproxy/`: Example of proxy service integration
- `__tests__/apps.test.ts`: Test patterns and validation