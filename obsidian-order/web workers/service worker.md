# service worker

### Service workers

This is one of the key technologies behind PWAs. They help support your app to work offline, and they perform advanced caching and run background tasks. Service workers can complete tasks even when your PWA is not running.  
Some other functions associated with service workers include:

-   Sending push notification
-   Badging icons
-   Running background fetch tasks etc.

Before the service worker takes control of your page, it must be registered for your PWA. That means the first time a user comes to your PWA, network requests will go directly to your server because the service worker is not yet in control of your pages.

After checking if the browser supports the Service Worker API, your PWA can register a service worker. When loaded, the service worker sets up as a shop between your PWA and the network, intercepting requests and serving the corresponding responses.
***
_Some key things to understand are:_

-   Service workers are only available over `HTTPS` or `localhost`.
-   If a service worker's contents contain syntax errors, registration fails and the service worker is discarded.
-   Service workers operate within a scope. Here, the scope is the entire origin, as it was loaded from the root directory.
-   When registration begins, the service worker state is set to `installing`.
***
Once registration finishes, installation begins.

#### [](https://dev.to/this-is-learning/what-are-progressive-web-applications-get-started-with-creating-pwa-184b#installation)Installation

A service worker fires its `install` event after registration. `install` is only called once per service worker, and won't fire again until it's updated. A callback for the install event can be registered in the worker's scope with `addEventListener`.
***
When a file needs to be loaded, the above code checks if the file is in the service worker cache. If it is available, then the file is served from the cache. If not, it would fetch the file from the network, store the response in the cache, and return the network response.

If the user is offline or facing any network issues, then the file `offline.html` would be loaded as a fallback to the user. This file could either have a static template to inform the user that they are offline or it could have some dynamic content such as the dinosaur game on google.

There are various caching strategies available while making this `fetch` event call. They are:

-   **Stale While Revalidate** uses a cached response for a request if it's available and updates the cache in the background with a response from the network. Therefore, if the asset isn't cached, it will wait for the network response and use that. It's a fairly safe strategy, as it regularly updates cache entries that rely on it. The downside is that it always requests an asset from the network in the background.
-   **Network First** tries to get a response from the network first. If a response is received, it passes that response to the browser and saves it to a cache. If the network request fails, the last cached response will be used, enabling offline access to the asset.
-   **Cache First** checks the cache for a response first and uses it if available. If the request isn't in the cache, the network is used and any valid response is added to the cache before being passed to the browser.
-   **Network Only** forces the response to come from the network.
-   **Cache Only** forces the response to come from the cache.

[Click here](https://developer.chrome.com/docs/workbox/caching-strategies-overview/) to learn more about them.

Apart from the 2 events that we discussed so far, service workers have another event called `activate`.

#### [](https://dev.to/this-is-learning/what-are-progressive-web-applications-get-started-with-creating-pwa-184b#activating)Activating

If registration and installation succeed, the service worker activates, and its state becomes 'activating'. When an updated service worker is installed and the waiting phase ends, it activates, and the old service worker is discarded. A common task to perform in an updated service worker's `activate` event is to prune old caches. Remove old caches by getting the keys for all open Cache instances with `caches.keys` and deleting caches that aren't in a defined allow list with `caches.delete`
#PWA #service-worker
