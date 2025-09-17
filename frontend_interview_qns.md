1. What is the DOM?
The DOM (Document Object Model) is a programming interface for web documents. It represents the structure of an HTML or XML document as a tree of objects, so that programming languages like JavaScript can interact with the page.

2. What is Responsive Design?

Responsive Design is an approach to web development where a website’s layout and content adapt to different screen sizes, devices, and orientations — like phones, tablets, laptops, or desktops.
The goal is to provide a seamless user experience across all devices without needing multiple versions of a site.

3. How to Implement Responsive Design
- Use a Fluid Layout: Use percentages (%), viewport units (vw, vh), or em / rem instead of fixed pixels.
- Media Queries: Change styles based on screen size
- Flexible Images & Videos: Ensure images scale properly
- Mobile-First Design: Start with styles for small screens, then scale up.
- Viewport Meta Tag
- Responsive Frameworks: Bootstrap, Tailwind CSS

4. What are Promises and how do they work?
- A Promise in JavaScript is an object that represents the eventual completion (or failure) of an asynchronous operation and its resulting value
- I promise to return you a result (or an error) once I'm done doing something that takes time.

5. What is the Use of async/await
The async/await syntax in JavaScript is used to work with asynchronous code in a cleaner and more readable way — especially when dealing with Promises

6. What Are Components in React?
Components are the building blocks of a React application. They are reusable, self-contained pieces of UI that return React elements (usually JSX) to be rendered on the screen

A React component is like a function or class that describes what a part of the UI should look like and how it behaves

7. What are hooks? Name a few commonly used ones
Hooks are special functions introduced in React 16.8 that allow you to use state, lifecycle features, and other React capabilities in functional components — without writing class components.

- useState: Adds state to a functional component
- useEffect: Runs side effects (e.g. data fetching, event listeners)
- useContext: Accesses data from a React context
- useRef: Accesses DOM nodes or store mutable values
- useMemo: Memoizes expensive computations to optimize performance
- useCallback: Memoizes a function to avoid unnecessary re-renders
- useReducer: Manages more complex state logic (like Redux-lite)
- useLayoutEffect: Like useEffect, but fires synchronously after layout



8. How Is State Managed in React?
In React, state refers to data that determines the behavior and rendering of a component. 
Managing state means controlling how that data is created, updated, and shared across your application

- Local Component State (via useState): Used for small, self-contained state within a single component.
- Shared State via Props (Parent → Child): When one component manages state and passes it down to others.
- Lifting State Up: Move shared state to the closest common ancestor so multiple components can access it.
- Global State (Across Many Components): When state needs to be accessed by many components across your app.

Options:
    React Context (for light state sharing like themes, user auth)
    State libraries for complex apps: Redux, Recoil, Zustand, Jotai, MobX

what is state in react?
State in React is data that changes over time and affects rendering. 
It’s managed through hooks like useState, shared via props or context, and sometimes handled by state management libraries in larger apps.  


9. What are props in React?
Props (short for "properties") are read-only inputs passed from a parent component to a child component in React.
They allow you to pass data and configuration into components so that they can behave or render dynamically.
Think of Props Like Function Parameters

Key Characteristics of Props
Read-only: Props cannot be changed by the child component
Passed from parent:	Only parents can pass props down to children
Dynamic: They allow components to render with custom data
Reusable: You can reuse the same component with different props

10. How do you optimize frontend performance?
- Optimizing frontend performance means making your website or web app load faster, run smoother, and consume fewer resources, especially on mobile or slow networks.

Here are the top strategies to achieve that:
1. Minimize and Compress Assets: Minify HTML, CSS, and JavaScript (remove whitespace, comments).
Use tools like: Webpack + Terser, CSSNano, UglifyJS, Compress assets (e.g. with Gzip or Brotli).

2. Optimize Images
Use modern formats like WebP or AVIF.
Compress images with tools like TinyPNG or Squoosh.
Use responsive images with srcset:
Lazy-load images with loading="lazy"

3. Use Code Splitting and Lazy Loading
Code Splitting: Break large JS bundles into smaller pieces that load on demand.
Lazy Loading: Only load components/pages when they are needed.

4. Bundle Efficiently
Remove unused code with tree shaking.
Avoid importing entire libraries (e.g. lodash) — import only needed functions.
Use tools like Webpack, Rollup, or Vite with proper configurations.

5. Minimize Repaints and Reflows
Avoid frequent changes to styles/layouts (which trigger reflow).
Use transform and opacity for animations (GPU-accelerated).
Batch DOM updates instead of doing them one at a time.

6. Leverage Browser Caching
Set proper cache headers (Cache-Control, ETag) to prevent re-downloading unchanged resources.

7. Use a CDN (Content Delivery Network)
Serve static assets (CSS, JS, images) via a CDN close to your users.
Reduces latency and improves load time.

8. Avoid Blocking Resources
Load non-essential scripts asynchronously
Use defer for scripts that can wait

9. Reduce HTTP Requests
Combine small files (or use HTTP/2 which supports multiplexing).
Use icon fonts or SVG sprites instead of many images.
Inline small critical CSS.

10. Measure and Monitor Performance
Use tools like: Lighthouse (in Chrome DevTools), WebPageTest, PageSpeed Insights, Core Web Vitals (CLS, FID, LCP)

11. Avoid inline styles: Makes CSS harder to cache and maintain
12. Remove unused CSS: Tools like PurgeCSS or Tailwind JIT
13. Use service workers: Cache static assets for offline usage
14. Use memoization: React.memo, useMemo, and useCallback for expensive operations