# MCP Server

This directory contains the MCP HTTP interface server implementation.

## Purpose
- Exposes MCP (Model Context Protocol) HTTP endpoints
- Handles tool registration and execution
- Provides `/mcp/tools/list` and `/mcp/tool/:name/call` endpoints
- Includes PII masking middleware
- Hot-reload configuration endpoint
- WorkOS authentication middleware

## Structure
```
mcp_server/
├── src/
│   ├── server.ts         # Main HTTP server
│   ├── middleware/       # Auth, PII masking, etc.
│   ├── routes/          # MCP endpoints
│   └── types/           # MCP protocol types
├── package.json
└── tsconfig.json
```