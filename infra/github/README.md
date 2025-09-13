# GitHub CI/CD

This directory contains GitHub Actions workflows for continuous integration and deployment.

## Purpose
- Automated testing and linting on pull requests
- Container image building and registry push
- Automated deployment to staging/production
- Code quality checks and security scanning

## Workflows
```
github/
└── workflows/
    ├── ci.yml              # Continuous integration
    ├── build-and-deploy.yml # Build and deploy
    ├── security-scan.yml   # Security scanning
    └── release.yml         # Release automation
```

## CI Pipeline
1. Code checkout and dependency installation
2. TypeScript compilation and linting
3. Unit and integration test execution
4. Container image building
5. Deployment to target environments
6. Smoke test execution