---
layout: guide
title: Documentation Style Guide
description: Standards and best practices for writing documentation in GoEcosystem projects
repo_name: GoEcosystem.github.io
order: 10
related_guides:
  - title: API Documentation Template
    url: /guides/api-documentation-template/
  - title: GitHub Pages Best Practices
    url: /guides/github-pages-best-practices/
---

# Documentation Style Guide

This style guide establishes consistent standards for all documentation across GoEcosystem projects. Following these guidelines helps ensure a unified, professional, and user-friendly documentation experience.

## Writing Style and Tone

### Voice and Tone

- **Be clear and concise:** Use simple, direct language. Avoid jargon, idioms, and colloquialisms.
- **Be conversational but professional:** Write in a friendly, approachable tone while maintaining technical accuracy.
- **Use active voice:** "The function returns a value" instead of "A value is returned by the function."
- **Address the reader directly:** Use "you" when giving instructions. "You can configure the settings by..."

### Grammar and Mechanics

- **Use present tense:** "The method returns..." rather than "The method will return..."
- **Consistent punctuation:** End all list items and bullet points with periods if they are complete sentences.
- **Oxford comma:** Use commas before the final "and" in a series (e.g., "x, y, and z").
- **Acronyms:** Define acronyms on first use, e.g., "Hypertext Markup Language (HTML)."

## Formatting Conventions

### Headers and Structure

- **Use title case for page titles and section headers:** "Getting Started with Go" (not "Getting started with Go").
- **Limit header depth:** Try not to exceed 3 levels of headers (###) for most content.
- **Follow header hierarchy:** Don't skip levels (e.g., don't follow an H2 with an H4).
- **Keep headers short:** Aim for 3-5 words maximum.

### Lists and Tables

- **Use bulleted lists** for unordered items.
- **Use numbered lists** for sequential steps or prioritized items.
- **Keep list items parallel:** All items should use the same grammatical structure.
- **Use tables** for structured data and comparisons.
- **Add headers to all table columns.**

### Text Formatting

- **Bold** for emphasis and UI elements: "Click the **Save** button."
- *Italic* for introducing new terms: "This is known as *dependency injection*."
- `Code font` for code references, file names, and paths.
- Use block quotes for quotations or important notes.

## Code Snippet Standards

### Inline Code

- Use backticks (`) for inline code references, variable names, function names, and short commands.
- Example: Use `fmt.Println()` to output text to the console.

### Code Blocks

- Use triple backticks (```) with language specifier for multiline code examples.
- Always specify the language for syntax highlighting.
- Keep examples concise but complete.
- Include comments to explain complex or non-obvious code.

```go
// Initialize a new HTTP server
func startServer(port string) error {
    server := &http.Server{
        Addr: ":" + port,
        Handler: router,
    }
    
    return server.ListenAndServe()
}
```

### Code Sample Best Practices

- **Keep it simple:** Eliminate unnecessary complexity.
- **Make it copy-paste ready:** Code should work when copied without modification.
- **Use realistic examples:** Show real-world usage, not contrived examples.
- **Be consistent with style:** Follow Go's official style guide (gofmt).
- **Handle errors:** Show proper error handling in examples.
- **Add context:** Explain what the code does before/after the sample.

## Documentation Organization

### File Structure

- Place documentation in a `/docs` directory at the repository root.
- Use lowercase file names with hyphens for spaces.
- Group related files in appropriate subdirectories.
- Include a README.md at each directory level.

### File Naming

- Use descriptive, concise names.
- Follow kebab-case: lowercase with hyphens (e.g., `api-reference.md`).
- Include the content type in the filename (e.g., `installation-guide.md`).

### Front Matter

All documentation files should include Jekyll front matter:

```yaml
---
layout: guide  # or api, reference, default
title: Descriptive Title
description: A brief description of the content
repo_name: repository-name
order: 10  # for controlling the display order
related_guides:
  - title: Related Guide Title
    url: /path/to/guide/
---
```

## Links and References

- **Use relative links** for internal documentation.
- **Use descriptive link text:** "See the [installation guide](/guides/installation/)" rather than "Click [here](/guides/installation/)".
- **Check link validity** before committing documentation.
- **Include version information** when linking to external resources.

## Go-Specific Documentation Standards

### Package Documentation

- Begin with a single-sentence summary of the package's purpose.
- Provide an overview of the package's functionality.
- List the primary types and functions.
- Include usage examples.

### Function and Method Documentation

- Describe what the function does, not how it does it.
- Document parameters and return values.
- Note any side effects or state changes.
- Document any errors that can be returned.
- Provide usage examples for complex functions.

### Example:

```go
// SumIntegers calculates the sum of all integers in the provided slice.
// It returns the sum and an error if the slice is empty.
//
// Example:
//
//     sum, err := SumIntegers([]int{1, 2, 3})
//     if err != nil {
//         log.Fatal(err)
//     }
//     fmt.Println(sum) // Output: 6
//
func SumIntegers(numbers []int) (int, error) {
    // Implementation
}
```

## Final Checklist

Before publishing documentation, ensure it:

- Follows all the guidelines in this style guide
- Has been spell-checked and proofread
- Contains accurate and up-to-date information
- Works with both Jekyll processing and as direct HTML (hybrid approach)
- Includes appropriate front matter
- Links correctly to related resources
- Has been tested in both desktop and mobile views
