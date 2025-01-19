# Commit Best Practices — A Guide for Software Engineers

This guide provides best practices for writing clean, meaningful, and efficient commit messages. It covers various scenarios, from ideal commits to common mistakes, helping you communicate effectively through your version control history. The guide also includes Git best practices and tips on using emojis to enhance readability and improve team communication.

---

## Table of Contents

1. [Why Write Good Commit Messages?](#why-write-good-commit-messages)  
2. [Anatomy of a Great Commit Message](#anatomy-of-a-great-commit-message)  
3. [Git Best Practices for Commit Messages](#git-best-practices-for-commit-messages)  
4. [Commit Message Templates](#commit-message-templates)  
5. [Using Emojis in Commit Messages](#using-emojis-in-commit-messages)  
6. [Examples for Various Scenarios](#examples-for-various-scenarios)  
   - [Adding Features](#adding-features)  
   - [Fixing Bugs](#fixing-bugs)  
   - [Improving Documentation](#improving-documentation)  
   - [Refactoring Code](#refactoring-code)  
   - [Handling Rollbacks](#handling-rollbacks)  
   - [Addressing Technical Debt](#addressing-technical-debt)  
   - [Performance Improvements](#performance-improvements)  
   - [Security Updates](#security-updates)  
   - [Dependency Management](#dependency-management)  
7. [Commit Message Conventions by Team Size](#commit-message-conventions-by-team-size)  
8. [Automated Commit Validation](#automated-commit-validation)  
9. [Branch Naming Conventions](#branch-naming-conventions)

---

## 1. Why Write Good Commit Messages?

- **Improves collaboration:** Helps team members understand the purpose and context of changes.  
- **Enhances code reviews:** Clear commit messages make it easier to review changes.  
- **Facilitates debugging:** Precise messages provide context for tracing issues.  
- **Supports project history:** Helps maintain a clear and meaningful Git log.

---

## 2. Anatomy of a Great Commit Message

### Structure:

1. **Subject line** (short, 50 characters or less):  
   - Summarize the change.  
   - Use the imperative mood (e.g., "Add," "Fix," "Refactor").  

2. **Body** (optional but recommended, 72 characters per line):  
   - Explain *why* the change was made.  
   - Highlight *what* changed.  
   - Discuss *how* the change was implemented.  

3. **Footer** (optional):  
   - Reference issues (e.g., "Closes #123").  
   - Mention breaking changes or other critical notes.  

---

## 3. Git Best Practices for Commit Messages

- Commit small, **atomic changes** for clarity.  
- Use **branch names** that reflect the purpose of the changes.  
- **Rebase** before merging to keep history clean.  
- Write commit messages that provide meaningful context, avoiding vague terms like "fix" or "update."  
- Avoid committing directly to the main branch.  

---

## 4. Commit Message Templates

### Standard Template:
```
<type>: <subject>

<body>

<footer>
```

### Example:
```
feat: Add user authentication module

Implement user login and registration functionality using OAuth.
Include unit tests for all authentication endpoints.

Closes #42
```

---

## 5. Using Emojis in Commit Messages

Emojis improve readability and convey intent quickly. Below is a suggested list:

- 💡 `:bulb:` – Idea or suggestion.  
- 🔧 `:wrench:` – Fix or maintenance.  
- ⚙️ `:gear:` – Configuration changes.  
- ✨ `:sparkles:` – New features.  
- 🛠️ `:hammer_and_wrench:` – Refactoring.  
- ⚠️ `:warning:` – Breaking changes.  
- 🔨 `:construction:` – Work in progress (WIP).  
- 📈 `:chart_with_upwards_trend:` – Performance improvements.  

### Usage Example:
```
✨ feat: Add dark mode toggle

Implement a dark mode toggle button with local storage support.
```

---

## 6. Examples for Various Scenarios

### Adding Features:
```
✨ feat: Add user profile page

Introduce a user profile page with editable fields.
Include validation for all inputs.
```

### Fixing Bugs:
```
🔧 fix: Resolve crash on startup

Fix an issue where the app crashes on startup due to null pointer dereference.
Add null checks to the initialization sequence.
```

### Improving Documentation:
```
📖 docs: Update README for installation instructions

Add a detailed guide for setting up the project locally.
Include common troubleshooting steps.
```

### Refactoring Code:
```
🛠️ refactor: Simplify database query logic

Refactor query builder for better readability and performance.
Replace raw SQL queries with ORM methods.
```

### Handling Rollbacks:
```
⚠️ revert: Revert "Add user analytics"

Rollback analytics module due to compliance concerns.
Original commit hash: abc123.
```

### Addressing Technical Debt:
```
🔧 chore: Remove unused dependencies

Clean up unused npm dependencies to reduce project size.
```

### Performance Improvements:
```
📈 perf: Optimize image loading algorithm

Implement lazy loading for images to improve initial page load.
Reduce memory usage by 40%.
Bundle size decreased by 250KB.
```

### Security Updates:
```
🔒 security: Update authentication tokens

Implement JWT token rotation.
Add rate limiting for login attempts.
Closes #234.
```

### Dependency Management:
```
📦 deps: Update core dependencies

Update React to v18.2.0.
Upgrade TypeScript to 4.9.5.
Fix security vulnerabilities in dev dependencies.
```

---

## 7. Commit Message Conventions by Team Size

- **Small teams:** Focus on detailed descriptions, as fewer people share the context.  
- **Large teams:** Adhere strictly to templates and conventions to ensure clarity across diverse contributors.  

---

## 8. Automated Commit Validation

- **Leverage hooks:** Use Git hooks to enforce message style (e.g., via `commitlint`).  
- **Automate checks:** Integrate tools like Husky or Prettier to streamline workflows.  

---

## 9. Branch Naming Conventions

### Pattern
```
<type>/<ticket-number>-<short-description>
```

### Examples
- `feature/PROJ-123-user-authentication`  
- `bugfix/PROJ-456-fix-memory-leak`  
- `hotfix/PROJ-789-critical-security-patch`  

---

By following these best practices, you’ll write commit messages that enhance team collaboration, improve project history, and maintain a clean Git workflow.
