## 1.
Option 1, we want to do this because it will automatically test without relying on the developer testing it themselves and will catch failures before they get merged into the build.

## 2.
No

## 3.
Navigation mode loads the page fresh from scratch and measures performance during the entire page load process. It captures JS execution, network requests, and rendering to give you an overall performance score.
Snapshot mode analyzes the page exactly as it currently exists in the browser's DOM at that moment. Its best for catching issues that may exist in a specific UI state like accessibility issues.


## 4.

Add a <meta name="description"> tag. The index.html has no meta description, which hurts the SEO score. Lighthouse flags this directly.

Add alt attributes to images / aria-label to icon elements — the nav bar uses <span class="icon"> elements with no accessible text, which Lighthouse flags as accessibility issues.

Reduce render-blocking resources — the page loads product-item.js, storage.js, and main.js in the <head>. Moving scripts to the bottom of <body> or adding defer to non-module scripts can improve First Contentful Paint.


