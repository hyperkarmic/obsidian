# Web Workers - Definitition
Web worker: background thread for performing computationally intensive tasks without freezing the user interface
***

**Web Worker** = When executing scripts in an HTML page, the page becomes unresponsive until the script is finished.
***

A web worker is a JavaScript that runs in the background, independently of other scripts, without affecting the performance of the page. You can continue to do whatever you want: clicking, selecting things, etc., while the web worker runs in the background.
***
Have you ever used a computer program that seems to **freeze or become unresponsive** when it’s doing a lot of work? That’s because the program is busy with a lot of tasks, and it can’t respond to user input until it’s finished.

Web workers are a way for web developers to prevent this problem from happening in web applications. Essentially, a web worker is a separate **“thread”** of code that runs in the **background, independently** of the main thread that controls the **user interface.**

By running code in a web worker, web developers can prevent the main thread from becoming unresponsive, even if the web app is doing a lot of work. This means that the user can continue to interact with the app even while it’s doing complex operations in the background.

To put it simply, **web workers are like helpers that work behind the scenes to keep your web app running smoothly and prevent it from freezing up.**
***

#webworker #web-worker #definition 