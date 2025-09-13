# Admin UI

This directory contains the React/Vite admin console.

## Purpose
- WorkOS authentication and login
- Configuration file upload and preview
- Session management and log viewing
- Demo buttons for testing (flip case status, OTP test)
- LiquidMetal powered search across KB and resources
- Real-time case status monitoring

## Structure
```
admin_ui/
├── src/
│   ├── components/      # React components
│   ├── pages/          # Page components
│   ├── hooks/          # Custom hooks
│   ├── utils/          # Utility functions
│   ├── types/          # TypeScript types
│   └── main.tsx        # App entry point
├── public/
├── package.json
├── vite.config.ts
└── tsconfig.json
```

## Features
- `/config` - Configuration management
- `/sessions` - Session logs and monitoring
- `/demo` - Testing and demonstration tools
- `/search` - KB and resource search