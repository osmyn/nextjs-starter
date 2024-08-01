## Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

## SSH setup

1. `ssh-keygen -t ed25519 -C "your_email@example.com"`
2. `eval "$(ssh-agent -s)"`
3. `ssh-add ~/.ssh/id_ed25519`
4. Add the pub file to Github

## Project Setup

1. `npm install -g pnpm`
2. `npx create-next-app@latest nextjs-dashboard --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example" --use-pnpm`
3. `CTRL+Shift+P` > TypeScript: Select TypeScript Version > [Use Workspace Version](https://nextjs.org/docs/app/building-your-application/configuring/typescript#typescript-plugin)
4. `pnpm i` to install packages
5. `pnpm dev` to start dev server
6. Install these [4 VS Code extensions](https://dev.to/kalimahapps/4-vscode-extensions-i-use-for-tailwind-2him) and read through the [VS Code settings reccomendations](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss) (Tailwind fold optional)
7. `pnpm i use-debounce` for query string debouncing

## Project Organization

- /app: Contains all the routes, components, and logic for your application, this is where you'll be mostly working from.
- /app/lib: Contains functions used in your application, such as reusable utility functions and data fetching functions.
- /app/ui: Contains all the UI components for your application, such as cards, tables, and forms. To save time, we've pre-styled these components for you.
- /public: Contains all the static assets for your application, such as images.
- Config Files: You'll also notice config files such as next.config.js at the root of your application. Most of these files are created and pre-configured when you start a new project using create-next-app. You will not need to modify them in this course.

## My vscode settings.json

```
{
  "typescript.tsdk": "node_modules/typescript/lib",
  "tailwindCSS.includeLanguages": {
    "html": "html",
    "javascript": "javascript",
    "css": "css"
  },
  "editor.quickSuggestions": {
    "strings": "on"
  },
  "files.associations": {
    "*.css": "tailwindcss"
  }
}
```

## Vercel intergration

1. Sign into [Vercel](https://vercel.com/)
2. Connect & Deploy the project. (May have to adjust permissions to see this repo)
3. In Vercel Storage, setup a Postgres database, then copy the local.env settings back to the .env settings here
4. `pnpm i @vercel/postgres` to isnteall Vercel SDK
5. Run script in `/seed` route
