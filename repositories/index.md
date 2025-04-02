---
layout: default
title: Repositories
description: Overview of all repositories in the GoEcosystem organization
---

# GoEcosystem Repositories

This page provides an overview of all repositories in the GoEcosystem organization, including their purpose, features, and documentation links.

## Featured Repositories

<div class="repo-featured">
  <div class="repo-card featured">
    <div class="repo-header">
      <h3>
        <a href="https://github.com/GoEcosystem/go-web-scraper">go-web-scraper</a>
        <span class="repo-language">Go</span>
      </h3>
      <div class="repo-stats">
        <span class="repo-stat"><i class="fa fa-star"></i> Stars</span>
        <span class="repo-stat"><i class="fa fa-code-fork"></i> Forks</span>
      </div>
    </div>
    <div class="repo-description">
      <p>A comprehensive web scraping solution built in Go, featuring concurrent scraping, database integration, and a responsive web interface.</p>
    </div>
    <div class="repo-features">
      <h4>Key Features</h4>
      <ul>
        <li>Multi-site scraping capabilities</li>
        <li>Concurrent processing using goroutines</li>
        <li>SQLite database integration</li>
        <li>Web interface with Bootstrap styling</li>
        <li>Export to JSON and CSV formats</li>
        <li>Ethical scraping with rate limiting</li>
      </ul>
    </div>
    <div class="repo-links">
      <a href="https://github.com/GoEcosystem/go-web-scraper" class="btn btn-secondary">GitHub Repository</a>
      <a href="https://goecosystem.github.io/go-web-scraper/" class="btn btn-primary">Documentation</a>
      <a href="https://goecosystem.github.io/go-web-scraper/api/" class="btn btn-primary">API Reference</a>
    </div>
  </div>
</div>

## All Repositories

<div class="repo-grid">
  <div class="repo-card">
    <div class="repo-header">
      <h3>
        <a href="https://github.com/GoEcosystem/go-template">go-template</a>
        <span class="repo-language">Go</span>
      </h3>
    </div>
    <div class="repo-description">
      <p>Standard template for Go projects with proper directory structure, GitHub workflows, and best practices.</p>
    </div>
    <div class="repo-links">
      <a href="https://github.com/GoEcosystem/go-template" class="btn btn-secondary">GitHub Repository</a>
      <a href="https://goecosystem.github.io/go-template/" class="btn btn-primary">Documentation</a>
    </div>
  </div>

  <div class="repo-card">
    <div class="repo-header">
      <h3>
        <a href="https://github.com/GoEcosystem/go-library-template">go-library-template</a>
        <span class="repo-language">Go</span>
      </h3>
    </div>
    <div class="repo-description">
      <p>Template for creating reusable Go libraries with examples, documentation, and best practices.</p>
    </div>
    <div class="repo-links">
      <a href="https://github.com/GoEcosystem/go-library-template" class="btn btn-secondary">GitHub Repository</a>
      <a href="https://goecosystem.github.io/go-library-template/" class="btn btn-primary">Documentation</a>
    </div>
  </div>

  <div class="repo-card">
    <div class="repo-header">
      <h3>
        <a href="https://github.com/GoEcosystem/go-utils">go-utils</a>
        <span class="repo-language">Go</span>
      </h3>
    </div>
    <div class="repo-description">
      <p>Collection of shared utilities for HTTP, database, logging, and configuration that can be used across Go projects.</p>
    </div>
    <div class="repo-links">
      <a href="https://github.com/GoEcosystem/go-utils" class="btn btn-secondary">GitHub Repository</a>
      <a href="https://goecosystem.github.io/go-utils/" class="btn btn-primary">Documentation</a>
      <a href="https://goecosystem.github.io/go-utils/api/" class="btn btn-primary">API Reference</a>
    </div>
  </div>

  <div class="repo-card">
    <div class="repo-header">
      <h3>
        <a href="https://github.com/GoEcosystem/go-docs">go-docs</a>
        <span class="repo-language">Markdown</span>
      </h3>
    </div>
    <div class="repo-description">
      <p>Organization-wide documentation and guidelines for GoEcosystem projects. Contains best practices, tutorials, and styleguides.</p>
    </div>
    <div class="repo-links">
      <a href="https://github.com/GoEcosystem/go-docs" class="btn btn-secondary">GitHub Repository</a>
      <a href="https://goecosystem.github.io/go-docs/" class="btn btn-primary">Documentation</a>
    </div>
  </div>

  <div class="repo-card">
    <div class="repo-header">
      <h3>
        <a href="https://github.com/GoEcosystem/go-cheatsheets">go-cheatsheets</a>
        <span class="repo-language">Markdown</span>
      </h3>
    </div>
    <div class="repo-description">
      <p>Quick reference guides for Go programming language syntax, patterns, and libraries.</p>
    </div>
    <div class="repo-links">
      <a href="https://github.com/GoEcosystem/go-cheatsheets" class="btn btn-secondary">GitHub Repository</a>
      <a href="https://goecosystem.github.io/go-cheatsheets/" class="btn btn-primary">Cheatsheets</a>
    </div>
  </div>

  <div class="repo-card">
    <div class="repo-header">
      <h3>
        <a href="https://github.com/GoEcosystem/GoEcosystem.github.io">GoEcosystem.github.io</a>
        <span class="repo-language">HTML/Jekyll</span>
      </h3>
    </div>
    <div class="repo-description">
      <p>Central documentation hub and website for the GoEcosystem organization.</p>
    </div>
    <div class="repo-links">
      <a href="https://github.com/GoEcosystem/GoEcosystem.github.io" class="btn btn-secondary">GitHub Repository</a>
      <a href="https://goecosystem.github.io/" class="btn btn-primary">Visit Website</a>
    </div>
  </div>
