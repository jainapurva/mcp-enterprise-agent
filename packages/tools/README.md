# Tools Package

This package contains all MCP tools for knowledge base search, resource queries, case management, identity verification, notifications, and escalation.

## Purpose
- MCP tool implementations with consistent interfaces
- Knowledge base search using embeddings and LiquidMetal
- Resource querying through configured adapters
- Case management with Convex integration
- Identity verification with OTP
- Notification services (email/SMS)
- Escalation handling

## Tools
- `kb.search.ts` - Knowledge base search with RAG
- `resource.query.ts` - Dynamic resource querying
- `case.create.ts` - Case creation
- `case.lookup.ts` - Case retrieval
- `case.update.ts` - Case status updates
- `identity.verify.ts` - OTP-based verification
- `notify.send.ts` - Email and SMS notifications
- `escalate.transfer.ts` - Escalation handling

## Usage
```typescript
import { KbSearchTool, ResourceQueryTool } from '@mcp-enterprise/tools';

const kbTool = new KbSearchTool(config);
const results = await kbTool.execute({ query: 'support hours' });

const resourceTool = new ResourceQueryTool(config);
const data = await resourceTool.execute({ 
  resource: 'orders', 
  operation: 'lookup', 
  params: { order_id: 'ORD-001' } 
});
```