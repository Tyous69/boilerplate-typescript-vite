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

### Get rid of the boilerplate link
```bash
rm -rf .git
```

### Initialize new git project
```
bash
git init
git remote add origin https://github.com/[YOUR-USERNAME]/[NEW-PROJECT-NAME].git
```

### First commit
```
bash
git add .
git commit -m "init: from boilerplate"
git push -u origin main
```

### Install dependencies
```bash
npm install
```

### Start the dev server
```bash
npm run dev
```

### Build for production
```bash
npm run build
```

### Preview the production build
```bash
npm run preview
```

## Notes

- Add new pages in `src/pages/` and register their routes in `App.tsx`.
- Global styles go in `src/styles/global.scss`.
- Component-level styles use SCSS Modules (`.module.scss`).