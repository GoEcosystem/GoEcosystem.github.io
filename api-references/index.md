---
layout: default
title: API References
description: API documentation for GoEcosystem projects
---

# API References

This page serves as a central hub for all API documentation across GoEcosystem projects. Each project's API is documented using a consistent format that includes endpoints, parameters, and examples.

## Available API Documentation

<div class="card-grid">
  <div class="card">
    <h3>Go Web Scraper API</h3>
    <p>RESTful API for accessing and manipulating scraped data programmatically.</p>
    <ul class="api-feature-list">
      <li>Article and product endpoints</li>
      <li>Pagination and search capabilities</li>
      <li>Data export functionality</li>
    </ul>
    <a href="https://goecosystem.github.io/go-web-scraper/api/" class="btn btn-primary">View API Docs</a>
  </div>
  
  <div class="card">
    <h3>Go Utils HTTP API</h3>
    <p>API for the HTTP client utilities with advanced features.</p>
    <ul class="api-feature-list">
      <li>Request and response handling</li>
      <li>Middleware support</li>
      <li>Rate limiting and retry mechanics</li>
    </ul>
    <a href="https://goecosystem.github.io/go-utils/api/http/" class="btn btn-primary">View API Docs</a>
  </div>
  
  <div class="card">
    <h3>Go Utils Database API</h3>
    <p>API for database interaction utilities.</p>
    <ul class="api-feature-list">
      <li>Connection management</li>
      <li>Query building</li>
      <li>Migration utilities</li>
    </ul>
    <a href="https://goecosystem.github.io/go-utils/api/database/" class="btn btn-primary">View API Docs</a>
  </div>
</div>

## API Documentation Standards

All API documentation across GoEcosystem follows consistent standards:

<div class="standards-section">
  <h3>Endpoint Documentation</h3>
  <p>Each endpoint is documented with:</p>
  <ul>
    <li>HTTP method and URL</li>
    <li>Description of functionality</li>
    <li>Request parameters and body schema</li>
    <li>Response status codes and body schema</li>
    <li>Example requests and responses</li>
  </ul>
</div>

<div class="standards-section">
  <h3>Error Handling</h3>
  <p>All APIs use consistent error response formats:</p>
  
  ```json
  {
    "error": "Error code or type",
    "message": "Human-readable error message",
    "details": {}  // Optional additional details
  }
  ```
  
  <p>Standard HTTP status codes are used across all APIs.</p>
</div>

<div class="standards-section">
  <h3>Authentication</h3>
  <p>When required, APIs use:</p>
  <ul>
    <li>API key authentication via headers</li>
    <li>OAuth 2.0 for more complex scenarios</li>
    <li>Rate limiting for all authenticated endpoints</li>
  </ul>
</div>

## Implementing the API Documentation Template

If you're adding a new project to GoEcosystem, follow these steps to implement our standardized API documentation:

1. Use the Jekyll API layout (`layout: api` in front matter)
2. Create both a Markdown file (`/docs/api/index.md`) and an HTML fallback file (`/docs/api/index.html`)
3. Follow the endpoint documentation structure in our template
4. Include interactive examples where possible

<a href="/guides/api-documentation-template/" class="btn btn-primary">View API Documentation Template Guide</a>

<style>
  .api-feature-list {
    list-style-type: none;
    padding-left: 0;
    margin-bottom: 1.5rem;
  }
  
  .api-feature-list li {
    padding-left: 1.5rem;
    position: relative;
    margin-bottom: 0.5rem;
  }
  
  .api-feature-list li::before {
    content: "✓";
    position: absolute;
    left: 0;
    color: var(--primary-color);
    font-weight: bold;
  }
  
  .standards-section {
    margin-bottom: 2rem;
    padding: 1.5rem;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
  }
  
  .standards-section h3 {
    margin-top: 0;
    color: var(--primary-color);
  }
</style>
