# Fixora

Fixora is a professional, multi-page frontend for a home services marketplace.  
It is built with React + TypeScript using a layered architecture so UI growth does not break domain and application boundaries.

## Highlights

- Light-themed, responsive multi-page website
- Clean route structure (`Home`, `Services`, `How It Works`, `About`)
- Layered architecture (`domain`, `application`, `infrastructure`, `presentation`)
- Reusable component system and typed data flow
- Production-ready lint and build setup with Vite + ESLint + TypeScript

## Tech Stack

- React 19
- TypeScript
- Vite
- React Router v7
- Framer Motion
- Lucide React
- Tailwind CSS + PostCSS (configured)
- ESLint + TypeScript ESLint

## Project Structure

```text
src
├── app
│   ├── App.tsx
│   └── routes.tsx
├── domain
│   ├── entities
│   └── interfaces
├── application
│   ├── dto
│   ├── services
│   └── use-cases
├── infrastructure
│   └── repositories
├── presentation
│   ├── components
│   │   ├── common
│   │   ├── features
│   │   └── layout
│   ├── hooks
│   └── pages
├── shared
│   ├── constants
│   └── utils
└── main.tsx
```

## Architecture

### Domain Layer

- Holds business entities and contracts
- No framework-specific dependencies

### Application Layer

- Contains use cases and presenters
- Converts domain/infrastructure data into UI-ready view models

### Infrastructure Layer

- Implements repository contracts
- Currently provides an in-memory dataset for marketplace content

### Presentation Layer

- Route pages, layout, UI components, hooks
- Consumes application-layer outputs only

## Pages

- `/` Home: hero, trust signals, featured services
- `/services` Full service catalog with pricing and ratings
- `/how-it-works` booking flow and platform model
- `/about` architecture principles and category snapshot

## Getting Started

### 1. Install dependencies

```bash
npm install
```

### 2. Start development server

```bash
npm run dev
```

### 3. Build for production

```bash
npm run build
```

### 4. Run lint checks

```bash
npm run lint
```

## Scripts

- `npm run dev` - start Vite dev server
- `npm run build` - run TypeScript build and Vite production bundle
- `npm run lint` - run ESLint across the project
- `npm run preview` - preview production build locally

## Design Goals

- Keep content readable by splitting concerns across focused pages
- Prioritize clarity: strong hierarchy, spacing, and visual breathing room
- Use reusable components instead of page-level duplication
- Maintain structure suitable for scaling into real booking flows

## Roadmap

- Authentication and role-based flows (customer/provider)
- Service booking form with validation and scheduling
- Provider dashboard and booking management
- API-backed repository implementation
- Test coverage for use cases and critical UI paths

## License

This project is currently unlicensed. Add a `LICENSE` file before public distribution.
