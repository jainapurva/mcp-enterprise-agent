# Convex Infrastructure

This directory contains Convex database schema definitions and functions.

## Purpose
- Database schema for cases, OTP tokens, and sessions
- Real-time database functions and triggers
- WebSocket handlers for live updates
- Data persistence and querying logic

## Structure
```
convex/
├── schema.ts            # Database schema definitions
├── functions/
│   ├── cases.ts         # Case management functions
│   ├── otp.ts          # OTP token handling
│   ├── sessions.ts     # Session management
│   └── webhooks.ts     # Real-time webhook handlers
├── convex.json         # Convex configuration
└── package.json
```

## Tables
- `cases` - Support case records
- `otp_tokens` - One-time password tokens
- `sessions` - Voice/chat session data
- `audit_logs` - System activity logs