# Orchestrator

This directory contains the routing and voice webhook handler.

## Purpose
- Routes intents to appropriate tools based on configuration
- Handles voice webhooks from Vapi
- Enforces OTP requirements for sensitive operations
- Manages session persistence
- Optional LLM slot filling for parameter extraction

## Structure
```
orchestrator/
├── src/
│   ├── server.ts         # Main orchestration server
│   ├── router.ts         # Intent routing logic
│   ├── voice/           # Vapi webhook handlers
│   ├── session/         # Session management
│   └── llm/             # Optional LLM integration
├── package.json
└── tsconfig.json
```