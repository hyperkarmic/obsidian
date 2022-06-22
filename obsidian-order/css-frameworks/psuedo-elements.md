# psuedo elements
### In **CSS**, `::before` and `::after` creates **pseudo-elements** that is the _prepended_ and _appended_ to the selected element respectively.
<hr>
### **Pseudo Elements** in **CSS** enable the developers to _style parts of an element_, giving them the _granular access to styling_.
<hr>
One really important thing to keep in mind while using `::before` and `::after` is to set `content` property in the **CSS**

`selector::before{  
  ``/* without content the pseudo-elements will not work */  
  `content: "";  
``}``


After adding the content, you can style them just like any other element
<hr>

## some others
# ::Selection

The `::selection` **CSS pseudo-element** styles the part of a document that is selected by a user (such as clicking and dragging the mouse across text to highlight it).

# ::Marker
The `::marker` **CSS pseudo-element** selects the marker box of a list item and generally contains a bullet or number. It works on any element or **pseudo-element** where the `display` property is set to `list-item` ( `display: list-item`), such as `<li>` elements.

# ::Placeholder

The `::placeholder` CSS **pseudo-element** can be used to target the placeholder text in an `<input>` or `<textarea>` element.

# ::Slotted()

The `::slotted()` **CSS pseudo-element** represents any element that has been placed into a `slot` inside an **HTML** template.

# ::First-Line & ::First-Letter

Just as the name suggests, the `::first-line` and `::first-letter` **CSS pseudo-elements** applies styles to the first line and the first letter respectively (of a block-level element).

***
Psuedo Element:A CSS pseudo-element is used to style specified parts of an element.
***


#before
#after
#css 
#selection
#marker
#placeholder
#slotted
#first-line
#first-letter
