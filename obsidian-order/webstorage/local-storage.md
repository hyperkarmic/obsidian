local storage allows you to store data in the browser that persists even after the browser is closed. This means that the data stored in local storage will still be available the next time the user visits the website.
***
Both local storage and session storage are useful for storing data that you want to access and use on multiple pages of a website, without having to send a request to the server to retrieve it each time. They can be used to store small amounts of data, such as user preferences or form field values, and can improve the performance and user experience of a website by reducing the number of requests made to the server.

local storage and session storage are properties of the Window object in JavaScript, which means they are part of the web API. They are not objects that you need to create or declare yourself.
***

To use local storage or session storage in your JavaScript code, you simply access the localStorage or sessionStorage property of the Window object and call the appropriate methods and properties.
***
-   Scope: Local storage is available to all pages from the same origin (i.e., domain), while session storage is only available to the pages of the current browsing session.
-   Lifetime: As mentioned, data stored in local storage persists even after the browser is closed, while data stored in session storage is deleted when the browser is closed.
-   Size: The amount of data that can be stored in local storage and session storage is limited by the browser, but local storage typically has a larger capacity than session storage.

***
Both local storage and session storage also have a length property that you can use to get the number of items stored in the storage, and a key() method that you can use to get the name of a specific item based on its index.
***
Local storage is a useful tool for storing data in the browser that needs to persist even after the browser is closed. Here are a few examples of use cases for local storage:

-   Storing user preferences or settings: Local storage can be used to store user preferences or settings for a website, such as the preferred language or theme, so that they are available the next time the user visits the website.
-   Storing form field values: Local storage can be used to store the values of form fields, so that they are not lost if the user navigates away from the page or closes the browser. This can be particularly useful for forms with a large number of fields, or forms that take a long time to fill out.
-   Storing authentication tokens: Local storage can be used to store authentication tokens or other data that is needed to maintain a logged-in state for a user across multiple sessions.
-   Storing data for offline access: Local storage can be used to store data that is needed for a web application to function offline, such as cached resources or data that has been previously downloaded from the server.
-   Improving performance: Local storage can be used to store data that is used frequently on a website, so that it can be accessed without sending a request to the server each time. This can improve the performance of the website by reducing the number of requests that need to be made.
-   Storing game state: Local storage can be used to store the state of a game, such as the current level or score, so that it is available the next time the user plays the game.
-   Storing shopping cart data: Local storage can be used to store data about the items in a shopping cart, so that the cart is not emptied if the user leaves the website or closes the browser.
-   Storing recently viewed items: Local storage can be used to store data about recently viewed items on a website, so that they can be displayed to the user the next time they visit the website.
-   Storing data for A/B testing: Local storage can be used to store data about which version of a page or feature a user has seen, so that the same version can be displayed to them on subsequent visits to the website.
-   Storing data for analytics: Local storage can be used to store data about the user’s interactions with a website, such as the pages they have visited or the actions they have taken, so that it can be analyzed and used to improve the website.

As you can see, local storage is a versatile tool that can be used in a variety of situations where it is necessary to store data in the browser and make it available on subsequent visits to the website.
***
![[local-storage.jpg]]
***
![[local-storage_.jpg]]
***
![[local-storage-how.jpg]]

***
![[local-storage2.jpg]]
***
![[local-storage3.jpg]]
***
![[local-storage4.jpg]]
#local-storage
#webstorage 