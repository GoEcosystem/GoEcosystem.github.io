---
layout: guide
title: GitHub Pages Best Practices
description: Modern approaches to GitHub Pages using GitHub Actions and Jekyll
repo_name: GoEcosystem.github.io
related_guides:
  - title: API Documentation Template
    url: /guides/api-documentation-template/
  - title: Jekyll for Documentation
    url: /guides/jekyll-for-documentation/
---

# GitHub Pages Best Practices

This guide provides modern best practices for setting up, configuring, and deploying GitHub Pages sites using GitHub Actions and Jekyll.

## What is GitHub Pages

GitHub Pages is a static site hosting service that takes HTML, CSS, and JavaScript files directly from a repository on GitHub, optionally runs the files through a build process, and publishes a website. You can host your site on GitHub's `github.io` domain or your own custom domain.

## Setting Up GitHub Pages

### GitHub Actions Deployment Method (Recommended)

The recommended approach for deploying GitHub Pages sites is using GitHub Actions workflows, which offers more flexibility and control.

1. Create a new repository or use an existing one
2. Navigate to Settings > Pages
3. Under "Build and deployment", select "GitHub Actions" as the source
4. GitHub will suggest workflow templates, or you can create a custom one

### Jekyll Configuration

For Jekyll sites, create a `_config.yml` file in the root of your repository:

```yaml
# Site settings
title: Your Project Title
description: A short description of your project
show_downloads: true # Set to false to hide download buttons

# Theme settings
remote_theme: pages-themes/cayman@v0.2.0 # Or another supported theme
plugins:
  - jekyll-remote-theme
  - jekyll-relative-links # Converts relative links to markdown files
  - jekyll-seo-tag # For better SEO
```

### Project Structure

A typical structure for a GitHub Pages site with Jekyll:

```
├── .github/
│   └── workflows/
│       └── pages.yml
├── _layouts/
│   ├── default.html
│   └── container.html
├── assets/
│   └── css/
│       └── style.scss
├── _config.yml
├── Gemfile
├── README.md
└── index.md
```

## GitHub Actions for Deployment

Using GitHub Actions for deployment is the modern approach that provides more flexibility and control over the build process. Create a `.github/workflows/pages.yml` file:

```yaml
name: GitHub Pages

on:
  push:
    branches:
      - main
  workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow one concurrent deployment
concurrency:
  group: "pages"
  cancel-in-progress: true

jobs:
  # Build job
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      
      - name: Setup Pages
        id: pages
        uses: actions/configure-pages@v4
      
      - name: Setup Ruby
        uses: ruby/setup-ruby@v1
        with:
          ruby-version: '3.2'
          bundler-cache: true
      
      - name: Install dependencies
        run: |
          gem install bundler
          bundle install
      
      - name: Build with Jekyll
        run: bundle exec jekyll build
        env:
          JEKYLL_ENV: production
      
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: '_site'

  # Deployment job
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

## Theme Customization

### Creating a Custom Theme

To create a custom theme, you can override the default theme styles:

1. Create an `assets/css/style.scss` file
2. Add the following content:

```scss
---
---

@import "{{ site.theme }}";

// Your custom styles here
body {
  font-family: 'Inter', -apple-system, sans-serif;
}

.page-header {
  background-color: #00ADD8; // Go blue color
}
```

### Modifying Navigation

To modify the navigation, you can override the default layout:

1. Create a `_layouts/default.html` file
2. Copy the content from the theme's default layout
3. Modify the navigation section:

```html
<header class="site-header">
  <div class="container">
    <a href="{{ '/' | relative_url }}" class="site-logo">
      <span class="logo-text">{{ site.title }}</span>
    </a>
    <nav class="site-nav">
      <ul>
        {% for item in site.navigation %}
        <li>
          <a href="{{ item.url | relative_url }}" {% if page.url == item.url %}class="active"{% endif %}>
            {{ item.title }}
          </a>
        </li>
        {% endfor %}
      </ul>
    </nav>
  </div>
</header>
```

## Adding a Hero Section

A hero section is a large, visually striking area at the top of a page that typically includes a heading, subheading, and call-to-action:

```html
<div class="hero-section">
  <h1>{{ page.title }}</h1>
  <p class="hero-subtitle">{{ page.description }}</p>
  <div class="hero-buttons">
    <a href="{{ page.cta_primary_url }}" class="btn btn-primary btn-lg">{{ page.cta_primary_text }}</a>
    <a href="{{ page.cta_secondary_url }}" class="btn btn-secondary btn-lg">{{ page.cta_secondary_text }}</a>
  </div>
</div>
```

## Using Card Components

Cards are versatile UI components that can be used to display content in a visually appealing way:

```html
<div class="card-grid">
  {% for item in site.data.features %}
  <div class="card">
    <h3>{{ item.title }}</h3>
    <p>{{ item.description }}</p>
    <a href="{{ item.url }}" class="btn btn-primary">{{ item.button_text }}</a>
  </div>
  {% endfor %}
</div>
```

## Troubleshooting

### Common Issues and Solutions

- **GitHub Pages Not Building**: Check your workflow permissions
- **Jekyll Build Errors**: Look for syntax errors or missing dependencies
- **CSS Not Loading**: Check the path to your CSS files
- **Images Not Displaying**: Use relative paths with the `{{ site.baseurl }}` prefix

### Debugging Tips

- Use the Actions tab to see workflow logs
- Test your site locally with `bundle exec jekyll serve`
- Check your site structure against the recommended patterns

## Conclusion

By following these best practices, you'll be able to create a modern, maintainable GitHub Pages site that leverages the power of GitHub Actions and Jekyll.

### Next Steps

- Explore advanced Jekyll features like collections and data files
- Implement a search functionality for your documentation
- Add custom JavaScript for interactive elements

### Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
