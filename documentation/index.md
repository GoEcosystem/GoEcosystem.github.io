---
layout: default
title: Documentation
description: Central documentation hub for GoEcosystem projects
---

# Documentation Hub

Welcome to the central documentation hub for GoEcosystem projects. Here you'll find comprehensive guides, API references, and tutorials for all our repositories.

## Project Documentation

<div class="card-grid">
  <div class="card">
    <h3>Go Web Scraper</h3>
    <p>Documentation for our flagship web scraper application with database integration and web interface.</p>
    <ul>
      <li><a href="https://goecosystem.github.io/go-web-scraper/">Overview</a></li>
      <li><a href="https://goecosystem.github.io/go-web-scraper/api/">API Reference</a></li>
      <li><a href="https://goecosystem.github.io/go-web-scraper/architecture/">Architecture</a></li>
    </ul>
    <a href="https://goecosystem.github.io/go-web-scraper/" class="btn btn-primary">View Documentation</a>
  </div>

  <div class="card">
    <h3>Go Utils</h3>
    <p>Documentation for shared utilities including HTTP clients, database helpers, and more.</p>
    <ul>
      <li><a href="https://goecosystem.github.io/go-utils/">Overview</a></li>
      <li><a href="https://goecosystem.github.io/go-utils/api/">API Reference</a></li>
      <li><a href="https://goecosystem.github.io/go-utils/examples/">Examples</a></li>
    </ul>
    <a href="https://goecosystem.github.io/go-utils/" class="btn btn-primary">View Documentation</a>
  </div>

  <div class="card">
    <h3>Go Cheatsheets</h3>
    <p>Quick reference guides and cheatsheets for Go programming and GoEcosystem libraries.</p>
    <ul>
      <li><a href="https://goecosystem.github.io/go-cheatsheets/">Overview</a></li>
      <li><a href="https://goecosystem.github.io/go-cheatsheets/syntax/">Go Syntax</a></li>
      <li><a href="https://goecosystem.github.io/go-cheatsheets/ecosystem/">Ecosystem Usage</a></li>
    </ul>
    <a href="https://goecosystem.github.io/go-cheatsheets/" class="btn btn-primary">View Cheatsheets</a>
  </div>
</div>

## Guides & Tutorials

<div class="doc-section">
  <h3>Getting Started</h3>
  <ul class="doc-list">
    <li><a href="/guides/installation/">Installation Guide</a></li>
    <li><a href="/guides/first-steps/">First Steps with GoEcosystem</a></li>
    <li><a href="/guides/contributing/">How to Contribute</a></li>
  </ul>
</div>

<div class="doc-section">
  <h3>Best Practices</h3>
  <ul class="doc-list">
    <li><a href="/guides/project-structure/">Project Structure</a></li>
    <li><a href="/guides/testing/">Testing Guidelines</a></li>
    <li><a href="/guides/error-handling/">Error Handling Patterns</a></li>
  </ul>
</div>

<div class="doc-section">
  <h3>Advanced Topics</h3>
  <ul class="doc-list">
    <li><a href="/guides/concurrency/">Concurrency Patterns</a></li>
    <li><a href="/guides/performance/">Performance Optimization</a></li>
    <li><a href="/guides/deployment/">Deployment Strategies</a></li>
  </ul>
</div>

## API References

<div class="doc-section">
  <h3>Core APIs</h3>
  <ul class="doc-list">
    <li><a href="/api-references/web-scraper/">Web Scraper API</a></li>
    <li><a href="/api-references/utils/">Utils API</a></li>
    <li><a href="/api-references/http-client/">HTTP Client API</a></li>
  </ul>
</div>

<style>
  .card-grid {
    margin-bottom: 3rem;
  }
  
  .doc-section {
    margin-bottom: 2rem;
  }
  
  .doc-list {
    list-style-type: none;
    margin-left: 0;
    padding-left: 0;
  }
  
  .doc-list li {
    position: relative;
    padding-left: 1.5rem;
    margin-bottom: 0.75rem;
  }
  
  .doc-list li::before {
    content: "→";
    position: absolute;
    left: 0;
    color: var(--primary-color);
  }
</style>
