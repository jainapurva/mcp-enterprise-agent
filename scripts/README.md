# Scripts

This directory contains utility scripts for testing, seeding, and maintenance.

## Purpose
- Smoke tests for all system components
- Database seeding with demo data
- Development utilities and helpers
- Deployment verification scripts

## Scripts
- `smoke.ts` - End-to-end smoke tests
- `seed.ts` - Database seeding with demo data  
- `test-tools.ts` - Individual tool testing
- `validate-config.ts` - Configuration validation
- `setup-dev.ts` - Development environment setup

## Usage
```bash
# Run smoke tests
npm run smoke-test

# Seed demo data
npm run seed

# Validate configuration
npm run validate-config ./configs/example.config.yaml
```