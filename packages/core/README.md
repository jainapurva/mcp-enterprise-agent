# Core Package

This package contains core configuration schema, loader, JSONPath utilities, and shared types.

## Purpose
- Configuration schema validation using Zod
- Configuration file loading and parsing
- JSONPath wrapper for data transformation
- Shared TypeScript types across the system

## Modules
- `config.schema.ts` - Zod schema definitions
- `config.loader.ts` - Configuration loading and validation
- `jsonpath.ts` - JSONPath utilities for data mapping
- `types/` - Shared TypeScript type definitions

## Usage
```typescript
import { loadConfig } from '@mcp-enterprise/core';
import { mapFields } from '@mcp-enterprise/core/jsonpath';

const config = await loadConfig('./config.yaml');
const mapped = mapFields(data, config.resources[0].operations.lookup.map);
```