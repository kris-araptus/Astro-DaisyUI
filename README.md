Astro + DaisyUI Starter Kit

sh

npm create astro@latest -- --template minimal

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/withastro/astro/tree/latest/examples/minimal)
[![Open with CodeSandbox](https://assets.codesandbox.io/github/button-edit-lime.svg)](https://codesandbox.io/p/sandbox/github/withastro/astro/tree/latest/examples/minimal)
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/withastro/astro?devcontainer_path=.devcontainer/minimal/devcontainer.json)

>  🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

🚀 Project Structure

Inside of your Astro + DaisyUI project, you'll see the following folders and files:

```text

/
├── README.md
├── astro.config.mjs
├── package-lock.json
├── package.json
├── postcss.config.js
├── public/
│   └── favicon.svg
├── src/
│   ├── env.d.ts
│   ├── pages/
│   │   └── index.astro
│   └── styles/
│       └── global.css
├── tailwind.config.js
└── tsconfig.json
```
Astro 
    Minimal Setup: Clean and simple structure to get started quickly.
    Tailwind CSS: A utility-first CSS framework packed with classes.
    DaisyUI: Tailwind CSS components for rapid UI development.

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).

🛠️ Setup Instructions

    Install Tailwind CSS and DaisyUI:

    sh

npm install -D tailwindcss postcss autoprefixer daisyui

Initialize Tailwind CSS:

sh

npx tailwindcss init -p

Configure Tailwind CSS:
Update your tailwind.config.js file to include DaisyUI:

javascript

/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    './src/**/*.{astro,html,js,jsx,ts,tsx,vue,svelte}',
  ],
  theme: {
    extend: {},
  },
  plugins: [require('daisyui')],
};

Create a global CSS file (src/styles/global.css):

css

@tailwind base;
@tailwind components;
@tailwind utilities;

/* DaisyUI components */
@import 'daisyui';

Import the global CSS file in your project (e.g., src/pages/index.astro):

jsx

    ---
    import "../styles/global.css";
    ---

    <html lang="en">
      <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Astro with DaisyUI</title>
      </head>
      <body>
        <div class="container mx-auto p-4">
          <h1 class="text-4xl font-bold mb-4">Welcome to Astro with DaisyUI</h1>

          <div class="card w-96 bg-base-100 shadow-xl mb-4">
            <div class="card-body">
              <h2 class="card-title">Card Title</h2>
              <p>If a dog chews shoes whose shoes does he choose?</p>
              <div class="card-actions justify-end">
                <button class="btn btn-primary">Buy Now</button>
              </div>
            </div>
          </div>

          <div class="alert alert-info mb-4">
            <div>
              <span>Info Alert</span>
            </div>
          </div>

          <button class="btn btn-primary mb-4">Primary Button</button>

          <input type="text" placeholder="Type here" class="input input-bordered input-primary w-full max-w-xs mb-4" />

          <label for="my-modal" class="btn modal-button mb-4">Open Modal</label>
          <input type="checkbox" id="my-modal" class="modal-toggle" />
          <div class="modal">
            <div class="modal-box">
              <h3 class="font-bold text-lg">Congratulations!</h3>
              <p class="py-4">You've been selected for a chance to get one year of subscription for free!</p>
              <div class="modal-action">
                <label for="my-modal" class="btn">Yay!</label>
              </div>
            </div>
          </div>
        </div>
      </body>
    </html>

🛡️ License

This project is licensed under the MIT License.