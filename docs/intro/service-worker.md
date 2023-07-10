---
title: Service Worker 🤖
sidebar_label: Service Worker 🤖
slug: /service-worker
---

<head>
  <title>Service Worker 🤖</title>
</head>

## Summary  📄 

Service workers are JavaScript files that run in the background of a web page, separate from the main browser thread. They enable advanced features like caching, push notifications, and background synchronization. In Next.js, you can implement service workers to cache assets, improve offline support, and enhance the performance of your web application.

## Example code 🖥️

To use a service worker in, follow these steps:

1. Create a new JavaScript file called `service-worker.js` in the root of your Next.js project.
2. Inside `service-worker.js`, write the code to define the caching strategy and handle service worker events. Here's a basic example that caches and serves static assets:

```javascript
const CACHE_NAME = 'my-cache';
const urlsToCache = [
  '/',
  '/about',
  '/contact',
  // Add other URLs and assets you want to cache
];

self.addEventListener('install', (event) => {
  event.waitUntil(
    caches.open(CACHE_NAME).then((cache) => {
      return cache.addAll(urlsToCache);
    })
  );
});

self.addEventListener('fetch', (event) => {
  event.respondWith(
    caches.match(event.request).then((response) => {
      return response || fetch(event.request);
    })
  );
});
```

3. Import and register the service worker in your Next.js app. Open the `_app.js` file and add the following code:

```javascript
if ('serviceWorker' in navigator) {
  window.addEventListener('load', () => {
    navigator.serviceWorker
      .register('/service-worker.js')
      .then((registration) => {
        console.log('Service Worker registered:', registration);
      })
      .catch((error) => {
        console.log('Service Worker registration failed:', error);
      });
  });
}
```

With this setup, your application will have a service worker that caches the specified URLs and assets. It will serve the cached content when available, improving the offline experience and reducing network requests.

Remember to customize the caching strategy, add more routes and assets to cache, and handle other service worker events as needed.

**Note:** Make sure to test the service worker thoroughly in different scenarios to ensure it behaves as expected and meets your application's requirements.
