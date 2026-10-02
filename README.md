# Personal AI Engine

A personal AI assistant concept web app — an interactive dashboard for managing, importing, and searching your own knowledge base through a neural-style interface. Includes a landing page, profile cards, import panel, neural network visualization, project roadmap, waitlist, and settings.

## Features

- **Landing experience** — animated hero, manage/design/deploy sections, use cases, testimonials, loading screen
- **Personal knowledge dashboard** — Manage page with project cards and roadmap
- **Import panel** — bring in your own data sources
- **Search** — semantic-style search over your personal knowledge
- **Neural visualization** — animated neural-node graph components
- **Profile & settings** — user profile card, theme toggle, preferences
- **Mock auth** — client-side login/logout state persisted in `localStorage` (no backend required)

## Tech Stack

- React 18 + TypeScript
- Vite 5
- Tailwind CSS + tailwindcss-animate
- shadcn/ui component library (Radix primitives)
- React Router v6, React Query, React Hook Form + Zod
- Framer Motion, recharts, embla-carousel, cmdk

## Quick Start

```sh
# Install dependencies
npm install

# Start the dev server
npm run dev

# Build for production
npm run build

# Preview the production build
npm run preview
```

## Project Structure

```
Personal-AI-Engine/
├── index.html          # Entry HTML
├── src/
│   ├── App.tsx         # Router + providers (Auth, Theme, QueryClient)
│   ├── main.tsx        # React entry point
│   ├── pages/          # Index, WhyPage, HowPage, Profile, Import,
│   │                   # SearchPage, Settings, ManagePage, NotFound
│   ├── components/
│   │   ├── landing/    # Hero, Manage, Design, Deploy, UseCases,
│   │   │               # Testimonials, CallToAction sections
│   │   ├── manage/     # Dashboard manage components
│   │   ├── projects/   # Project roadmap/cards
│   │   ├── search/     # Search UI
│   │   ├── waitlist/   # Waitlist components
│   │   └── ui/         # shadcn/ui primitives
│   ├── contexts/       # Auth (mock) + Theme contexts
│   ├── hooks/          # Reusable hooks
│   ├── lib/            # Utilities, animations
│   └── types/          # TypeScript types
├── public/             # Static assets
└── package.json
```

## Environment Variables

None required — the app runs fully client-side. Auth is a mock persisted in `localStorage`.

## Deploy

Static build — deploy `dist/` to any static host:

- **Cloudflare Pages:** `cloudflare pages_deploy personal-ai-engine dist`
- **Netlify / Vercel / GitHub Pages:** build with `npm run build` and serve `dist/`

---

Built by Girish Lade — https://ladestack.in
