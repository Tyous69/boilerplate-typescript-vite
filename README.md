# Vite + React + TypeScript Boilerplate

A clean, minimal, and scalable boilerplate for web projects using **Vite**, **React**, **TypeScript**, and **SCSS Modules** — ready to clone, rename, and ship.

---

## Stack

| Tool | Purpose |
|------|---------|
| [Vite](https://vitejs.dev/) | Lightning-fast build tool & dev server |
| [React](https://react.dev/) | UI library |
| [TypeScript](https://www.typescriptlang.org/) | Type safety |
| [SCSS Modules](https://sass-lang.com/) | Scoped component styles |
| [React Router DOM](https://reactrouter.com/) | Client-side routing |

---

## Project Structure

```
Boilerplate/
├── public/
│   └── assets/
│       ├── fonts/
│       ├── icons/
│       └── images/          # Static assets served directly (referenced by URL)
│
└── src/
    ├── assets/              # Assets imported via JS/TS (optimized by Vite)
    ├── components/
    │   ├── button/          # Button component
    │   ├── layout/
    │   │   ├── header/      # App header
    │   │   └── footer/      # App footer
    │   └── ui/              # Reusable atomic components (Input, Modal, Card…)
    ├── constants/
    │   └── routes.ts        # Centralized route paths
    ├── contexts/            # React Contexts (global state without external lib)
    ├── hooks/               # Custom React hooks
    ├── pages/
    │   ├── home/
    │   └── test/
    ├── services/
    │   └── api.ts           # HTTP helpers (fetch wrapper)
    ├── styles/
    │   └── global.scss      # Global styles & CSS variables
    ├── types/
    │   └── index.ts         # Global TypeScript types & interfaces
    ├── utils/               # Pure utility functions (formatters, helpers…)
    ├── App.tsx              # Route declarations
    └── main.tsx             # Entry point
```

---

## Getting Started

### 1. Clone & Rename

```bash
git clone https://github.com/Tyous69/boilerplate-typescript-vite.git [YOUR-PROJECT-NAME]
cd [YOUR-PROJECT-NAME]
```

---

### 2. Reset Git History

Disconnect from the boilerplate repository and start a clean history.

**macOS / Linux:**
```bash
rm -rf .git
```

**Windows (PowerShell):**
```powershell
Remove-Item -Recurse -Force .git
```

---

### 3. Initialize Your New Repository

```bash
# Start a new git history
git init

# Rename branch to main (standard convention)
git branch -M main

# Connect to your new GitHub repository
git remote add origin https://github.com/[YOUR-USERNAME]/[YOUR-NEW-REPO].git

# First commit
git add .
git commit -m "init: bootstrap from boilerplate"

# Push (use --force only if the remote repo is not empty)
git push -u origin main --force
```

---

### 4. Install Dependencies

```bash
npm install
```

> ⚠️ If vulnerabilities are reported, run `npm audit fix` to resolve them automatically.

---

### 5. Start Development Server

```bash
npm run dev
```

The app will be available at `http://localhost:5173` by default.

---

### 6. Build & Preview

```bash
# Build for production
npm run build

# Preview the production build locally
npm run preview
```

---

## Environment Variables

Create a `.env` file at the root of the project:

```env
VITE_API_URL=https://your-api-url.com
```

> All Vite environment variables must be prefixed with `VITE_` to be exposed to the client.  
> Never commit `.env` files containing secrets — add them to `.gitignore`.

Access them in code:
```ts
const apiUrl = import.meta.env.VITE_API_URL;
```

---

## Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start the development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint |

---

## Conventions

### Adding a Page

1. Create a folder under `src/pages/your-page/`
2. Add `YourPage.tsx` and `YourPage.module.scss`
3. Register the route in `App.tsx`
4. Add the path constant to `src/constants/routes.ts`

### Adding a Component

Each component lives in its own folder with:
```
src/components/my-component/
├── MyComponent.tsx
└── MyComponent.module.scss
```

### Styles

- **Global styles** → `src/styles/global.scss`
- **Component styles** → SCSS Modules (`.module.scss`) co-located with the component
- **Assets imported via JS** (SVGs, images used in components) → `src/assets/`
- **Static assets** (fonts, icons, images referenced by URL) → `public/assets/`

### Types

Global or shared TypeScript types and interfaces go in `src/types/index.ts`. Component-specific types can be declared locally in the component file.

---

## License

This boilerplate is open-source and free to use for any project.