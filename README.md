# Recipe Explorer

A modern Astro frontend for browsing, viewing, and managing recipes.

## Getting Started

- Node 18+ recommended.

Install dependencies:
```sh
cd frontend
npm install
```

Run locally:
```sh
npm run dev
```
Dev server runs at http://localhost:3000 (or the configured port).

## Environment Variables

This app reads the following public environment variable at build/runtime:

- PUBLIC_API_BASE: Base URL for a recipes API (e.g., https://api.example.com). If unset, the app uses local mock data and the home page and recipe details will render with the bundled mocks.

Other PUBLIC_* variables may exist but are not modified by this app. They will remain intact.

To set PUBLIC_API_BASE during development, create a `.env` in `frontend/`:
```
PUBLIC_API_BASE=https://your-api.example.com
```

## Features

- Ocean Professional theme with blue and amber accents, subtle gradients, rounded corners.
- Responsive recipe grid with search.
- Recipe detail page at `/recipes/[id]`.
- Accessible components with semantic markup and focus states.

## Project Structure

- src/layouts/BaseLayout.astro: global layout with header and theming
- src/pages/index.astro: recipe grid and client-side search
- src/pages/recipes/[id].astro: recipe detail page
- src/components/: Header, SearchBar, RecipeCard, Tag, Rating, Modal
- src/lib/api.ts: fetch helpers with PUBLIC_API_BASE fallback to mocks
- src/lib/mockData.ts: mock recipes

## License

MIT