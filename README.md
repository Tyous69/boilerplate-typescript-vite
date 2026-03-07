# Vite + TypeScript Boilerplate

A minimal boilerplate for web projects using **Vite**, **React**, **TypeScript**, and **SCSS Modules**.

## Stack

- [Vite](https://vitejs.dev/)
- [React](https://react.dev/)
- [TypeScript](https://www.typescriptlang.org/)
- [SCSS Modules](https://sass-lang.com/)
- [React Router DOM](https://reactrouter.com/)

## Project Structure
```
src/
├── components/
│   ├── button/
│   ├── layout/
│   │   ├── header/
│   │   └── footer/
│   └── ui/          # Reusable atomic components (Modal, Input, Card...)
├── pages/
│   └── home/
├── styles/
│   └── global.scss
├── App.tsx          # Routes
└── main.tsx         # Entry point
```

## Getting Started

### 1. Clone & Rename
Clone the boilerplate and give it your new project name:
```bash
git clone https://github.com/Tyous69/boilerplate-typescript-vite.git [YOUR-PROJECT-NAME]
cd [YOUR-PROJECT-NAME]

```

### 2. Reset Git History

To start a fresh history and disconnect from the boilerplate:

**On macOS / Linux:**

```bash
rm -rf .git

```

**On Windows (PowerShell):**

```powershell
Remove-Item -Recurse -Force .git

```

### 3. Initialize your New Repository

```bash
# 1. Start a new git
git init

# 2. Rename branch to main (Standard)
git branch -M main

# 3. Connect to your NEW GitHub repo
git remote add origin [https://github.com/](https://github.com/)[YOUR-USERNAME]/[YOUR-NEW-REPO].git

# 4. First Push
git add .
git commit -m "init: bootstrap from boilerplate"

# Note: Use --force only for the very first push if your repo on GitHub is not empty
git push -u origin main --force

```

### 4. Install & Run

```bash
# Install dependencies
npm install

# Start development server
npm run dev

```

### 5. Build & Preview

```bash
# Build for production
npm run build

# Preview production build locally
npm run preview

```

## Notes

- Add new pages in `src/pages/` and register their routes in `App.tsx`.
- Global styles go in `src/styles/global.scss`.
- Component-level styles use SCSS Modules (`.module.scss`).