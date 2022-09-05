# Install Tailwind with NPM

> The simplest and fastest way to get up and running with Tailwind CSS from scratch is with the Tailwind CLI tool. The CLI is also available as a standalone executable if you want to use it without installing Node.js.

Install Tailwind :

```
npm install -D tailwindcss
npx tailwindcss init
```

Configure your template paths :

```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./index.html"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Create a CSS folder with a "style.css" file and add the Tailwind directives to your CSS :

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Start the Tailwind CLI build process :

```
npx tailwindcss -i ./css/style.css -o ./dist/output.css --watch
```

Put this line of code in your site's head tag :

```
<link href="/dist/output.css" rel="stylesheet">
```

Don't forget to .gitignore "node_modules/".

And start using Tailwind.