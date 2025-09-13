# Docker Infrastructure

This directory contains Docker configurations for containerized deployment.

## Purpose
- Dockerfiles for each service
- Multi-stage build optimization
- Development and production configurations
- Docker Compose for local development

## Files
```
docker/
├── Dockerfile.mcp-server     # MCP server container
├── Dockerfile.orchestrator   # Orchestrator container  
├── Dockerfile.admin-ui       # Admin UI container
├── docker-compose.yml        # Local development setup
└── docker-compose.prod.yml   # Production configuration
```

## Usage
```bash
# Local development
docker-compose up -d

# Production build
docker build -f docker/Dockerfile.mcp-server -t mcp-server .
```