
CSS Grid is a layout mode in CSS that allows you to easily create complex grid-based layouts. It’s particularly useful for building responsive layouts that can adapt to different screen sizes and devices.

Here’s an example of how you might use CSS Grid to create a simple two-column layout:

```html
<div style="display: grid; grid-template-columns: 1fr 1fr;"> <div style="background-color: lightblue;">Column 1</div> <div style="background-color: lightgreen;">Column 2</div> </div>
```


In this example, the outer **div** element is the grid container, and the two inner **div** elements are the grid items. The **display: grid** style tells the browser to treat the outer **div** as a grid container, and the **grid-template-columns: 1fr 1fr** style tells the browser to create a grid with two equal-width columns.

You can also use the **grid-template-rows** property to specify the number and size of rows in the grid, and the **grid-template-areas** property to define the areas within the grid. For example, you can use the following styles to create a grid with three rows and two columns.

```css
grid-template-columns: 1fr 1fr; grid-template-rows: 100px 200px 300px; grid-template-areas: "header header" "sidebar main" "footer footer";
```

You can then use the **grid-area** property to assign grid items to specific areas within the grid. For example:

```html
<div style="display: grid; grid-template-columns: 1fr 1fr; grid-template-rows: 100px 200px 300px; grid-template-areas: 'header header' 'sidebar main' 'footer footer';"> <div style="grid-area: header; background-color: lightblue;">Header</div> <div style="grid-area: sidebar; background-color: lightgreen;">Sidebar</div> <div style="grid-area: main; background-color: lightyellow;">Main content</div> <div style="grid-area: footer; background-color: lightpink;">Footer</div> </div>
```

#grid #responsive-design 