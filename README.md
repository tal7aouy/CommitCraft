# Commit Best Practices — A Guide for Software Engineers

This guide provides best practices for writing clean, meaningful, and efficient commit messages. It covers various scenarios, from ideal commits to common mistakes, helping you communicate effectively through your version control history. The guide also includes Git best practices and how to use emojis to enhance readability and improve team communication.

![Commit Best Practices](https://media2.dev.to/dynamic/image/width=1000,height=420,fit=cover,gravity=auto,format=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fsmvlw63q0m91pn1pf1cq.jpg)
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
7. [Additional Tips and Tricks](#additional-tips-and-tricks)
8. [Resources](#resources)

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

---

## 7. Additional Tips and Tricks

- **Review before committing:** Double-check your messages for clarity and grammar.
- **Use `git commit --amend`:** Fix mistakes in your last commit message.
- **Leverage hooks:** Use Git hooks to enforce message style (e.g., via `commitlint`).
- **Automate checks:** Integrate tools like Husky or Prettier to streamline workflows.

---

## 8. Resources

- [Conventional Commits](https://www.conventionalcommits.org/)
- [Git Emoji Guide](https://gitmoji.dev/)
- [Pro Git Book](https://git-scm.com/book/en/v2)

---

By following these best practices, you’ll write commit messages that enhance team collaboration, improve project history, and maintain a clean Git workflow.
