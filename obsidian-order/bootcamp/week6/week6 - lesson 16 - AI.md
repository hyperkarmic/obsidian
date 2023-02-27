The three markdown files describe a project to create a search engine that will utilize the New York Times API to search for and display articles. The project is split into three phases, with each phase having tasks designated for the front-end team, back-end team, and the entire team.

Learning outcomes:

-   Designing and creating layouts using Bootstrap
-   Retrieving input values using JavaScript
-   Registering and using APIs
-   Using AJAX to make calls to an API
-   Identifying and solving bugs

Code Snippets:

Phase 1:

Creating a text input box and button in HTML:

```javascript
<div class="input-group mb-3">
  <input type="text" class="form-control" placeholder="Search Term" aria-label="Search Term" aria-describedby="button-addon2" id="search-term">
  <div class="input-group-append">
    <button class="btn btn-outline-secondary" type="button" id="search-button">Search</button>
  </div>
</div>

```

Retrieving input values using JavaScript:

```javascript
var searchTerm = $("#search-term").val().trim();
```

Phase 2:

-   Creating a click event for the search button:

```javascript
$("#search-button").on("click", function(event) {
  event.preventDefault();
  var searchTerm = $("#search-term").val().trim();
  // Perform AJAX call
});

```

Making an AJAX call to the API

```javascript
var queryURL = "https://api.nytimes.com/svc/search/v2/articlesearch.json?q=" + searchTerm + "&api-key=" + apiKey;

$.ajax({
  url: queryURL,
  method: "GET"
}).then(function(response) {
  console.log(response);
});
```

Phase 3:

-   Adding visual appeal using Bootstrap and Font Awesome:

```html
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootswatch/4.3.1/flatly/bootstrap.min.css"> <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.8.1/css/all.css">
```

Handling missing fields using JavaScript:

```javascript
var article = {
  headline: "",
  author: "",
  section: "",
  date: "",
  url: ""
};

if (typeof response.response.docs[i].headline === "undefined") {
  article.headline = "";
} else {
  article.headline = response.response.docs[i].headline.main;
}

// Repeat for other fields

```