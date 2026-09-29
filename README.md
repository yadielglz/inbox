# Glz Inbox

Dashboard-first unified communications at `inbox.glztech.com`.

## Current implementation

Phase 2 connects Google accounts with OAuth 2.0 + PKCE and reads live Gmail inbox metadata. The UI does not generate demonstration mailbox data: messages, labels, counts, account identities and empty states reflect provider responses.

## Google OAuth setup

Create a Google Cloud OAuth 2.0 Web application, enable the Gmail API, and configure the authorized redirect URI for the deployed app. Copy `.env.example` to `.env.local` for local development and set `VITE_GOOGLE_CLIENT_ID`.

> Current development implementation keeps short-lived access tokens in browser storage. Before public production use, OAuth token exchange, refresh-token custody and synchronization should move to a server-side Glz backend.

## Development

```bash
npm install
cp .env.example .env.local
npm run dev
```

Production build:

```bash
npm run build
```
