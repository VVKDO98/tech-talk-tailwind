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

## Configure tailwind.config.js

```
module.exports = {
  content: ['./src/**/*.{html,js}'],      // File you want to add to the project
  theme: {                                // Theme modification
    colors: {                             // Adding custom colours
      'blue': '#1fb6ff',
      'purple': '#7e5bef',
      'pink': '#ff49db',
      'orange': '#ff7849',
      'green': '#13ce66',
      'yellow': '#ffc82c',
      'gray-dark': '#273444',
      'gray': '#8492a6',
      'gray-light': '#d3dce6',
    },
    fontFamily: {                         // Custom fonts
      sans: ['Graphik', 'sans-serif'],
      serif: ['Merriweather', 'serif'],
    },
    extend: {                             // Custom values
      spacing: {
        '8xl': '96rem',
        '9xl': '128rem',
      },
      borderRadius: {
        '4xl': '2rem',
      }
    }
  },
}
```

```
module.exports = {
  // ...
  plugins: [
    require('@tailwindcss/forms'),                // A plugin that provides a basic reset for form styles that makes form elements easy to override with utilities.
    require('@tailwindcss/typography'),           // The official Tailwind CSS Typography plugin provides a set of prose classes you can use to add beautiful typographic defaults to any vanilla HTML you don’t control, like HTML rendered from Markdown, or pulled from a CMS.
    require('@tailwindcss/line-clamp'),           // A plugin that provides utilities for visually truncating text after a fixed number of lines.
  ],
}
```

## Links

[Setup documentation](https://tailwindcss.com/docs/configuration)

[Plugins documentation](https://tailwindcss.com/docs/plugins)