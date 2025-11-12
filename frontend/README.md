# Recipe Explorer Frontend (Astro)

A modern, responsive Astro app to browse and view recipes.

## Run locally

```bash
npm install
npm run dev
```

The dev server runs on http://localhost:3000.

## Configuration

Public environment variables:
- PUBLIC_API_BASE: Optional base URL to a recipes API. When not provided, the UI uses bundled mock data.

Create a `.env` file (optional):
```
PUBLIC_API_BASE=https://api.example.com
```

## Structure

- src/layouts/BaseLayout.astro — site layout, header, theme
- src/pages/index.astro — recipe grid with search
- src/pages/recipes/[id].astro — recipe detail
- src/components/ — UI components (Header, SearchBar, RecipeCard, Tag, Rating, Modal)
- src/lib/api.ts — API helpers read `import.meta.env.PUBLIC_API_BASE` safely
- src/lib/mockData.ts — mock recipes fallback

## Style

Ocean Professional theme:
- Primary: #2563EB
- Secondary/Success: #F59E0B
- Error: #EF4444
- Background: #f9fafb
- Surface: #ffffff
- Text: #111827

Accessible components with focus states and semantic HTML.
