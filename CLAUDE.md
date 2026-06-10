# Navruz - Project Documentation

This document provides comprehensive guidance for AI assistants working with this codebase.

## Project Overview

**Repository**: navruzboboqulov3-stack/Navruz  
**Status**: New repository - awaiting initial code  
**Primary Contact**: navruzboboqulov6@gmail.com

### Purpose
[To be filled: Describe the project's purpose, goals, and target users]

### Technology Stack
[To be filled: List programming languages, frameworks, databases, and key dependencies]

## Repository Structure

```
/
├── .git/                 # Git version control
├── CLAUDE.md            # This file - AI assistant documentation
└── [To be added]        # Project files and directories
```

### Expected Directory Layout
Once the project is initialized, document the directory structure here:
- `/src/` or `/app/` - Source code
- `/tests/` or `/spec/` - Test files
- `/docs/` - Documentation
- `/config/` - Configuration files
- `/scripts/` - Build and utility scripts

## Development Workflow

### Getting Started

1. **Initial Setup**
   ```bash
   # Clone the repository (if not already cloned)
   git clone [repository-url]
   cd Navruz
   
   # Install dependencies (update based on technology stack)
   # npm install          # for Node.js
   # pip install -r requirements.txt  # for Python
   # bundle install       # for Ruby
   ```

2. **Branch Strategy**
   - Main branch: `main` or `master`
   - Feature branches: `feature/feature-name`
   - Bug fix branches: `fix/bug-description`
   - AI assistant branches: `claude/[description]-[session-id]`

3. **Development Cycle**
   ```bash
   # Create/switch to feature branch
   git checkout -b feature/new-feature
   
   # Make changes and commit
   git add .
   git commit -m "Descriptive commit message"
   
   # Push changes
   git push -u origin feature/new-feature
   ```

### Git Conventions

#### Commit Messages
Follow conventional commit format:
- `feat:` - New feature
- `fix:` - Bug fix
- `docs:` - Documentation changes
- `style:` - Code style changes (formatting, no logic change)
- `refactor:` - Code refactoring
- `test:` - Adding or updating tests
- `chore:` - Maintenance tasks

Example: `feat: add user authentication module`

#### Branch Protection Rules
[To be filled: Document any branch protection rules, required reviews, CI checks]

## Code Conventions

### General Principles
1. **Code Quality**
   - Write clean, readable, and maintainable code
   - Follow the DRY (Don't Repeat Yourself) principle
   - Keep functions small and focused on a single responsibility
   - Use meaningful variable and function names

2. **Documentation**
   - Document complex logic and non-obvious decisions
   - Explain WHY, not WHAT (code should be self-documenting for WHAT)
   - Keep comments up-to-date with code changes

3. **Error Handling**
   - Handle errors gracefully
   - Provide meaningful error messages
   - Log errors appropriately for debugging

### Language-Specific Conventions
[To be filled: Add conventions for the specific languages used]

#### Example for JavaScript/TypeScript:
- Use ESLint for linting
- Follow Airbnb style guide
- Use TypeScript for type safety
- Prefer async/await over callbacks

#### Example for Python:
- Follow PEP 8 style guide
- Use type hints
- Document with docstrings
- Use pylint/flake8 for linting

## Testing Guidelines

### Test Structure
[To be filled: Document test organization and structure]

### Running Tests
```bash
# Run all tests
[command to run tests]

# Run specific test file
[command]

# Run tests with coverage
[command]
```

### Testing Principles
- Write tests for all new features
- Maintain test coverage above [X]%
- Follow AAA pattern: Arrange, Act, Assert
- Use descriptive test names that explain the scenario

## Build and Deployment

### Local Development
```bash
# Start development server
[command]

# Build for production
[command]

# Run linter
[command]

# Format code
[command]
```

### Environment Variables
[To be filled: Document required environment variables]

### Deployment Process
[To be filled: Document deployment steps and CI/CD pipeline]

## Dependencies Management

### Adding Dependencies
```bash
# Add production dependency
[command]

# Add development dependency
[command]
```

### Updating Dependencies
```bash
# Update all dependencies
[command]

# Update specific dependency
[command]
```

## Common Tasks for AI Assistants

### Code Analysis
When analyzing code:
1. Read relevant files first using the Read tool
2. Understand the context and existing patterns
3. Look for related code in other files
4. Check tests to understand expected behavior

### Making Changes
When modifying code:
1. Read the file before editing to understand context
2. Follow existing code style and patterns
3. Update related tests
4. Update documentation if needed
5. Run tests to verify changes
6. Commit with clear, descriptive messages

### Adding Features
When adding new features:
1. Understand the existing architecture
2. Follow established patterns and conventions
3. Write tests for new functionality
4. Document public APIs and complex logic
5. Consider edge cases and error handling
6. Update relevant documentation

### Bug Fixes
When fixing bugs:
1. Reproduce the bug if possible
2. Add a test that fails with the bug
3. Fix the bug
4. Verify the test now passes
5. Check for similar issues elsewhere
6. Document the fix in commit message

### Refactoring
When refactoring:
1. Ensure tests exist and pass before refactoring
2. Make incremental changes
3. Run tests after each significant change
4. Keep commits small and focused
5. Don't change behavior, only structure

## Security Considerations

### Best Practices
- Never commit sensitive information (API keys, passwords, tokens)
- Use environment variables for configuration
- Validate and sanitize all user input
- Follow OWASP top 10 guidelines
- Keep dependencies up-to-date for security patches

### Common Vulnerabilities to Avoid
- SQL injection
- Cross-Site Scripting (XSS)
- Cross-Site Request Forgery (CSRF)
- Command injection
- Path traversal
- Insecure deserialization

## Performance Considerations

[To be filled: Document performance requirements and optimization strategies]

## Troubleshooting

### Common Issues
[To be filled: Document common issues and solutions]

### Debug Commands
```bash
# Check application logs
[command]

# Run in debug mode
[command]

# Check system status
[command]
```

## Resources

### Documentation Links
[To be filled: Add links to relevant documentation]

### Team Communication
[To be filled: Add information about team communication channels]

### External Resources
[To be filled: Add links to external resources, tutorials, related projects]

## AI Assistant Specific Guidelines

### Tool Usage
1. **Prefer dedicated tools over Bash**
   - Use `Read` for reading files
   - Use `Edit` for modifying files
   - Use `Write` for creating new files
   - Use `Glob` for finding files by pattern
   - Use `Grep` for searching file contents

2. **Parallel Operations**
   - Make independent tool calls in parallel when possible
   - Use sequential calls only when operations depend on each other

3. **Git Operations**
   - Always push to branches starting with `claude/` and ending with session ID
   - Use `git push -u origin <branch-name>`
   - Retry up to 4 times with exponential backoff on network errors
   - Never use destructive operations without confirmation
   - Create new commits rather than amending unless explicitly requested

### Response Guidelines
1. **Communication**
   - Be concise and direct
   - State what you're about to do before tool calls
   - Provide brief updates at key moments
   - End with a 1-2 sentence summary

2. **Code Changes**
   - Only implement what's requested - no extra features
   - Follow existing patterns and conventions
   - Don't add unnecessary error handling or abstractions
   - Write minimal comments - only for non-obvious WHY
   - Test changes in the browser/app before reporting completion (for UI work)

3. **Risk Management**
   - Confirm before destructive operations
   - Ask before pushing code or creating PRs
   - Investigate unexpected state before modifying
   - Consider reversibility and blast radius of actions

### Session Management
- This repository uses the branch: `claude/claude-md-mk74cae4i5nwtmti-6ez4Q`
- Always develop on this branch
- Commit work with clear messages
- Push to the specified branch when complete

## Maintenance

### Keeping This Document Updated
This CLAUDE.md file should be updated when:
- Project structure changes significantly
- New development patterns are established
- Important conventions are adopted
- Common issues and solutions are identified
- New team members join who need context

Last updated: 2026-06-10

---

## Quick Reference

### Essential Commands
```bash
# [To be filled with project-specific commands]
```

### Key Files
- `CLAUDE.md` - This documentation file
- [To be filled: List other important files]

### Important Notes
- This is a new repository - structure and conventions will evolve
- Keep this documentation up-to-date as the project grows
- Follow security best practices from the start
- Write tests alongside new code
