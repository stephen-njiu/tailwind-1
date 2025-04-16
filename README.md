# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript and enable type-aware lint rules. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.

## Tailwind v4 + React
1. create a react app using vite
'npm create vite@latest my_app -- --template react'

2. cd 'my_app'
3. npm install
4. npm install tailwindcss @tailwindcss/vite
5. include this in your config file

``` javascript 
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'  // plugin for react
import tailwindcss from '@tailwindcss/vite' // plugin for v4 tailwind
export default defineConfig({
  plugins: [
    react(),
    tailwindcss(), // include tailwindcss here
  ],
})
// The config works perfect with ts too.

```

6. At the first line of index.css import tailwind
``` css
@import "tailwindcss";

```

7. Run you application using<br>
 `npm run dev`