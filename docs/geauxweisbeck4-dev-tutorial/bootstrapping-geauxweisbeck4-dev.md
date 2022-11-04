---
sidebar_position: 3
---

# Bootstrapping GeauxWeisbeck4.dev

In the introduction, we talked a little bit about the project and got started on setting up some of the basic things, like cloning the GitHub Repository. That is great for those of you who want to just use the project and get rolling. This section will help you set everything up from scratch - I'll even show you how to set up the whole GitHub Repository for productivity so you can code at your best.

## Setting Up NextJS and Storyblok CMS

I am only including how to set up the project on this page, so you can find the full tutorial over at the NextJS and Storyblok CMS integration pages.



## [Setting up Dev Server with HTTPS Proxy on macOS](https://www.storyblok.com/faq/setup-dev-server-https-proxy)

I used a HTTPS Proxy to connect to the Storyblok CMS. Yes, you will want to set up an HTTPS server if you are using Storyblok. I will show other applications for this in the future hopefully.

Start out by installing mkcert onto your terminal. mkcert creates a valid certificate and installs localhost with mkcert.

```
// Install mkcert

brew install mkcert
mkcert -install
mkcert localhost
```

Install the HTTPS proxy and run the proxy with these commands.

```
npm install -g local-ssl-proxy // Installing the proxy
local-ssl-proxy --source 3010 --target 3000 --cert localhost.pem --key localhost-key.pem  // Running the proxy to target port 3000, you can change that any port of your choice but it should be what your app is running on in development.
```

After this runs, it will show that our devellopment project is on https://localhost:3000.

## Adding TailwindCSS to Project

You can find the official instructions for adding your website to TailwindCSS [here](https://tailwindcss.com/docs/guides)

Here is how I added TailwindCSS:

```
$ cd geauxweisbeck4-dev
$ npm install -D tailwindcss postcss autoprefixer
$ npm tailwindcss init -p
```

Configure your template paths in the `tailwind.config.js` file:

```tailwind.config.js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./pages/**/*.{js,ts,jsx,tsx}",
    "./components/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Add the Tailwind directives to your CSS:

```globals.css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Start the build process by running `npm run dev` - now you can start adding Tailwind to your project!

You can view more on how to edit pages with Tailwind CSS in that section, and you can also view the styling documentation for this website here. I will have a Tailwind CSS class coming out soon, so stay tuned!


