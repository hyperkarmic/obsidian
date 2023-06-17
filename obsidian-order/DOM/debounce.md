# debounce
**ebouncing:** **Debouncing** is a programming pattern or a technique to restrict the calling of a time-consuming function frequently, by delaying the execution of the function until a specified time to avoid unnecessary CPU cycles, and API calls and improve performance. A Debounce function is a **higher-order function** that returns another function, to create closure around the function parameters (func, timeout) and the timer variable.

Debounce:_**In the debouncing technique, no matter how many times the user fires the event, the attached function will be executed only after the specified time once the user stops firing the event.**_A Debounce function is a **_higher-order function_** that returns another function, to create closure around the function parameters (func, timeout) and the timer variable.
***

![[DOM.png]]
***
Debouncing is a technique in JavaScript that is used to improve the performance of a website or web application by limiting the rate at which a particular function gets executed. This can be especially useful when working with events that are triggered frequently, such as window resizing or scrolling, as it allows us to group multiple events together and reduce the number of times that a function needs to be run. In this article, we will take a closer look at debouncing and how it can be implemented in JavaScript.
***

Debouncing is a programming technique that is used to limit the rate at which a function gets executed. It does this by grouping multiple events that occur within a certain time period into a single event, and then executing the function only once for that event.

For example, let’s say you have a function that gets called every time the user scrolls the page. Without debouncing, this function would get called multiple times as the user scrolls, which can be resource intensive and may lead to a less smooth scrolling experience.

By applying debouncing to the scroll event, we can group all of the scroll events that occur within a certain time period into a single event, and then execute the function only once for that event. This helps to reduce the number of times the function gets called and can improve the overall performance of the website or web application.
***

![[debounce.jpg]]
#debounce #DOM #js 