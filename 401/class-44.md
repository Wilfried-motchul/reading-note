# React 4

# Pre-rendering and Data Fetching


# Download Starter Code (Optional)
If you’re NOT continuing from the previous lesson, you can download, install, and run the starter code for this lesson below. This sets up a `nextjs-blog` directory such that it’s identical to the result of the previous lesson.

Again, this is NOT necessary if you’ve just finished the previous lesson.

```
npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn-starter/tree/master/data-fetching-starter"
```

Then follow the instructions from the command output (cd into the directory and start the development server).

You should also update the following files:

* `public/images/profile.jpg` with your photo (Recommended: 400px width/height).
* `const name = '[Your Name]'` in `components/layout.js` with your name.

* `<p>[Your Self Introduction]</p>` in `pages/index.js` with your self introduction.

# Pre-rendering
Before we talk about data fetching, let’s talk about one of the most important concepts in Next.js: Pre-rendering.

By default, Next.js pre-renders every page. This means that Next.js generates HTML for each page in advance, instead of having it all done by client-side JavaScript. Pre-rendering can result in better performance and SEO.

Each generated HTML is associated with minimal JavaScript code necessary for that page. When a page is loaded by the browser, its JavaScript code runs and makes the page fully interactive. (This process is called hydration.)

# Check That Pre-rendering Is Happening
You can check that pre-rendering is happening by taking the following steps:

* Disable JavaScript in your browser (here’s how in Chrome) and…
* Try accessing this page (the final result of this tutorial).

You should see that your app is rendered without JavaScript. That’s because Next.js has pre-rendered the app into static HTML, allowing you to see the app UI without running JavaScript.

> Note: You can also try the above steps on localhost, but CSS won’t be loaded if you disable JavaScript.

If your app is a plain React.js app (without Next.js), there’s no pre-rendering, so you won’t be able to see the app if you disable JavaScript. For example:

* Enable JavaScript in your browser and check out this page. This is a plain React.js app built with Create React App.
* Now, disable JavaScript and access the same page again.
* You won’t see the app anymore — instead, it’ll say “You need to enable JavaScript to run this app.” This is because the app is not pre-rendered into static HTML.