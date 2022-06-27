# simple pwa
## Get Started with PWA Development

The first characteristic of a progressive web app is that it must work on all devices and must enhance on devices and browsers that allow it. Therefore, you could develop a web app using traditional HTML5 and JavaScript that simulates the retrieval of data from a server API. Alternatively, SPA (Single Page Applications) could be created using Angular, React, Vue, etc.

Now, to convert this simple web application into a PWA, we would need to include the following files.

1.  Manifest
2.  Service Worker

I have created a simple weather app in React and converted it into a PWA by adding the above-mentioned files. You can view the code on this [repository](https://github.com/supminn/weather_app_PWA).

### [](https://dev.to/this-is-learning/what-are-progressive-web-applications-get-started-with-creating-pwa-184b#manifest-file)Manifest file

Each PWA should include a single manifest per application, typically hosted in the root folder, and linked on all HTML pages the PWA can be installed from. Its official extension is `.webmanifest`, so you could name your manifest something like `app.webmanifest`. While the recommended extension is `.webmanifest`, any filename will work as long as it's delivered with the `application/manifest+json` content type or another JSON-valid content type, such as `text/json`. As such, many PWAs, particularly older ones, use `manifest.json` instead.

This file contains information about how the PWA should appear and function. It allows us to determine the name, description, icon, colors, and other features of the PWA. With this manifest file, it is possible to run the web app in full-screen mode as a standalone application.

Here's an example of a manifest file:

```
{
"short_name": "MyPWA",
"name": "My Progressive Web App",
"description": "Creating a PWA that is compatible with all the devices",
"theme_color": "#eb5252",
"background_color": "#e840cf",
"display": "fullscreen",
"start_url": "index.html",
"scope": "/",
"orientation": "portrait",
"icons": [
    {
        "src": "images/AppIcon-48-48.png",
        "type": "image/png",
        "sizes": "48x48"
    },
    {
        "src": "images/AppIcon-96-96.png",
        "type": "image/png",
        "sizes": "96x96"
    },
    {
        "src": "images/AppIcon-192-192.png",
        "type": "image/png",
        "sizes": "192x192"
    }
   ],
  }
`````` javascript

```

Let’s break down and understand what each field depicts within the manifest file:

-   `short_name` is a human-readable name for the application. In Chrome for Android, this is the name accompanying the icon on the home screen.
-   `name` is also a human-readable name for the application and defines how the application will be listed.
-   `description` provides a general description of the web application.
-   `theme_color` is the default theme color for the application. On Android, this is also used to color the status bar.
-   `background_color` defines the background color of the web application. In Chrome, it also defines the background color of the splash screen.
-   `start_url` is the starting URL of the application.
-   `scope` changes the navigation scope of the PWA, allowing you to define what is and isn't displayed within the installed app's window. For example, if you link to a page outside of the scope, it will be rendered in an in-app browser instead of within your PWA window.
-   `display` defines the default display mode describing how the OS should draw the PWA window. They can take either `fullscreen`, `standalone`, `minimal-ui` or `browser` as value.
-   `orientation` defines the default orientation for the web application: portrait or landscape.
-   `icons` define an array of icon objects with `src`, `type`, `sizes`, and optional `purpose` fields, describing what images should represent the PWA. In Chrome for Android, the icon will be used on the splash screen, on the home screen, and in the task switcher.

**Linking your manifest**  
To make the browser aware of your web app manifest, you need to link it to your PWA using `<link>` HTML element and the `rel` attribute set to `manifest` on all of your PWA's HTML pages. This is similar to how you link a CSS stylesheet to a document
<html lang="en">
  <title>This is my first PWA</title>
  <link rel="manifest" href="/app.webmanifest" />
</html>

```
<html lang="en">
  <title>This is my first PWA</title>
  <link rel="manifest" href="/app.webmanifest" />
</html>
```

_Note:_ If your PWA includes multiple HTML pages, make sure to link its manifest to all of them.

Once the manifest file is linked to the document, you should be able to verify it on the 'Application' tab of the dev tools.

 #simple-pwa
 #PWA 
