# Svelte + Vite + Tailwind Init



## Setup
- npm create vite@latest my-project -- --template svelte
- cd my-project

**edit package.json**

***add to devDependecies***
- "@sveltejs/vite-plugin-svelte": "^4.0.0-next.4",

 ***install***
 - npm install -D svelte@next tailwindcss postcss autoprefixer
 - npx tailwindcss init -p

***edit tailwind.config.js then add***
- content: ["./index.html", "./src/**/*.{svelte,js,ts,jsx,tsx}",]

