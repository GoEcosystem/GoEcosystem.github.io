---
layout: default
title: GoEcosystem
description: A comprehensive ecosystem of Go applications, libraries, and tools
---

<div class="hero-section" style="background-color: #00ADD8; padding: 4rem 0; border-radius: 0; text-align: center; margin-bottom: 3rem; color: white;">
  <h1>GoEcosystem</h1>
  <p class="hero-tagline">A comprehensive ecosystem of Go applications, libraries, and tools</p>
  <div class="hero-buttons">
    <a href="https://github.com/GoEcosystem" class="btn btn-primary">View on GitHub</a>
    <a href="#documentation" class="btn btn-secondary">Explore Documentation</a>
  </div>
</div>

<div class="container">
  <section id="featured-project" class="featured-section">
    <h2>Featured Project</h2>
    <div class="feature-card featured">
      <h3>Go Web Scraper</h3>
      <p>Our flagship web scraper demonstrates Go's capabilities for concurrent programming, database integration, and web development.</p>
      <ul class="feature-list">
        <li>Concurrent data extraction from multiple sources</li>
        <li>SQLite database for persistent storage</li>
        <li>Web interface for browsing scraped data</li>
        <li>Export to JSON and CSV formats</li>
        <li>Ethical scraping with rate limiting</li>
      </ul>
      <div class="button-group">
        <a href="https://github.com/GoEcosystem/go-web-scraper" class="btn btn-primary">View on GitHub</a>
        <a href="https://goecosystem.github.io/go-web-scraper/" class="btn btn-secondary">View Documentation</a>
      </div>
    </div>
  </section>
  
  <section id="repositories" class="repositories-section">
    <h2>Our Repositories</h2>
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
        <a href="https://github.com/GoEcosystem/go-docs" class="btn btn-primary">View Documentation</a>
      </div>
      
      <div class="card">
        <h3>go-web-scraper</h3>
        <p>Comprehensive web scraper with database integration and web interface.</p>
        <div class="button-group">
          <a href="https://github.com/GoEcosystem/go-web-scraper" class="btn btn-primary">View Repository</a>
          <a href="https://goecosystem.github.io/go-web-scraper/" class="btn btn-secondary">View Documentation</a>
        </div>
      </div>
      
      <div class="card">
        <h3>go-cheatsheets</h3>
        <p>Quick reference guides for Go programming language syntax and patterns.</p>
        <a href="https://github.com/GoEcosystem/go-cheatsheets" class="btn btn-primary">View Cheatsheets</a>
      </div>
    </div>
  </section>
</div>

<section id="documentation" class="documentation-section">
  <div class="container">
    <h2>Documentation Hub</h2>
    <p class="documentation-intro">Access standardized documentation across all GoEcosystem repositories.</p>
    
    <div class="documentation-grid">
      <div class="doc-card">
        <h3>API References</h3>
        <div class="doc-card-content">
          <p>Comprehensive API documentation for all GoEcosystem projects.</p>
          <div class="doc-links">
            <a href="https://goecosystem.github.io/go-web-scraper/api/" class="doc-link">Go Web Scraper API</a>
            <a href="https://goecosystem.github.io/go-utils/api/" class="doc-link">Go Utils API</a>
          </div>
        </div>
      </div>
      
      <div class="doc-card">
        <h3>Guides & Tutorials</h3>
        <div class="doc-card-content">
          <p>Step-by-step guides for using GoEcosystem tools and libraries.</p>
          <div class="doc-links">
            <a href="https://goecosystem.github.io/go-web-scraper/guides/" class="doc-link">Web Scraper Guides</a>
            <a href="/guides/documentation-style-guide" class="doc-link">Documentation Style Guide</a>
          </div>
        </div>
      </div>
      
      <div class="doc-card">
        <h3>Templates</h3>
        <div class="doc-card-content">
          <p>Standardized templates for creating consistent documentation.</p>
          <div class="doc-links">
            <a href="/_templates/api-page-template" class="doc-link">API Documentation Template</a>
            <a href="/_templates/reference-page-template" class="doc-link">Reference Documentation Template</a>
            <a href="/_templates/guide-page-template" class="doc-link">Guide Documentation Template</a>
            <a href="/_templates/readme-template" class="doc-link">README Template</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  .hero-section {
    background-color: #00ADD8;
    padding: 4rem 0;
    border-radius: 0;
    text-align: center;
    margin-bottom: 3rem;
    color: white;
  }
  
  .hero-section h1 {
    font-size: 3.5rem;
    margin-bottom: 1rem;
    color: white;
  }
  
  .hero-tagline {
    font-size: 1.5rem;
    margin-bottom: 2rem;
    max-width: 800px;
    margin-left: auto;
    margin-right: auto;
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
  
  .feature-card.featured {
    background-color: #f8f9fa;
    border-left: 5px solid #00ADD8;
    padding: 2rem;
    border-radius: 8px;
  }
  
  .repositories-section, 
  .documentation-section {
    margin-bottom: 4rem;
  }
  
  .card-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 2rem;
  }
  
  .card {
    background-color: white;
    border: 1px solid #e9ecef;
    border-radius: 8px;
    padding: 1.5rem;
    transition: transform 0.2s, box-shadow 0.2s;
    display: flex;
    flex-direction: column;
  }
  
  .card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  }
  
  .card h3 {
    color: #00ADD8;
    margin-top: 0;
  }
  
  .card p {
    margin-bottom: 1.5rem;
    flex-grow: 1;
  }
  
  .documentation-intro {
    text-align: center;
    margin-bottom: 2rem;
  }
  
  .documentation-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 2rem;
  }
  
  .doc-card {
    border: 1px solid #e9ecef;
    border-radius: 8px;
    overflow: hidden;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  
  .doc-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  }
  
  .doc-card h3 {
    background-color: #00ADD8;
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
    color: #00ADD8;
    text-decoration: none;
    font-weight: 500;
  }
  
  .doc-link:hover {
    text-decoration: underline;
  }
  
  .btn {
    display: inline-block;
    padding: 0.5rem 1.5rem;
    font-weight: 500;
    text-align: center;
    border-radius: 4px;
    cursor: pointer;
    transition: all 0.2s;
    text-decoration: none;
  }
  
  .btn-primary {
    background-color: #00ADD8;
    color: white;
    border: 1px solid #00ADD8;
  }
  
  .btn-primary:hover {
    background-color: #0092B8;
    border-color: #0092B8;
    text-decoration: none;
    color: white;
  }
  
  .btn-secondary {
    background-color: white;
    color: #00ADD8;
    border: 1px solid #00ADD8;
  }
  
  .btn-secondary:hover {
    background-color: #f8f9fa;
    text-decoration: none;
    color: #00ADD8;
  }
  
  .btn-lg {
    padding: 0.75rem 2rem;
    font-size: 1.1rem;
  }
  
  .button-group {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
  }
  
  @media (max-width: 768px) {
    .hero-section h1 {
      font-size: 2.5rem;
    }
    
    .hero-tagline {
      font-size: 1.2rem;
    }
    
    .card-grid,
    .documentation-grid {
      grid-template-columns: 1fr;
    }
  }
</style>