</div>

## Repository Structure Standards

All repositories in the GoEcosystem organization follow standardized structures and conventions:

- **Documentation**: Every repository has documentation in the `/docs` directory, built with Jekyll
- **API References**: API-providing repositories include standardized API documentation
- **Examples**: Code examples in the `/examples` directory
- **Testing**: Comprehensive test coverage with examples
- **CI/CD**: GitHub Actions workflows for testing, linting, and documentation

<style>
  .repo-featured {
    margin-bottom: 3rem;
  }
  
  .repo-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 1.5rem;
    margin-bottom: 3rem;
  }
  
  .repo-card {
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
    padding: 1.5rem;
    display: flex;
    flex-direction: column;
  }
  
  .repo-card.featured {
    grid-column: 1 / -1;
    display: flex;
    flex-direction: column;
  }
  
  .repo-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 1rem;
  }
  
  .repo-header h3 {
    margin: 0;
    font-size: 1.25rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  
  .repo-language {
    font-size: 0.75rem;
    background-color: var(--primary-light);
    color: white;
    padding: 0.25rem 0.5rem;
    border-radius: 12px;
    font-weight: normal;
  }
  
  .repo-description {
    margin-bottom: 1rem;
    flex-grow: 1;
  }
  
  .repo-description p {
    margin: 0;
    color: var(--gray-700);
  }
  
  .repo-features {
    margin-bottom: 1.5rem;
  }
  
  .repo-features h4 {
    font-size: 1rem;
    margin-bottom: 0.5rem;
    color: var(--gray-800);
  }
  
  .repo-features ul {
    list-style-type: none;
    padding-left: 0;
    margin-bottom: 0;
  }
  
  .repo-features li {
    padding-left: 1.5rem;
    position: relative;
    margin-bottom: 0.3rem;
  }
  
  .repo-features li::before {
    content: "✓";
    position: absolute;
    left: 0;
    color: var(--primary-color);
  }
  
  .repo-links {
    display: flex;
    gap: 0.5rem;
    flex-wrap: wrap;
  }
  
  .repo-links .btn {
    flex: 1;
    min-width: 120px;
    text-align: center;
  }
  
  .repo-stats {
    display: flex;
    gap: 1rem;
  }
  
  .repo-stat {
    font-size: 0.875rem;
    color: var(--gray-600);
  }
  
  @media (max-width: 768px) {
    .repo-header {
      flex-direction: column;
      align-items: flex-start;
    }
    
    .repo-stats {
      margin-top: 0.5rem;
    }
  }
</style>
