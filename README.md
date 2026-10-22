# AIGADO

> An AI assistant project focused on conversational AI, image workflows, and a clean web experience.

<p align="center">
  <a href="https://aigado.lovable.app"><strong>Live demo</strong></a>
  ·
  <a href="https://github.com/gado-prog/GadoAi/issues">Report an issue</a>
</p>

## Overview

AIGADO (GadoAI) is a web-based AI assistant built with React, TypeScript, TanStack Start, and Supabase. The application includes a chat interface, conversation history, image-related workflows, voice input, account authentication, and light/dark themes.

**Live application:** https://aigado.lovable.app

## Features

- AI chat interface with streaming responses
- Per-account conversation history in browser storage
- Image upload and image-generation workflow integration
- Voice input and text-to-speech support
- Email/password authentication and Google sign-in integration
- Email verification flow and Telegram-related integration
- Responsive interface with light and dark themes
- Typing Arena and home-page motion components

> Feature availability depends on configured backend services and environment variables. Google OAuth currently requires provider configuration to be verified.

## Tech stack

- React 19 + TypeScript
- TanStack Start / Router
- Vite
- Supabase Auth and backend integration
- Tailwind CSS and component primitives
- Bun / npm

## Repository layout

```text
src/
├── components/       # Chat UI, shared components, arena and motion
├── hooks/            # Authentication, voice and responsive hooks
├── integrations/     # Supabase and Lovable integrations
├── lib/              # App utilities, i18n, OAuth helpers and tests
└── routes/           # App routes and server API endpoints
supabase/
└── migrations/       # Database migrations, when included in this checkout
```

## Getting started

### Requirements

- A current Node.js version supported by the project toolchain
- Bun or npm
- A configured Supabase project and the external services used by the app

### Install dependencies

```bash
npm install
```

### Configure environment

Create a local `.env` file from `.env.example` and set the values for your own backend. Never commit real credentials.

Common configuration names include:

- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_PUBLISHABLE_KEY`
- `SUPABASE_URL`
- `SUPABASE_PUBLISHABLE_KEY`
- Server-only keys required by enabled integrations

The browser publishable key is not a substitute for a server secret. Never expose service-role keys, bot tokens, passwords, or private API keys in client-side variables.

### Run locally

Use the script available in `package.json`, for example:

```bash
npm run dev
```

Check the project scripts before running build or lint commands.

## Authentication configuration

Google sign-in requires a correctly configured Google OAuth client and Supabase Auth provider. The Google OAuth callback must match the callback URL shown by Supabase, and the deployed and local app URLs must be allowed in Supabase URL Configuration.

Do not disable email verification or reset existing user data to troubleshoot authentication.

## Security

- Do not commit `.env`, `.env.*`, credentials, tokens, or user data.
- Keep privileged secrets server-side.
- Enable GitHub secret scanning and Dependabot alerts where available.
- Rotate credentials immediately if a secret is ever exposed.

## Project status

This repository is intended to contain the source code for the AIGADO application. External service configuration, database data, OAuth provider settings, and deployment secrets are not stored in Git. Confirm the latest source synchronization and run checks before presenting a build as verified.

## Author

Maintained by **gado-prog**.

---

Built with curiosity and a focus on practical AI.
