# CLAUDE.md - AI Assistant Guide for AutoMexec Labs

> Comprehensive guide for AI assistants working on the AutoMexec Labs repository

---

## Table of Contents

1. [Repository Overview](#repository-overview)
2. [Current State](#current-state)
3. [Architecture & Project Structure](#architecture--project-structure)
4. [Technology Stack](#technology-stack)
5. [Development Workflows](#development-workflows)
6. [Coding Conventions](#coding-conventions)
7. [Testing Standards](#testing-standards)
8. [Documentation Guidelines](#documentation-guidelines)
9. [AI Assistant Guidelines](#ai-assistant-guidelines)
10. [Project-Specific Information](#project-specific-information)

---

## Repository Overview

**AutoMexec Labs** is a monorepo showcasing applied engineering projects that explore automation, DevOps, and AI systems integration. The repository represents hands-on demonstrations of modern engineering leadership where automation, intelligence, and design intersect to accelerate developer productivity.

**Author:** Debasish Bhattacharjee
**Role:** Engineering Director | AI Generalist | DevSecOps Leader
**Location:** San Francisco Bay Area
**Contact:** debasish.bhattacharjee@automexec.com
**License:** MIT License (Copyright 2025)

### Core Themes

1. **AI Code Intelligence** - Automated code review, coverage, and refactoring tools powered by OpenAI & Replicate
2. **Workflow Automation** - No-code orchestration using n8n for end-to-end DevSecOps and release flows
3. **Cloud Orchestration** - Deploying front- and back-end systems across AWS, GCP, and Vercel
4. **Observability** - CI/CD integration with real-time log tracing, test analytics, and error telemetry

---

## Current State

**Repository Stage:** Skeleton/Foundation Phase

**Existing Files:**
- `README.md` - Project overview and vision
- `LICENSE` - MIT License
- `.gitignore` - Comprehensive ignore patterns for Node.js, Python, and cloud tooling
- `CLAUDE.md` - This file

**Implementation Status:** The repository contains only foundational files. The five planned projects described in the README are architectural placeholders and have not yet been implemented.

**Git Configuration:**
- Current branch pattern: `claude/claude-md-*` (feature branches)
- Main branch: To be established
- Remote: Git proxy configuration in place

---

## Architecture & Project Structure

### Intended Monorepo Structure

The repository is designed as a monorepo containing five independent projects:

```
automexec-labs/
├── .git/
├── .github/
│   └── workflows/           # CI/CD workflows (to be created)
├── ai-code-reviewer/        # Project 1 (planned)
│   ├── src/
│   ├── tests/
│   ├── config/
│   ├── package.json or requirements.txt
│   ├── Dockerfile
│   └── README.md
├── ai-code-coverage/        # Project 2 (planned)
│   └── [similar structure]
├── ai-code-understanding/   # Project 3 (planned)
│   └── [similar structure]
├── cloud-ci-observability/  # Project 4 (planned)
│   └── [similar structure]
├── end-to-end-app/          # Project 5 (planned)
│   ├── frontend/
│   ├── backend/
│   └── [similar structure]
├── docs/                    # Shared documentation
├── scripts/                 # Automation and utility scripts
├── .gitignore
├── LICENSE
├── README.md
└── CLAUDE.md
```

### Planned Projects

| Project | Description | Primary Tech Stack | Status |
|---------|-------------|-------------------|--------|
| **ai-code-reviewer** | Intelligent PR analyzer that reviews code quality, suggests improvements, and identifies potential bugs using LLMs | Replicate, OpenAI API, GitHub Actions, TypeScript/Python | Not Started |
| **ai-code-coverage** | Automatically generates and analyzes coverage reports from test runs with AI-powered gap analysis | Jest, Pytest, Coverage.py, Python | Not Started |
| **ai-code-understanding** | Helps developers understand large legacy codebases through semantic search and AI-powered explanations | LangChain, OpenAI Embeddings, Vector DB (Pinecone/Weaviate), Python | Not Started |
| **cloud-ci-observability** | Monitors CI/CD pipelines and infrastructure health with dashboards and alerts | Prometheus, Grafana, n8n, Docker | Not Started |
| **end-to-end-app** | Full-stack web application (frontend + backend) deployed via automated cloud pipeline | Node.js, React, AWS/GCP, Docker, Terraform | Not Started |

---

## Technology Stack

### Languages
- **Python** (3.9+) - For AI/ML projects, data processing, and automation
- **TypeScript/JavaScript** (Node.js 18+) - For web applications and automation tools
- **Bash/Shell** - For scripts and CI/CD automation

### Frameworks & Libraries

**AI/ML:**
- OpenAI API (GPT models)
- Replicate (LLM hosting)
- LangChain (AI orchestration)
- Hugging Face (ML models)

**Backend:**
- Node.js with Express/Fastify
- Python with FastAPI/Flask

**Frontend:**
- React (with TypeScript)
- Next.js or Vite for build tooling

**Workflow Automation:**
- n8n (workflow orchestration)
- GitHub Actions (CI/CD)

**Cloud & Infrastructure:**
- AWS (Lambda, EC2, S3, CloudWatch)
- GCP (Cloud Functions, Cloud Run)
- Vercel (frontend deployment)
- Docker & Docker Compose
- Terraform (Infrastructure as Code)

**Testing:**
- Jest (JavaScript/TypeScript)
- Pytest (Python)
- Coverage.py (Python coverage)
- nyc/istanbul (JavaScript coverage)

**Observability:**
- Prometheus (metrics)
- Grafana (dashboards)
- CloudWatch/Stackdriver (cloud logging)

### Package Managers
- **Node.js:** npm, yarn, or pnpm
- **Python:** pip with virtual environments (venv) or Poetry

---

## Development Workflows

### Git Workflow

**Branch Naming Conventions:**
- Feature branches: `claude/claude-md-*` or `feature/<feature-name>`
- Bugfix branches: `bugfix/<issue-name>`
- Hotfix branches: `hotfix/<critical-fix>`

**Commit Message Format:**
```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, semicolons, etc.)
- `refactor`: Code refactoring without feature changes
- `test`: Adding or updating tests
- `chore`: Maintenance tasks, dependency updates
- `ci`: CI/CD configuration changes

**Example:**
```
feat(ai-code-reviewer): add LLM-based code quality analysis

Implement integration with OpenAI API to analyze pull requests
and provide automated code review comments focusing on:
- Code quality and best practices
- Potential bugs and edge cases
- Performance considerations

Closes #123
```

### Development Setup (For Future Implementation)

**For Node.js Projects:**
1. Install Node.js 18+ and npm/yarn
2. Run `npm install` or `yarn install`
3. Copy `.env.example` to `.env` and configure
4. Run `npm run dev` to start development server
5. Run `npm test` to execute tests

**For Python Projects:**
1. Install Python 3.9+
2. Create virtual environment: `python -m venv venv`
3. Activate: `source venv/bin/activate` (Linux/Mac) or `venv\Scripts\activate` (Windows)
4. Install dependencies: `pip install -r requirements.txt`
5. Copy `.env.example` to `.env` and configure
6. Run tests: `pytest`

### CI/CD Pipeline (Planned)

**GitHub Actions Workflows:**
- **Linting:** ESLint (JS/TS), Black/Flake8 (Python)
- **Testing:** Jest, Pytest with coverage thresholds
- **Building:** Docker image builds
- **Deployment:** Automated deployment to AWS/GCP/Vercel
- **Security:** Dependency scanning, SAST tools

---

## Coding Conventions

### General Principles

1. **Write Clean, Readable Code** - Prioritize clarity over cleverness
2. **Follow Language Idioms** - Use language-specific best practices
3. **Document Complex Logic** - Add comments for non-obvious code
4. **Keep Functions Small** - Single responsibility principle
5. **Error Handling** - Always handle errors gracefully
6. **Security First** - Avoid common vulnerabilities (XSS, SQL injection, etc.)

### TypeScript/JavaScript Conventions

```typescript
// Use TypeScript strict mode
// Use functional components with hooks (React)
// Use async/await over promises.then()
// Use const/let, never var
// Use meaningful variable names

// Example:
async function analyzeCodeQuality(code: string): Promise<AnalysisResult> {
  try {
    const result = await openai.chat.completions.create({
      model: "gpt-4",
      messages: [{ role: "user", content: code }]
    });
    return parseAnalysisResult(result);
  } catch (error) {
    logger.error("Code analysis failed", { error });
    throw new AnalysisError("Failed to analyze code", { cause: error });
  }
}
```

**File Naming:**
- Components: `PascalCase.tsx` (e.g., `CodeReviewer.tsx`)
- Utilities: `camelCase.ts` (e.g., `formatCode.ts`)
- Types: `PascalCase.types.ts` (e.g., `Analysis.types.ts`)

### Python Conventions

```python
# Follow PEP 8 style guide
# Use type hints for function signatures
# Use docstrings for classes and functions
# Use dataclasses or Pydantic for structured data

from typing import List, Optional
from dataclasses import dataclass

@dataclass
class CodeAnalysis:
    """Represents the result of a code quality analysis."""
    score: float
    issues: List[str]
    suggestions: List[str]

async def analyze_code(code: str, model: str = "gpt-4") -> CodeAnalysis:
    """
    Analyze code quality using OpenAI API.

    Args:
        code: Source code to analyze
        model: OpenAI model to use

    Returns:
        CodeAnalysis object with results

    Raises:
        AnalysisError: If analysis fails
    """
    try:
        # Implementation here
        pass
    except Exception as e:
        logger.error(f"Code analysis failed: {e}")
        raise AnalysisError("Failed to analyze code") from e
```

**File Naming:**
- Modules: `snake_case.py` (e.g., `code_analyzer.py`)
- Classes: `PascalCase` in `snake_case.py` files
- Tests: `test_*.py` or `*_test.py`

### Environment Variables

**Never commit secrets or API keys!**

Use `.env` files (gitignored) with `.env.example` as a template:

```bash
# .env.example
OPENAI_API_KEY=your_api_key_here
REPLICATE_API_TOKEN=your_token_here
AWS_REGION=us-west-2
DATABASE_URL=postgresql://localhost/dbname
NODE_ENV=development
```

---

## Testing Standards

### Coverage Requirements

- **Minimum Coverage:** 80% for all projects
- **Critical Paths:** 100% coverage for security and business logic

### Test Structure

**JavaScript/TypeScript (Jest):**
```typescript
describe('CodeAnalyzer', () => {
  describe('analyzeCode', () => {
    it('should return analysis result for valid code', async () => {
      const code = 'function test() { return 42; }';
      const result = await analyzeCode(code);

      expect(result.score).toBeGreaterThan(0);
      expect(result.issues).toBeInstanceOf(Array);
    });

    it('should handle API errors gracefully', async () => {
      const invalidCode = '';

      await expect(analyzeCode(invalidCode))
        .rejects.toThrow(AnalysisError);
    });
  });
});
```

**Python (Pytest):**
```python
import pytest
from code_analyzer import analyze_code, AnalysisError

class TestCodeAnalyzer:
    @pytest.mark.asyncio
    async def test_analyze_code_success(self):
        code = "def test(): return 42"
        result = await analyze_code(code)

        assert result.score > 0
        assert isinstance(result.issues, list)

    @pytest.mark.asyncio
    async def test_analyze_code_handles_errors(self):
        with pytest.raises(AnalysisError):
            await analyze_code("")
```

### Running Tests

```bash
# JavaScript
npm test                    # Run all tests
npm run test:watch          # Watch mode
npm run test:coverage       # With coverage report

# Python
pytest                      # Run all tests
pytest -v                   # Verbose output
pytest --cov=src            # With coverage
pytest -k "test_analyze"    # Run specific tests
```

---

## Documentation Guidelines

### Code Documentation

1. **README.md in Each Project Directory**
   - Project overview and purpose
   - Installation instructions
   - Usage examples
   - API documentation (if applicable)
   - Environment variables
   - Development setup

2. **Inline Comments**
   - Explain "why" not "what"
   - Document complex algorithms
   - Add TODOs with issue references: `// TODO(#123): Fix edge case`

3. **API Documentation**
   - Use JSDoc for TypeScript/JavaScript
   - Use docstrings for Python
   - Include examples in documentation

### Architecture Documentation

- **ADRs (Architecture Decision Records):** Document significant architectural decisions in `docs/adr/`
- **Diagrams:** Use Mermaid for flowcharts and architecture diagrams
- **Runbooks:** Document operational procedures in `docs/runbooks/`

---

## AI Assistant Guidelines

### When Working on This Repository

1. **Understand the Context**
   - This is a **skeleton repository** - most projects are not yet implemented
   - Focus on building solid foundations for each project
   - Follow the established patterns in README and this document

2. **Project Creation Guidelines**
   - When creating new projects, follow the intended directory structure
   - Always include README, tests, and configuration files
   - Use the technology stack specified for each project
   - Set up proper .env.example files

3. **Code Quality Standards**
   - Write production-ready code with proper error handling
   - Include comprehensive tests (aim for 80%+ coverage)
   - Add proper logging and observability hooks
   - Follow security best practices (no hardcoded secrets, input validation, etc.)

4. **Documentation Requirements**
   - Update project-specific README.md files
   - Add inline documentation for complex logic
   - Update this CLAUDE.md file when introducing new patterns or conventions
   - Keep README.md in sync with actual implementation

5. **Git Workflow**
   - Work on feature branches following naming conventions
   - Write clear, descriptive commit messages
   - Commit frequently with logical changesets
   - Push to the designated branch when complete

6. **Dependencies Management**
   - Use specific version numbers, avoid wildcards in production
   - Document why dependencies are added
   - Keep dependencies up to date
   - Minimize dependency count (prefer standard library when possible)

7. **Security Considerations**
   - Never commit API keys, tokens, or passwords
   - Use environment variables for all secrets
   - Validate and sanitize all user inputs
   - Follow OWASP guidelines for web applications
   - Implement proper authentication and authorization

8. **Testing Philosophy**
   - Write tests before or alongside implementation (TDD encouraged)
   - Test edge cases and error conditions
   - Use meaningful test descriptions
   - Mock external API calls in tests

9. **AI/LLM Integration Best Practices**
   - Implement rate limiting for API calls
   - Add retry logic with exponential backoff
   - Cache responses when appropriate
   - Monitor token usage and costs
   - Provide fallback mechanisms for API failures

10. **Observability**
    - Add structured logging (JSON format preferred)
    - Include correlation IDs for request tracing
    - Expose metrics endpoints (Prometheus format)
    - Set up health check endpoints
    - Document alerting thresholds

### Common Tasks

**Creating a New Project:**
```bash
# 1. Create project directory structure
mkdir -p <project-name>/{src,tests,config,docs}

# 2. Initialize package manager
cd <project-name>
npm init -y  # or python -m venv venv && pip install ...

# 3. Create essential files
touch README.md .env.example Dockerfile .dockerignore

# 4. Set up testing framework
# (Install Jest/Pytest and create test config)

# 5. Create GitHub Actions workflow
mkdir -p ../.github/workflows
# (Create CI/CD workflow file)

# 6. Update root README.md to reflect new project status
```

**Adding a New Feature:**
1. Create feature branch: `git checkout -b feature/<feature-name>`
2. Implement feature with tests
3. Update documentation
4. Run linting and tests locally
5. Commit with conventional commit message
6. Push to remote branch

**Debugging Issues:**
- Check logs first (structured logging helps!)
- Verify environment variables are set correctly
- Ensure all dependencies are installed
- Check API rate limits and quotas
- Review error messages in CI/CD pipelines

---

## Project-Specific Information

### ai-code-reviewer

**Purpose:** Automated PR review using LLMs

**Key Features:**
- Integration with GitHub webhooks
- OpenAI/Replicate API for code analysis
- Automated comment posting on PRs
- Configurable review rules

**Tech Stack:** TypeScript, OpenAI API, Replicate, GitHub Octokit

**Environment Variables:**
```
OPENAI_API_KEY=
REPLICATE_API_TOKEN=
GITHUB_TOKEN=
WEBHOOK_SECRET=
```

---

### ai-code-coverage

**Purpose:** AI-enhanced code coverage analysis

**Key Features:**
- Parse coverage reports from Jest/Pytest
- AI-powered gap analysis
- Suggest test cases for uncovered code
- Generate coverage badges

**Tech Stack:** Python, Coverage.py, OpenAI API

**Environment Variables:**
```
OPENAI_API_KEY=
COVERAGE_THRESHOLD=80
```

---

### ai-code-understanding

**Purpose:** Semantic code search and understanding

**Key Features:**
- Code embedding generation
- Vector database for semantic search
- Natural language queries over codebase
- Explain complex code sections

**Tech Stack:** Python, LangChain, OpenAI Embeddings, Pinecone/Weaviate

**Environment Variables:**
```
OPENAI_API_KEY=
PINECONE_API_KEY=
PINECONE_ENVIRONMENT=
```

---

### cloud-ci-observability

**Purpose:** CI/CD and infrastructure monitoring

**Key Features:**
- Prometheus metrics collection
- Grafana dashboards
- n8n workflow automation
- Alerting and notifications

**Tech Stack:** Docker, Prometheus, Grafana, n8n, Python/Node.js

**Environment Variables:**
```
PROMETHEUS_URL=
GRAFANA_API_KEY=
SLACK_WEBHOOK_URL=
N8N_ENCRYPTION_KEY=
```

---

### end-to-end-app

**Purpose:** Full-stack reference application

**Key Features:**
- React frontend with TypeScript
- Node.js backend API
- PostgreSQL database
- Docker Compose for local development
- Terraform for cloud deployment

**Tech Stack:** React, TypeScript, Node.js, Express, PostgreSQL, Docker, Terraform, AWS/GCP

**Environment Variables:**
```
DATABASE_URL=
JWT_SECRET=
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
FRONTEND_URL=
BACKEND_URL=
```

---

## Maintenance and Updates

### Keeping This Document Updated

This CLAUDE.md file should be updated whenever:
- New projects are added or removed
- Coding conventions change
- New tools or frameworks are introduced
- Development workflows are modified
- New best practices are established

### Version History

- **v1.0.0** (2025-01-16) - Initial creation for skeleton repository

---

## Quick Reference

### Useful Commands

```bash
# Git
git status
git checkout -b feature/new-feature
git add .
git commit -m "feat: add new feature"
git push -u origin feature/new-feature

# Node.js
npm install
npm run dev
npm test
npm run lint
npm run build

# Python
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
pytest
black src/
flake8 src/

# Docker
docker-compose up -d
docker-compose logs -f
docker-compose down
docker build -t project-name .
```

### Important Files and Directories

- `README.md` - Project overview
- `LICENSE` - MIT License
- `.gitignore` - Comprehensive ignore patterns
- `CLAUDE.md` - This file (AI assistant guide)
- `.env.example` - Environment variable templates (to be created)
- `.github/workflows/` - CI/CD workflows (to be created)

---

## Support and Contact

**Repository Owner:** Debasish Bhattacharjee
**Email:** debasish.bhattacharjee@automexec.com
**LinkedIn:** [linkedin.com/in/debasishtech](https://www.linkedin.com/in/debasishtech)

For issues, questions, or suggestions, please open a GitHub issue or contact the repository owner directly.

---

**Last Updated:** 2025-01-16
**Document Version:** 1.0.0
**Repository Stage:** Skeleton/Foundation Phase
