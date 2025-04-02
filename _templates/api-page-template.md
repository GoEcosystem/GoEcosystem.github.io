---
layout: api
title: API Documentation Title
description: Description of this API documentation page
repo_name: repository-name
breadcrumb_name: API Reference
order: 10
---

{% include breadcrumbs.html %}

<div class="api-documentation">
  <div class="api-sidebar">
    {% include sidebar.html title="API Sections" items=site.data.api_navigation %}
  </div>
  
  <div class="api-content">
    <h1>API Documentation Title</h1>
    
    <p>Brief overview of this API and its functionality.</p>
    
    <h2 id="base-url">Base URL</h2>
    
    <p>When running locally:</p>
    <pre><code>http://localhost:8080/api</code></pre>
    
    <h2 id="authentication">Authentication</h2>
    
    <p>Authentication information goes here.</p>
    
    <h2 id="endpoints">Endpoints</h2>
    
    <h3 id="resource-name">Resource Name</h3>
    
    <table>
      <thead>
        <tr>
          <th>Method</th>
          <th>Endpoint</th>
          <th>Description</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><span class="endpoint-method get">GET</span></td>
          <td><code>/api/resource</code></td>
          <td>List all resources</td>
        </tr>
        <tr>
          <td><span class="endpoint-method post">POST</span></td>
          <td><code>/api/resource</code></td>
          <td>Create a new resource</td>
        </tr>
        <tr>
          <td><span class="endpoint-method get">GET</span></td>
          <td><code>/api/resource/:id</code></td>
          <td>Get a specific resource by ID</td>
        </tr>
      </tbody>
    </table>
    
    <h4 id="list-resources">List Resources</h4>
    
    <pre><code>GET /api/resource?page=1&limit=20</code></pre>
    
    <p><strong>Query Parameters:</strong></p>
    <ul>
      <li><code>page</code>: Page number (default: 1)</li>
      <li><code>limit</code>: Number of items per page (default: 20)</li>
    </ul>
    
    <p><strong>Response:</strong></p>
    <pre><code class="language-json">{
  "data": [
    {
      "id": 1,
      "name": "Resource name",
      "created_at": "2025-01-01T00:00:00Z"
    },
    {
      "id": 2,
      "name": "Another resource",
      "created_at": "2025-01-02T00:00:00Z"
    }
  ],
  "meta": {
    "current_page": 1,
    "per_page": 20,
    "total_items": 50,
    "total_pages": 3
  }
}</code></pre>
    
    <h2 id="error-handling">Error Handling</h2>
    
    <p>All API errors return an appropriate HTTP status code and a JSON error response:</p>
    
    <pre><code class="language-json">{
  "error": {
    "code": "error_code",
    "message": "Human readable error message"
  }
}</code></pre>
    
    <h3 id="common-error-codes">Common Error Codes</h3>
    
    <table>
      <thead>
        <tr>
          <th>HTTP Status</th>
          <th>Error Code</th>
          <th>Description</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>400</td>
          <td>invalid_request</td>
          <td>The request is malformed or missing required parameters</td>
        </tr>
        <tr>
          <td>404</td>
          <td>not_found</td>
          <td>The requested resource was not found</td>
        </tr>
        <tr>
          <td>500</td>
          <td>internal_error</td>
          <td>An unexpected error occurred on the server</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>
