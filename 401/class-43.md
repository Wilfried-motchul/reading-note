# React 3

## Next.js: The React Framework

Enter `Next.js`, the React Framework. Next.js provides a solution to all of the above problems. But more importantly, it puts you and your team in the pit of success when building React applications.

Next.js has the best-in-class "Developer Experience" and many built-in features; a sample of them are:

* An intuitive page-based routing system (with support for dynamic routes)
* Pre-rendering, both static generation (SSG) and server-side rendering (SSR) are supported on a per-page basis
* Automatic code splitting for faster page loads
* Client-side routing with optimized prefetching
* Built-in CSS and Sass support, and support for any CSS-in-JS library
* Development environment with Fast Refresh support
* API routes to build API endpoints with Serverless Functions
* Fully extendable

Next.js is used in tens of thousands of production-facing websites and web applications, including many of the world's largest brands.

## Create a Next.js app

To create a Next.js app, open your terminal, cd into the directory you’d like to create the app in, and run the following command:
```
npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn-starter/tree/master/learn-starter"
```

Under the hood, this uses the tool called `create-next-app`, which bootstraps a Next.js app for you. It uses this template through the `--example` flag.

If it doesn’t work, please take a look at this page.

## Run the development server

You now have a new directory called `nextjs-blog`. Let’s `cd` into it:

```
cd nextjs-blog
```

Then, run the following command:

```
npm run dev
```

This starts your Next.js app’s "development server" (more on this later) on port 3000.

Let’s check to see if it’s working. Open http://localhost:3000 from your browser.

