# positioning
Positioning in CSS means, to set the position of an element in the webpage.

***
## position: static;

This is the default position for all HTML elements. It is positioned with the normal flow of the webpage just like these texts. You can’t use top, bottom, left, right properties with this.
***
## position: relative;

Now, what if you want to specify directions to a particular element while being static, well, this is where relative position comes into play.
***
## position: fixed;

The name gives it away, doesn’t it? The element stays fixed at the specified place on the viewport, no matter what!

`position: fixed;` makes an element acts like an overlay. It is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled.
***
## position: absolute;

Remember, how in `position: relative;` the element resides at the specified space but holds the normal area to itself. Well, in absolute-position, just like fixed, element is removed from document normal flow which means, for other elements, it doesn’t exist in that webpage. Again, power of overlapping.

An element with absolute position is positioned relative to its closest positioned ancestor. It looks up for relative parent, if any. If not relative, then it becomes relative to  HTML tag .  
***
## position: sticky;

Literally every nav/top nav has this as position. This is a hybrid of fixed and relative/static. Let’s break it down and see what it brings to table.

So, the quirks this position element gets from static/relative is that it follows the normal flow of the webpage till it hits the specified mark, and the moment it hits that specified mark it acts like an overlay, fixed on that place.
![[css-position.jpg]]
***

***
![[css-pos.jpg]]
***
![[css-positioning.jpeg]]

#positioning #CSS 
