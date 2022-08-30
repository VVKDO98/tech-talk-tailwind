# Tech Talk Tailwind

Tailwind is a CSS framework, it works by parsing all your HTML files, JavaScript components and any other templates for class names, generating the corresponding styles, then writing them to a static CSS file.

## How to install Tailwind ?

There are two ways to install it.

### Using CDN

> Use the Play CDN to try Tailwind right in the browser without any build step. The Play CDN is designed for development purposes only, and is not the best choice for production. 

Put this line of code in your site's head tag :

```
<script src="https://cdn.tailwindcss.com"></script>
```

And start using Tailwind.

### Using NPM

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
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Add the Tailwind directives to your CSS :

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Start the Tailwind CLI build process :

```
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```

Put this line of code in your site's head tag :

```
<link href="/dist/output.css" rel="stylesheet">
```

And start using Tailwind.

The whole process can be found in the  [Tailwind documentation.](https://tailwindcss.com/docs/installation/play-cdn)

### Configure config.tailwind.js file

---------------------------To do---------------------------

## Project created with Tailwind

[Personnal portfolio](https://vvkdo98.github.io/portfolio/)

[Repository](https://github.com/VVKDO98/portfolio)

## ✅ Why should you use Tailwind ?

- Customization
    - Basic configuration with config.tailwind.js
    - Colours
    - Sizes
    - Fonts
    - ...
- Speed of development
    - No need to switch between files
- Mobile first
    - Responsive and easy to implement
    - No need for mixins or media querries
- Integrated design system
    - Thanks to the config file you can configure most of the values before the project
- Weight
    - Once in production, the file weight is generally low
- Good documentation for learning

## ⛔ Why shouldn't you use Tailwind ?

- The HTML document can look disorganised for large projects
- Not easy to get to grips with at first, as you need to know the tailwind syntax
- Not easy to use if you don't know basic CSS
- Difficult to maintain over time