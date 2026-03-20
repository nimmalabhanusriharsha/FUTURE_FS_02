# Apex CRM

Apex CRM is a polished lead management dashboard built for small teams, agencies, and independent operators who need a fast way to capture, organize, and convert inbound leads.

It combines a clean React interface with Supabase authentication and database storage, giving you a focused CRM workflow without the overhead of a large enterprise system.

## Highlights

- Secure email and password authentication
- Lead pipeline with status tracking for new, contacted, and converted leads
- Search, filter, pagination, and quick actions across the lead list
- Recent activity and visual reporting on the dashboard
- Follow-up notes for lead conversations and context
- Profile management and password update flows
- Responsive UI built with Tailwind CSS, shadcn/ui, and Framer Motion

## Tech Stack

- React 18
- TypeScript
- Vite
- Tailwind CSS
- shadcn/ui
- Framer Motion
- Supabase
- ESLint

## Project Structure

```text
src/
  components/        UI primitives and CRM-specific components
  hooks/             Auth and lead data hooks
  integrations/      Supabase client and generated types
  pages/             Route-level screens
supabase/
  migrations/        Database schema migrations
```

Core frontend entry files are kept around:

- `index.html`
- `src/main.tsx`
- `src/index.css`
- `package.json`
- `package-lock.json`
- `README.md`

Supabase backend files in `supabase/` remain unchanged.

## Getting Started

### Prerequisites

- Node.js 18 or newer
- npm
- A Supabase project

### Environment Variables

Create a `.env` file in the project root:

```env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_PUBLISHABLE_KEY=your_supabase_anon_key
```

### Install and Run

```sh
npm install
npm run dev
```

The app will start on the local Vite development server.

## Database Setup

Supabase migrations are stored in `supabase/migrations`.

Apply the SQL migration to your Supabase project before using the authenticated CRM flows. The app expects the backing tables, auth setup, and policies to exist in Supabase.

## Available Scripts

```sh
npm run dev
npm run build
npm run preview
npm run lint
```

## Quality Checks

The project currently supports:

- Production builds with `npm run build`
- Linting with `npm run lint`

## Product Screens

The current app includes these main areas:

- Login and account creation
- Dashboard with lead metrics and charts
- Lead management table with search and filtering
- Lead detail drawer and edit dialog
- Settings page for profile and password updates

## Deployment Notes

Before deploying, verify these items:

- Environment variables are set correctly
- Supabase auth is configured for your target domain
- Database migrations have been applied
- Row-level security and policies match your access model

