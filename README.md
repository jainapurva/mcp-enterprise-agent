# MCP Enterprise Agent

A config-driven enterprise voice agent built with the Model Context Protocol (MCP). This system provides a flexible, extensible platform for handling customer support interactions through voice, with configurable knowledge bases, resources, and routing logic.

## Architecture

This repository follows a modular monorepo structure:

```
mcp-enterprise-agent/
├─ apps/
│ ├─ mcp_server/     # MCP HTTP interface
│ ├─ orchestrator/   # Routing + voice webhooks  
│ └─ admin_ui/       # React/Vite console
├─ packages/
│ ├─ core/           # config schema/loader, jsonpath, types
│ ├─ adapters/       # rest, csv data sources
│ └─ tools/          # kb.search, resource.query, case.*, verify, notify, escalate
├─ infra/
│ ├─ convex/         # schema + functions (cases, otp, sessions)
│ ├─ smithery/       # deploy spec
│ ├─ docker/         # Dockerfiles
│ └─ github/         # CI workflows
├─ configs/
│ ├─ example.config.yaml  # Sample configuration
│ ├─ demo.orders.csv      # Sample orders data
│ └─ demo.cases.csv       # Sample cases data
├─ scripts/          # smoke tests, seeders
├─ .env.example      # Environment variables template
└─ README.md
```

## Quick Start

1. **Copy environment variables:**
   ```bash
   cp .env.example .env
   # Edit .env with your API keys and configuration
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Run the system:**
   ```bash
   npm run dev
   ```

## Features

- **Config-driven**: No code changes needed for new use cases
- **Voice integration**: Vapi-powered voice interactions
- **Flexible data sources**: REST APIs, CSV files, with SQL support planned
- **Real-time updates**: Convex-powered live case status updates
- **Authentication**: WorkOS integration for admin access
- **Notifications**: Email via Google Lab, SMS via Vapi
- **Search**: LiquidMetal-powered fuzzy search
- **Deployment**: Smithery-based containerized deployment

## Sponsor Integrations

This project integrates with several sponsor technologies:
- **Vapi** - Voice AI platform for ASR/TTS and SMS
- **Convex** - Real-time database and backend functions
- **WorkOS** - Authentication and user management
- **Google Lab** - Email services and embeddings
- **LiquidMetal** - Advanced search capabilities
- **Smithery** - Container deployment platform

## Configuration

See `configs/example.config.yaml` for a complete configuration example. The system supports:

- **Knowledge Base**: Define FAQ documents and policies
- **Resources**: Configure data sources (CSV, REST API)
- **Routing**: Map keywords to tools and actions
- **Policy**: Set PII handling, OTP requirements, escalation rules

## Development

Each directory contains its own README with specific development instructions. Key commands:

```bash
# Run tests
npm test

# Lint code  
npm run lint

# Build all packages
npm run build

# Run smoke tests
npm run smoke-test
```

For detailed architecture and implementation details, see the `PROJECT_PLAN` file.