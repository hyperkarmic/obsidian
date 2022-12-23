# web storage
**WebStorage:** With web storage, web applications can store data locally within the user's browser.

Before HTML5, application data had to be stored in cookies, included in every server request. Web storage is more secure, and large amounts of data can be stored locally, without affecting website performance.

Unlike cookies, the storage limit is far larger (at least 5MB) and information is never transferred to the server.

Web storage is per origin (per domain and protocol). All pages, from one origin, can store and access the same data.

The Web Storage API provides mechanisms by which browsers can securely store key/value pairs.
***
WebStorage API, also known as **HTML5 storage**, is a form of persistent storage that stores data on the client's computer. It consists of the following:

-   LocalStorage
-   SessionStorage

### What Are LocalStorage and SessionStorage?

LocalStorage is one of the most used browser storage options. We store all our data on our computer permanently in localStorage. It saves our data to the point where we can still access it after we close and reopen our browser.

The data saved in localStorage does not expire until we delete it manually. To erase data from localStorage, use **JavaScript** or clear the **browser cache**.

[SessionStorage](https://www.javascripttutorial.net/web-apis/javascript-sessionstorage/) is like localStorage but with a few differences. It only keeps data for a particular session. We store all our data on our computer temporarily in sessionStorage. When the session expires, i.e., when we close that browser or tab, our data is erased.

Each time we open two tabs with the same URL, the web browser creates its sessionStorage. A different window tab cannot access another sessionStorage data. For example, we can conduct separate transactions on an e-commerce site even if we open two browser tabs.

LocalStorage and sessionStorage store data as a **key-value** pair, but it must be either a number or a string.

**Note:** To store other data types like arrays or objects, we use `JSON.stringify()` to convert them into strings.
***

#webstorage
#API 