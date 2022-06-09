# Tailwind Elements npm and tailwind driven instance

## Done according to YT Tutorial

- See [Tailwind Elements tutorial - Tailwind CSS components library](https://www.youtube.com/watch?v=-GmnyjgI4Jc)
- And following
  - [Tailwind Elements](https://tailwind-elements.com/quick-start/)
  - [Tailwind CSS Installation: Tailwind CLI](https://tailwindcss.com/docs/installation)

## Running this instance in watch mode

```bash
git clone https://github.com/awebfactory/tw-elements-tw-css-cli-instance.git
cd tw-elements-tw-css-cli-instance
npm install
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```

Alternatively build without the `--watch` option and serve the index.html file as is.

## Sequence of commands and configurations used to create this instance

```bash
npm init
npm install -D tailwindcss
npx tailwindcss init
```

- `tailwind.config.js`

```js
module.exports = {
  content: [
    "./src/**/*.{html,js}",
    "./node_modules/tw-elements/dist/js/**/*.js",
  ],
  plugins: [require("tw-elements/dist/plugin")],
}
```

- `./src/input.css`

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

- Run `npm install tw-elements`

- `index.html`

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href="/dist/output.css" rel="stylesheet" />
  </head>
  <body>
    <h1 class="text-3xl font-bold underline">Hello world!</h1>
    <script src="/node_modules/tw-elements/dist/js/index.min.js"></script>
  </body>
</html>
```

- Execute tailwind

```bash
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```
