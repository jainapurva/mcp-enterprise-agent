# Adapters Package

This package contains data source adapters for REST APIs, CSV files, and future SQL databases.

## Purpose
- REST API adapter with templating, query parameters, and error handling
- CSV adapter supporting filter and append operations
- Standardized adapter interface for consistent data access
- Request/response transformation and normalization

## Modules
- `rest.adapter.ts` - REST API integration
- `csv.adapter.ts` - CSV file operations
- `base.adapter.ts` - Common adapter interface
- `types.ts` - Adapter type definitions

## Usage
```typescript
import { RestAdapter, CsvAdapter } from '@mcp-enterprise/adapters';

const restAdapter = new RestAdapter(config.restConfig);
const result = await restAdapter.query('users', 'lookup', { id: '123' });

const csvAdapter = new CsvAdapter('./data.csv');
const records = await csvAdapter.filter({ status: 'active' });
```