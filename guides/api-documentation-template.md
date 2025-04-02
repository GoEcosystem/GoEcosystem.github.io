---
layout: guide
title: API Documentation Template Guide
description: How to implement standardized API documentation across GoEcosystem projects
repo_name: GoEcosystem.github.io
related_guides:
  - title: GitHub Pages Best Practices
    url: /guides/github-pages-best-practices/
  - title: Jekyll for Documentation
    url: /guides/jekyll-for-documentation/
---

# API Documentation Template Guide

This guide provides a comprehensive template and instructions for implementing standardized API documentation across all GoEcosystem projects. Following these guidelines ensures consistency, reliability, and a great developer experience.

## Hybrid Approach Overview

GoEcosystem uses a hybrid approach for API documentation which combines both Jekyll Markdown processing and direct HTML:

1. **Jekyll Markdown File**: The primary documentation source, using Jekyll front matter and Markdown format.
2. **HTML Fallback File**: A direct HTML version that serves as a fallback if Jekyll processing fails.

This approach ensures documentation is always accessible, even if there are Jekyll build issues.

## Directory Structure

For each repository, your API documentation should follow this structure:

```
your-repository/
├── docs/
│   ├── _layouts/
│   │   └── api.html          # Custom layout extending default layout
│   ├── api/
│   │   ├── index.md          # Jekyll Markdown version
│   │   └── index.html        # Direct HTML fallback
│   └── _config.yml           # Jekyll configuration
```

## Jekyll Markdown Implementation

The `index.md` file should use the following template:

```markdown
---
layout: api
title: API Documentation
description: API reference for [Your Repository Name]
---

# API Documentation

[Repository Name] provides a RESTful API for [brief description]. This documentation covers all the available endpoints and how to use them.

## Base URL

When running locally:
```
http://localhost:8080/api
```

## Authentication

[Authentication details - if any]

## Endpoints

### Resource Group Name

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/resource` | List all resources |
| GET | `/api/resource/:id` | Get a specific resource |
| POST | `/api/resource` | Create a new resource |
| PUT | `/api/resource/:id` | Update a resource |
| DELETE | `/api/resource/:id` | Delete a resource |

#### List Resources

```
GET /api/resource?page=1&limit=20
```

Query Parameters:
- `page`: Page number (default: 1)
- `limit`: Number of items per page (default: 20)

Response:
```json
{
  "data": [
    {
      "id": 1,
      "name": "Example resource",
      "created_at": "2025-03-30T15:42:31Z"
    },
    ...
  ],
  "pagination": {
    "total": 42,
    "page": 1,
    "limit": 20,
    "totalPages": 3
  }
}
```

[Additional endpoint documentation following the same pattern...]

## Status Codes

The API uses standard HTTP status codes:

- `200 OK`: Request successful
- `201 Created`: Resource created successfully
- `400 Bad Request`: Invalid request parameters
- `401 Unauthorized`: Authentication failed
- `403 Forbidden`: Permission denied
- `404 Not Found`: Resource not found
- `500 Internal Server Error`: Server error
```

## HTML Fallback Implementation

The HTML fallback file should be a standalone file that contains all necessary styles and content. While the specific implementation will vary, it should:

1. Include all content from the Markdown version
2. Embed all necessary CSS directly in the file
3. Match the styling of the Jekyll-processed version
4. Be accessible without any Jekyll processing

## Custom API Layout

Create a custom API layout in `_layouts/api.html` that extends the default layout:

```html
---
layout: default
---

<div class="api-documentation">
  {{ content }}
</div>

<style>
  /* API Documentation specific styling */
  .api-documentation {
    max-width: 900px;
    margin: 0 auto;
    padding: 0 1rem;
  }
  
  /* Additional API-specific styling... */
</style>
```

## Implementation Checklist

- [ ] Create standard directory structure
- [ ] Implement Jekyll Markdown version with correct front matter
- [ ] Create HTML fallback version
- [ ] Add custom API layout
- [ ] Test both versions for proper rendering
- [ ] Ensure all links work correctly
- [ ] Update navigation and cross-references

## Terminal Commands Reference

Here are the commands to set up standardized API documentation:

```bash
# Create necessary directories
mkdir -p docs/api docs/_layouts

# Create Jekyll Markdown version
cat > docs/api/index.md << EOF
---
layout: api
title: API Documentation
---

# API Documentation
...
EOF

# Create custom API layout
cat > docs/_layouts/api.html << EOF
---
layout: default
---

<div class="api-documentation">
  {{ content }}
</div>

<style>
  /* API styles here */
</style>
EOF

# Create HTML fallback version
# (Create a standalone HTML file that includes all styling)

# Commit changes
git add docs/api/index.md docs/api/index.html docs/_layouts/api.html
git commit -m "Implement standardized API documentation with hybrid approach"
git push
```

## Best Practices

1. **Keep in Sync**: Always update both the Markdown and HTML versions when making changes
2. **Modular Approach**: Break down complex APIs into logical sections
3. **Examples**: Include request/response examples for every endpoint
4. **Status Codes**: Document all possible status codes and response formats
5. **Styling**: Use the standard GoEcosystem API styling for consistency

## Troubleshooting

### Common Issues and Solutions

- **Jekyll Front Matter Not Processing**: Ensure there's no extra whitespace before the `---` markers
- **HTML Fallback Not Working**: Check that the HTML file includes all necessary CSS
- **Styling Inconsistencies**: Compare with other repositories to ensure consistent styling
- **Missing Elements in ToC**: Make sure headings have the proper hierarchy (h1, h2, h3)

## Need Help?

If you have questions or need assistance, please:

1. Check existing documentation in the GoEcosystem repositories
2. Open an issue in the relevant repository
3. Contact the GoEcosystem documentation team

Happy documenting!

<style>
  /* Guide-specific styling */
  .implementation-steps {
    counter-reset: step-counter;
    list-style-type: none;
    padding-left: 0;
  }
  
  .implementation-steps li {
    counter-increment: step-counter;
    padding-left: 2.5rem;
    position: relative;
    margin-bottom: 1.5rem;
  }
  
  .implementation-steps li::before {
    content: counter(step-counter);
    position: absolute;
    left: 0;
    top: 0;
    width: 1.8rem;
    height: 1.8rem;
    background-color: var(--primary-color);
    color: white;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
  }
</style>
