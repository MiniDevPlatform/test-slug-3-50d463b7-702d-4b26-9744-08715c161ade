# {{PROJECT_NAME}} - Usage Guide

## Getting Started

### Installation

```bash
npm install
```

### Development

Start the development server:

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Building

Create a production build:

```bash
npm run build
```

Preview the production build:

```bash
npm run preview
```

## Project Type

This is a **{{TYPE}}** project ({{CATEGORY}}).

## Features

{{FEATURES_LIST}}

## Configuration

Edit `src/lib/config.ts` to customize:

```typescript
export const PROJECT = {
  name: '{{PROJECT_NAME}}',
  slug: '{{SLUG}}',
  description: '{{DESCRIPTION}}',
};

export const FEATURES = {
  // Your feature settings here
};
```

## Project Structure

```
src/
├── App.tsx           # Main app component
├── main.tsx          # Entry point
├── components/       # UI components
│   ├── app/          # App-specific components
│   ├── game/         # Game components
│   ├── layout/       # Layout components
│   └── ui/           # UI primitives
├── engine/           # Game engine code
├── hooks/            # Custom React hooks
├── lib/              # Libraries & utilities
│   ├── config.ts     # Project configuration
│   ├── theme.ts      # Theme settings
│   └── utils.ts      # Utility functions
├── styles/           # Global styles
└── types/            # TypeScript types
```

## Customization

### Theme

The project supports dark/light modes. Configure in `src/lib/config.ts`:

```typescript
theme: {
  enabled: true,
  defaultMode: 'system', // 'light', 'dark', or 'system'
  modes: ['light', 'dark', 'system'],
}
```

### Game Settings

For game projects, configure:

```typescript
game: {
  enabled: true,
  type: '{{CATEGORY}}',
  canvas: { width: 800, height: 600 },
  physics: { gravity: 0.5, friction: 0.8 },
  difficulty: { lives: 3, enemySpeed: 2 },
}
```

## Deployment

### GitHub Pages

The project includes GitHub Actions workflow. Push to GitHub and your site will deploy automatically.

### Cloudflare Pages

1. Connect your GitHub repo to Cloudflare Pages
2. Set build command: `npm run build`
3. Set output directory: `dist`

## Troubleshooting

### Port Already in Use

```bash
# Kill process on port 5173
npx kill-port 5173
```

### Build Errors

```bash
# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm install
```

## License

GPL-3.0 - See LICENSE file

---

Built with [MiniDev ONE Template](https://minidev.app)
