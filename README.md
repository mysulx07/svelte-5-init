# Svelte + Vite + Tailwind Init

## Setup
```
npm create vite@latest my-project -- --template svelte
```
```
cd my-project
```

***edit package.json add to devDependecies***
```
"@sveltejs/vite-plugin-svelte": "^4.0.0-next.4",
```
 ***install***
 ```
 npm install -D svelte@next tailwindcss postcss autoprefixer
```
```
 npx tailwindcss init -p
```

***edit tailwind.config.js then add***
```
content: [
      "./index.html",
      "./src/**/*.{svelte,js,ts,jsx,tsx}",
],
```
***edit app.css then add***
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```
***run development server***
```
npm run dev
```
#svelte main.js
```
import { mount } from "svelte";
import "./app.css";
import App from "./App.svelte";

const app = mount(App, { target: document.getElementById("app") });

export default app;
```

#vite setting
```
plugins: [svelte()],
  server: {
    port: 3001,
    proxy: {
      "/api": {
        target: "http://localhost/ampu",
        changeOrigin: true,
      },
    },
  },
  base: "/ampu",
```
