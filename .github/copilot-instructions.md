# Copilot Instructions for ghc-guide

This repository contains a comprehensive guide to GitHub Copilot, built as a Material for MkDocs documentation site. When contributing to this project, please follow these guidelines to maintain consistency and quality.

## Project Structure

The repository is organized as follows:

- **`docs/`** - Main documentation content in Markdown format
  - `index.md` - Homepage and welcome content
  - `getting-started/` - Beginner guides and setup instructions
  - `ghc-vscode/` - GitHub Copilot in Visual Studio Code features
  - `ghc-web/` - GitHub Copilot web interface features
  - `preview-advanced-topics/` - Advanced features and customization
  - `workshops/` - Hands-on tutorial content
  - `resources/` - External links and additional reading
  - `assets/` - Images, logos, and static assets

- **`.github/`** - GitHub-specific configuration files
  - `workflows/ci.yml` - Automated CI/CD pipeline for deployment

- **`mkdocs.yml`** - Main configuration file for Material MkDocs
- **`.devcontainer/`** - Development container configuration for consistent environments

## Libraries and Technologies Used

### Documentation Framework
- **Material for MkDocs** (`mkdocs-material`): Modern documentation theme with responsive design
- **MkDocs** (`mkdocs`): Static site generator for project documentation
- **Python Markdown** (`markdown`): Core markdown processing engine

### Markdown Extensions
- **PyMdown Extensions** (`pymdown-extensions`): Advanced markdown features including:
  - `pymdownx.superfences`: Enhanced code blocks with language-specific highlighting
  - `pymdownx.tabbed`: Tabbed content sections (alternate style enabled)
  - `pymdownx.details`: Collapsible content sections
- **Admonition**: Note, warning, and info callout boxes
- **Mermaid Diagrams**: Support for flowcharts, sequence diagrams, and other visualizations

### Build and Deployment
- **GitHub Actions**: Automated CI/CD pipeline
- **GitHub Pages**: Hosting platform for the generated site
- **Python 3.x**: Runtime environment for the build process

## Available Tools

### Development Tools
- **mkdocs serve**: Local development server with hot-reload (`mkdocs serve`)
- **mkdocs build**: Static site generation (`mkdocs build`)
- **mkdocs gh-deploy**: Automated deployment to GitHub Pages

### CI/CD Pipeline
- Automatic builds on push to `main` or `master` branches
- Deployment to GitHub Pages using `mkdocs gh-deploy --force`
- Caching of dependencies for faster builds
- Python environment setup with `mkdocs-material` installation

### Content Validation
The build process includes validation for:
- Broken internal links
- Missing anchor references
- Absolute vs. relative link consistency

## Documentation Guidance

### Content Style and Structure
When generating documentation for this project, always:

1. **Write for Beginners**: Assume readers are new to GitHub Copilot and need clear, step-by-step explanations
2. **Use Tutorial Format**: Structure content as hands-on tutorials with practical examples
3. **Break Content into Digestible Sections**: Use short paragraphs, bullet points, and clear headings
4. **Include Visual Elements**: Reference images, diagrams, and code examples where helpful

### Markdown Requirements
**CRITICAL**: Only generate documentation in Markdown (`.md`) files. The Material MkDocs framework automatically converts these into beautiful, responsive web pages.

#### Supported Markdown Features
Use these Material MkDocs features for enhanced documentation:

```markdown
# Admonitions for important information
!!! note "Important Note"
    This is a note callout

!!! warning "Be Careful"
    This is a warning callout

!!! tip "Pro Tip"
    This is a helpful tip

# Tabbed content for multiple options
=== "VS Code"
    Instructions for VS Code users

=== "Web Interface"
    Instructions for web users

# Code blocks with syntax highlighting
```python
def example_function():
    return "Hello, Copilot!"
```

# Mermaid diagrams for visual explanations
```mermaid
graph LR
    A[Start] --> B[Configure Copilot]
    B --> C[Write Code]
    C --> D[Get Suggestions]
```
```

### Content Organization
Follow the existing navigation structure in `mkdocs.yml`:

- **Getting Started**: Basic setup and configuration
- **Copilot in VSCode**: IDE-specific features and workflows
- **GitHub Copilot Web**: Browser-based functionality
- **Preview and Advanced Features**: Cutting-edge capabilities
- **Workshops**: Hands-on tutorials and exercises
- **Resources**: External references and further reading

### Writing Best Practices
1. **Clear Headings**: Use descriptive section headings that explain what users will learn
2. **Step-by-Step Instructions**: Number steps when describing procedures
3. **Code Examples**: Include working code snippets that users can copy and test
4. **Screenshots and Diagrams**: Reference visual aids to clarify complex concepts
5. **Cross-References**: Link between related sections using relative paths
6. **Accessibility**: Write alt text for images and use semantic HTML structures

### File Naming and Organization
- Use lowercase filenames with hyphens (e.g., `getting-started.md`)
- Place files in appropriate subdirectories matching the navigation structure
- Include an `index.md` file in each directory for overview content
- Store images in `docs/assets/` or relevant subdirectories

## Quality Standards

### Content Quality
- **Accuracy**: Verify all technical information against official GitHub Copilot documentation
- **Completeness**: Ensure tutorials include all necessary steps and dependencies
- **Clarity**: Use simple language and explain technical terms
- **Examples**: Provide real-world, practical examples that users can follow

### Technical Standards
- **Validation**: Test all code examples and procedures before publication
- **Links**: Use relative links for internal navigation, absolute links for external resources
- **Formatting**: Follow consistent markdown formatting throughout
- **Navigation**: Ensure all new pages are properly referenced in `mkdocs.yml`

Remember: This documentation is automatically transformed into a professional website using Material MkDocs. Focus on creating excellent markdown content, and the framework will handle the presentation layer.