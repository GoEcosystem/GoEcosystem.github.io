# GoEcosystem Documentation Templates

This directory contains standardized templates for documentation across all GoEcosystem repositories. Using these templates ensures consistency in structure, style, and content organization across our projects.

## Available Templates

| Template | Description | Usage |
|----------|-------------|-------|
| [api-page-template.md](./api-page-template.md) | Template for API documentation pages | Copy this template when creating API reference documentation |
| [reference-page-template.md](./reference-page-template.md) | Template for technical reference documentation | Use for detailed component or feature references |
| [guide-page-template.md](./guide-page-template.md) | Template for guides and tutorials | Use when creating how-to guides or tutorials |
| [readme-template.md](./readme-template.md) | Standard README template for repositories | Copy as the base for your repository's README.md |
| [api_navigation.yml](./api_navigation.yml) | Template for API sidebar navigation | Copy to your repository's _data directory |

## How to Use These Templates

1. **Choose the Appropriate Template**: Select the template that best fits your documentation needs
2. **Copy to Your Repository**: Copy the template to the appropriate location in your repository
3. **Update Front Matter**: Edit the YAML front matter at the top of the file to match your repository and content
4. **Customize Content**: Replace placeholder content with your specific documentation
5. **Maintain Structure**: Keep the overall structure intact to ensure consistency

### Example: Creating API Documentation

```bash
# Copy the API template to your repository
cp /home/anubix/CODE/job_project/GoEcosystem.github.io/_templates/api-page-template.md /path/to/your-repo/docs/api/index.md

# Create the data directory and copy the navigation template
mkdir -p /path/to/your-repo/docs/_data
cp /home/anubix/CODE/job_project/GoEcosystem.github.io/_templates/api_navigation.yml /path/to/your-repo/docs/_data/api_navigation.yml

# Edit the files to customize for your repository
```

## Template Guidelines

When using these templates, follow these guidelines:

1. **Maintain Consistent Structure**: Keep the overall document structure intact
2. **Use Proper Front Matter**: Ensure all required front matter variables are set
3. **Follow Style Guidelines**: Adhere to the [documentation style guide](https://goecosystem.github.io/guides/documentation-style-guide/)
4. **Use Include Tags**: Utilize the standardized include components (breadcrumbs, sidebar, etc.)
5. **Test Locally**: Verify your documentation renders correctly before committing

## Notes for Template Maintainers

When updating these templates:

1. Document changes in the commit message
2. Update any related documentation to reflect template changes
3. Consider backward compatibility with existing documentation
4. Ensure templates follow current best practices in documentation
