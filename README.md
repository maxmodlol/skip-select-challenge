# Skip Select Challenge

A responsive, accessible React + TypeScript application for selecting skip sizes, redesigned with Material UI, React Query, and Vite. This project demonstrates clean, maintainable code, UI/UX improvements, dark/light theming, and full responsiveness across mobile, tablet, and desktop.

## 🚀 Features

- **Responsive grid** of skip cards (1–3 columns by viewport)
- **Animated marquee** on mobile for selected info
- **Sticky action bar** with back/continue actions and warning for restricted skips
- **Custom Stepper** replacing default Material UI Stepper on small screens
- **Dark & Light theme toggle** with persistence
- **Data fetching** via React Query and Axios, with environment-configured API URL
- **TypeScript** for type safety and clear interfaces
- **Linting & formatting**: ESLint + Prettier

## 🗂️ Project Structure

```
skip-select-challenge/
├── public/                 # Static assets
│   └── skip-placeholder.jpg
├── src/
│   ├── api/                # HTTP clients (Axios)
│   │   └── getSkipOptions.ts
│   ├── assets/             # Images, fonts, icons
│   ├── components/         # Reusable UI components
│   │   ├── SkipCard/
│   │   │   ├── index.tsx
│   │   │   └── types.ts
│   │   ├── StickyBar/
│   │   │   ├── index.tsx
│   │   │   └── types.ts
│   │   └── StepperStatic/  # Custom Stepper + SpeedDial
│   │       └── index.tsx
│   ├── config/             # Vite and alias config (vite.config.ts)
│   ├── hooks/              # Custom React Query hooks
│   │   └── useSkipOptions.ts
│   ├── theme/              # MUI theme overrides, ModeToggle
│   │   └── index.tsx
│   ├── types/              # Shared TypeScript interfaces
│   ├── App.tsx             # Main layout & routing
│   ├── main.tsx            # App entrypoint (ThemeProvider, QueryClient)
│   ├── index.css           # Global resets & base styles
│   └── vite-env.d.ts       # Vite env type declarations
├── .env.example            # Copy → .env.local with your API URL
├── .gitignore
├── README.md
├── package.json
├── tsconfig.json
└── vite.config.ts          # Vite + alias config
```

## 🔧 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) >= 16
- [pnpm](https://pnpm.io/) (or npm / yarn)

### Installation

```bash
# clone repo
git clone https://github.com/maxmodlol/skip-select-challenge.git
cd skip-select-challenge

# install deps
pnpm install

# copy env example
cp .env.example .env.local
# edit .env.local if needed
```

### Available Scripts

- `pnpm dev` — run Vite dev server
- `pnpm build` — build for production
- `pnpm preview` — preview production build
- `pnpm lint` — run ESLint

## 🌐 Environment Variables

Create `.env.local` at project root:

```env
VITE_API_URL=https://app.wewantwaste.co.uk/api
```

## 📐 Approach & Decisions

- **Vite + React + TS** for fast iteration and type safety
- **Material UI v7** for accessible, themeable components
- **React Query** for caching and easy data-fetching logic
- **Axios** wrapped in `src/api/getSkipOptions.ts` for extensibility
- **Alias `@/` → `src/`** for cleaner imports (configured in `vite.config.ts` and `tsconfig.json`)
- **Dark/light mode** via MUI `ThemeProvider` and custom `ModeToggle`
- **Responsive design**: breakpoints, grid layout, marquee animation on mobile
- **Custom Stepper** that degrades into a SpeedDial on small screens to maintain clarity
- **StickyBar** for persistent call-to-action at viewport bottom

## 🤝 Contributing

Contributions welcome! Please open issues or PRs for improvements or bug fixes.

## 📄 License

[MIT](LICENSE)
Abd Al-kareem Abu Al-soud

---

_Designed & developed with care._
