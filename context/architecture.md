# Architecture Context

## Stack

| Layer     | Technology                | Role |
|----------|--------------------------|------|
| Framework | Next.js + TypeScript     | Fullstack (UI + API routes) |
| UI        | Tailwind + shadcn/ui     | Component system |
| Auth      | Hardcoded credentials    | Simple admin access |
| Database  | Prisma + SQLite (dev) / PostgreSQL (prod) | Data persistence |
| Notifications | Node mailer / cron jobs | Email alerts |

## Feature-Based Architecture

The project is organized by business feature instead of technical layer.

## System Boundaries

- `app/` — Next.js routes, layouts, and pages
- `features/auth/` — login, session handling, route protection
- `features/users/` — user CRUD and user profile logic
- `features/devices/` — MAC address registration and device ownership
- `features/wifi-networks/` — WiFi network CRUD and assignment logic
- `features/subscriptions/` — subscription creation, pricing, duration, and expiration logic
- `features/notifications/` — in-app notifications, email reminders, notification logs
- `components/ui/` — generated shadcn/ui components only
- `components/shared/` — reusable app-specific UI components
- `lib/` — shared utilities, Prisma client, constants, validation helpers
- `prisma/` — Prisma schema, migrations, seed data

## Feature Folder Pattern

Each feature should keep its own UI, actions, validation, and business logic close together.

```txt
features/
  users/
    components/
    actions/
    schemas/
    services/
    types.ts

## Storage Model

- **Database (Prisma)**:
  - Users
  - Devices (MAC addresses)
  - WiFi networks
  - Subscriptions
  - Notification logs  

- No file/blob storage required  

## Auth and Access Model

- Single admin user stored in DB  
- Credentials hardcoded via seed  
- No public signup  
- All routes protected  

## Invariants

1. Every device must belong to exactly one user  
2. Every subscription must be linked to a device  
3. Subscription price must always match duration rules  
4. Expiration logic must remain consistent and deterministic  