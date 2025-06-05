# Contributing to CDP Project

First off, thank you for your interest in contributing! We welcome contributions of all kinds—from bug reports and feature requests to documentation improvements and code fixes.

This document explains how to:

1. File issues and request features  
2. Set up your local environment  
3. Create branches, write commits, and submit pull requests  
4. Follow our coding style and testing guidelines  
5. Navigate the review process  

---

## 1. Filing Issues & Feature Requests

1. **Search existing issues**: Before opening a new issue, check [Issues](https://github.com/ASUCICREPO/CDP-Project/issues) to see if someone else has already reported the same bug or requested a similar feature.
2. **Open a new issue** if needed and use one of our issue templates:
   - **Bug report**: Choose “Bug report” template and include:
     - A clear title, e.g., `Bug: Unexpected crash when opening file`
     - Steps to reproduce
     - Expected behavior vs. actual behavior
     - Environment details (OS, version, dependencies)
   - **Feature request**: Choose “Feature request” template and include:
     - What problem you’re trying to solve
     - Any relevant examples or mockups
3. **Assign labels** (if you have permission) or let the maintainers triage your issue. We use labels like `bug`, `enhancement`, `help wanted`, and `good first issue`.

---

## 2. Setting Up Your Development Environment

1. **Fork the repository**: Click “Fork” in the upper-right corner of the repo page.  
2. **Clone your fork**:
   ```bash
   git clone https://github.com/ASUCICREPO/CDP-Project.git
   cd CDP-Project
   ```
3. **Install dependencies** (modify these commands to match your project’s stack):
   - If it’s a Node.js project:
     ```bash
     npm install
     ```
   - If it’s Python:
     ```bash
     python3 -m venv .venv
     source .venv/bin/activate
     pip install -r requirements.txt
     ```
   - If it’s something else, update this section accordingly.

4. **Create a “dev” branch** or ensure you’re on `main` before branching for new work:
   ```bash
   git checkout main
   git pull origin main
   ```
5. **Run tests & linters** to confirm everything is passing:
   ```bash
   # JavaScript example
   npm test
   npm run lint

   # Python example
   pytest
   flake8 .
   ```

---

## 3. Branching, Commits & Pull Requests

### 3.1 Branch Naming

- Create a new branch for each logical change or feature request. Prefix branches with one of:
  - `feature/` (for new features)  
  - `bugfix/` (for bug fixes)  
  - `docs/` (for documentation changes)  
  - `chore/` (for maintenance tasks)  
- Examples:
  ```text
  feature/add-user-authentication
  bugfix/fix-null-pointer-on-startup
  docs/update-api-reference
  ```

### 3.2 Writing Good Commit Messages

We follow [Conventional Commits](https://www.conventionalcommits.org/) style. Each commit message should include:
1. A **type** prefix (`feat:`, `fix:`, `docs:`, `refactor:`, `chore:`)
2. A short, imperative description (max ~72 characters)
3. (Optional) A blank line followed by a more detailed explanation

**Example:**
```text
feat: add OAuth2 login endpoint

- Introduced `POST /auth/login` using Passport.js
- Unit tests added in `tests/auth.test.js`
- Updated README with authentication instructions
```

### 3.3 Submitting a Pull Request

1. **Push your branch** to your fork:
   ```bash
   git push origin feature/your-branch-name
   ```
2. **Open a Pull Request**:
   - Go to `https://github.com/ASUCICREPO/CDP-Project/compare`
   - Select your branch on the right and `main` (or `develop`) on the left
   - Click “Create pull request”
3. **Fill in the PR template**:
   - Link to the issue (e.g., “Closes #123”)
   - Provide a brief description of your changes
   - Summarize how to test locally
   - Mention any dependencies or migrations required
4. **Wait for reviews**:
   - At least one maintainers must approve
   - Respond to reviewer feedback by pushing additional commits to the same branch
5. **Merge once approved**:
   - Maintainers will merge using the designated merge method (e.g., “Squash and merge” or “Merge commit”)
   - Once merged, your branch can be safely deleted

---

## 4. Coding Style & Testing Guidelines

### 4.1 General Coding Standards

- **Consistent Formatting**:  
  - For JavaScript/TypeScript, use ESLint + Prettier.  
  - For Python, use `flake8` / `black` / `isort`.  
  - For other languages, follow their widely adopted style guides.
- **Naming Conventions**:  
  - Variables and functions in `camelCase` (for JS/TS) or `snake_case` (for Python).  
  - Classes and types in `PascalCase`.
- **Complex Functions**: If a function grows beyond ~50 lines, consider refactoring into smaller, single-purpose helpers.

### 4.2 Testing

- **Unit tests**:  
  - Place tests in a `tests/` (or `__tests__/`) folder parallel to your `src/` directory.  
  - Aim for >80% test coverage on core logic.
- **Integration tests** (if applicable):  
  - Use a separate environment (e.g., a test database).  
  - Mock external dependencies whenever possible.
- **End-to-End tests**:  
  - If you have a web UI or CLI, write basic E2E tests to cover major workflows.
- **Running Tests Locally**:  
  ```bash
  # Example for Jest (JavaScript)
  npm test

  # Example for Pytest (Python)
  pytest
  ```

---

## 5. Code Review & Collaboration

1. **Be responsive**: Check the PR regularly for review comments or CI failures.  
2. **Be respectful**: Provide constructive feedback and explanations—remember every contributor is learning.  
3. **Small, atomic PRs**: Where possible, keep each pull request focused on a single issue or feature. Larger changes are harder to review.  

---

## 6. Maintenance & Roadmap

- **Dependabot / Automated Dependency Upgrades**: We use [Dependabot](https://docs.github.com/en/code-security/supply-chain-security/keeping-your-dependencies-updated-automatically) to open PRs for dependency updates. Please review them promptly.  
- **Labeling Strategy**:  
  - `good first issue` = suitable for new contributors  
  - `help wanted` = extra eyes would be appreciated  
  - `in progress` = active work under way  
  - `resolved` = closed/fixed issues  
- **Milestones & Versioning**: We follow [Semantic Versioning](https://semver.org/). Check the “Milestones” tab to see what’s scheduled for the next release.  

---

## 7. Getting Help

- For general questions or discussions, refer to our [Discussion Board](https://github.com/ASUCICREPO/CDP-Project/discussions) (if enabled). 

---

### Thank You for Contributing!

Every contribution—no matter how small—makes a difference. We appreciate your time and effort in helping improve CDP Project.
