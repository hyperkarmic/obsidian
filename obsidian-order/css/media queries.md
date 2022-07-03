# Media Queries

## What is a media query in CSS?

Long ago, most websites had a lot of trouble rendering components on different screen sizes, especially with the mobile phone revolution. Most websites fixed that problem by creating a new website with the domain `m.`. If you’ve ever used `m.facebook.com`, this is why.

All that was before media queries. With media queries, websites can be built to fit a particular viewport, so gone are the days of zooming in on your smartphone to see what’s on the website.

Media queries provide a conditional statement around some styles, which are then implemented or not based on whether the conditions are met or not.

## The problem with media queries

While media queries changed a lot, they still had one problem: they’re not reusable. With media queries, you can create a responsive element and implement it, and even though it looks good in a standard use case, it probably won’t work as well if it’s moved to a different container with CSS properties that affect element dimensions. For it to work properly, you’ll need to add many more CSS properties.
***
![[media-queries.png]]
***

#media-query
