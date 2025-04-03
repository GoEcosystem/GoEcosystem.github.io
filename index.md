---
layout: default
title: GoEcosystem
description: A comprehensive ecosystem of Go applications, libraries, and tools with standardized documentation
---

<div class="hero-section">
  <h1>Welcome to GoEcosystem</h1>
  <p class="hero-subtitle">A comprehensive ecosystem of Go applications, libraries, and tools with standardized documentation across all repositories.</p>
  <div class="hero-buttons">
    <a href="#documentation" class="btn btn-primary btn-lg">Explore Documentation</a>
    <a href="https://github.com/GoEcosystem" class="btn btn-secondary btn-lg">View on GitHub</a>
  </div>
</div>

<div class="featured-section">
  <h2>Featured Project</h2>
  <div class="featured-project">
    <div class="featured-content">
      <h3>Go Web Scraper</h3>
      <p>Our flagship web scraper demonstrates Go's capabilities for concurrent programming, database integration, and web development.</p>
      <ul class="feature-list">
        <li>Concurrent web scraping from multiple sources</li>
        <li>SQLite database integration</li>
        <li>Web interface with Bootstrap styling</li>
        <li>Data export to JSON and CSV formats</li>
        <li>Ethical scraping practices</li>
      </ul>
      <div class="featured-links">
        <a href="https://goecosystem.github.io/go-web-scraper/" class="btn btn-primary">View Documentation</a>
        <a href="https://github.com/GoEcosystem/go-web-scraper" class="btn btn-secondary">GitHub Repository</a>
      </div>
    </div>
    <div class="featured-image">
      <img src="/assets/images/web-scraper-preview.png" alt="Go Web Scraper Interface" onerror="this.src='/assets/images/placeholder.png'; this.onerror=null;">
    </div>
  </div>
</div>

<h2 id="documentation">Documentation Hub</h2>

<div class="documentation-section">
  <p class="documentation-intro">
    All GoEcosystem repositories follow a standardized documentation approach using Jekyll with consistent layouts, navigation, and styling.
    Each repository includes comprehensive API references, architecture documentation, and user guides.
  </p>
  
  <div class="documentation-grid">
    <div class="doc-card">
      <h3>Go Web Scraper</h3>
      <div class="doc-card-content">
        <p>Complete documentation for our web scraping solution with API references and architectural guides.</p>
        <div class="doc-links">
          <a href="https://goecosystem.github.io/go-web-scraper/" class="doc-link">Documentation Home</a>
          <a href="https://goecosystem.github.io/go-web-scraper/api/" class="doc-link">API Reference</a>
          <a href="https://goecosystem.github.io/go-web-scraper/architecture/" class="doc-link">Architecture</a>
        </div>
      </div>
    </div>

    <div class="doc-card">
      <h3>Go Docs</h3>
      <div class="doc-card-content">
        <p>Organization-wide documentation, standards, and guidelines for GoEcosystem projects.</p>
        <div class="doc-links">
          <a href="https://goecosystem.github.io/go-docs/" class="doc-link">Documentation Home</a>
          <a href="https://goecosystem.github.io/go-docs/standards/" class="doc-link">Code Standards</a>
          <a href="https://goecosystem.github.io/go-docs/guidelines/" class="doc-link">Development Guidelines</a>
        </div>
      </div>
    </div>

    <div class="doc-card">
      <h3>Go Cheatsheets</h3>
      <div class="doc-card-content">
        <p>Quick reference guides for Go programming language syntax and common patterns.</p>
        <div class="doc-links">
          <a href="https://goecosystem.github.io/go-cheatsheets/" class="doc-link">Cheatsheets Home</a>
          <a href="https://goecosystem.github.io/go-cheatsheets/syntax/" class="doc-link">Syntax Reference</a>
          <a href="https://goecosystem.github.io/go-cheatsheets/patterns/" class="doc-link">Design Patterns</a>
        </div>
      </div>
    </div>
  </div>
</div>

<h2>Our Projects</h2>

<div class="card-grid">
  <div class="card">
    <h3>go-template</h3>
    <p>Standard template for Go projects with proper directory structure and GitHub workflows.</p>
    <a href="https://github.com/GoEcosystem/go-template" class="btn btn-primary">View Repository</a>
  </div>

  <div class="card">
    <h3>go-library-template</h3>
    <p>Template for creating reusable Go libraries with examples and best practices.</p>
    <a href="https://github.com/GoEcosystem/go-library-template" class="btn btn-primary">View Repository</a>
  </div>

  <div class="card">
    <h3>go-utils</h3>
    <p>Collection of shared utilities for HTTP, database, logging, and configuration.</p>
    <a href="https://github.com/GoEcosystem/go-utils" class="btn btn-primary">View Repository</a>
  </div>

  <div class="card">
    <h3>go-docs</h3>
    <p>Organization-wide documentation and guidelines for GoEcosystem projects.</p>
    <a href="https://goecosystem.github.io/go-docs/" class="btn btn-primary">View Documentation</a>
  </div>

  <div class="card">
    <h3>go-cheatsheets</h3>
    <p>Quick reference guides for Go programming language syntax and patterns.</p>
    <a href="https://github.com/GoEcosystem/go-cheatsheets" class="btn btn-primary">View Cheatsheets</a>
  </div>
</div>

<style>
  .hero-section {
    text-align: center;
    padding: 3rem 1rem;
    margin-bottom: 3rem;
    background-color: #f0f9ff;
    border-radius: 8px;
  }

  .hero-subtitle {
    font-size: 1.25rem;
    color: #495057;
    max-width: 800px;
    margin: 1rem auto 2rem;
  }

  .hero-buttons {
    display: flex;
    gap: 1rem;
    justify-content: center;
    flex-wrap: wrap;
  }

  .featured-section {
    margin-bottom: 3rem;
  }

  .featured-project {
    display: flex;
    gap: 2rem;
    background-color: white;
    border-radius: 8px;
    padding: 2rem;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
  }

  .featured-content {
    flex: 3;
  }

  .featured-image {
    flex: 2;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .featured-image img {
    max-width: 100%;
    border-radius: 4px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }

  .feature-list {
    margin-bottom: 1.5rem;
  }

  .featured-links {
    display: flex;
    gap: 1rem;
  }

  .documentation-section {
    margin-bottom: 3rem;
    background-color: #f8f9fa;
    padding: 2rem;
    border-radius: 8px;
  }
  
  .documentation-intro {
    text-align: center;
    margin-bottom: 2rem;
    max-width: 800px;
    margin-left: auto;
    margin-right: auto;
  }
  
  .documentation-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 2rem;
  }
  
  .doc-card {
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
    overflow: hidden;
  }
  
  .doc-card h3 {
    background-color: #007bff;
    color: white;
    padding: 1rem;
    margin: 0;
  }
  
  .doc-card-content {
    padding: 1.5rem;
  }
  
  .doc-links {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }
  
  .doc-link {
    display: inline-block;
    font-weight: 500;
    text-decoration: none;
    color: #007bff;
  }
  
  .doc-link:hover {
    text-decoration: underline;
  }

  @media (max-width: 768px) {
    .featured-project {
      flex-direction: column;
    }

    .featured-image {
      order: -1;
    }
    
    .documentation-grid {
      grid-template-columns: 1fr;
    }
  }
</style>
