all right then gang so we have a single component so far in our application this one right here app.js this is known as the root component of the application meaning it's the first component that gets rendered to the dom and it sits at the very top of our application it's the thing that this index file renders right here now in react applications our components are structured in a way that makes up a component tree now the root component sits at the top of this tree and this is the component that is initially rendered inside our html file

[00:39](https://www.youtube.com/watch?v=undefined&t=39s)

in our case that component is called app.js then if we were to make more components we nest them inside this root one so if we made components for a navbar some block details sidebar etc all of those components would be nested inside this root app component and then if we make further components they could be nested inside these ones as well so this makes up our component tree and we're going to start by just making a navbar component which is going to sit inside our root app component at the top all right then so to make a new

[01:15](https://www.youtube.com/watch?v=undefined&t=75s)

component the first thing we need is a new file which i'm going to make inside the source folder and this will be called navbar.js now remember a component is just a function which returns a jsx template and then that function is exported at the bottom of the file now remember that package i told you to install to vs code which was called simple react snippets this thing over here well i'm going to use a snippet to create a functional component right here so this is sfc and then tab and it creates what's known as a

[01:48](https://www.youtube.com/watch?v=undefined&t=108s)

stateless functional component so all i need to do now is give this a name which i'm going to call navbar with a capital n and then we have our boilerplate component now notice this time that this is an arrow function unlike this one now it doesn't matter like i said it can be an arrow function if you prefer and i generally create arrow functions for my components but either way it doesn't matter so inside here we now need to return some kind of templates the first thing i'm going to do is a nav

[02:18](https://www.youtube.com/watch?v=undefined&t=138s)

with a class of navbar and then inside that i'm going to do an h1 and that h1 is going to say the dojo blog and below the h1 i will do another div with a class of links and these are going to be the links in our navigation so let's do an anchor tag for the first one that's going to go to just forward slash which will ultimately be the home page and we'll say home for the text i'm going to duplicate this and i'm going to change the href right here to forward slash create and this is going to be to later create

[02:51](https://www.youtube.com/watch?v=undefined&t=171s)

a new blog so we'll just type here new blog now at the minute this is not going to work because we've not set up multiple pages or anything like that yet but when we come to work with routing later on in the course this will work then okay but for now we just want some content to output to the browser so that's pretty much it that's our template for the navbar and we're exporting this function at the bottom so now what we need to do is import this nav bar into this app root component and then nest it somewhere inside this

[03:24](https://www.youtube.com/watch?v=undefined&t=204s)

template so the first thing we need to do is import it so i can say import the nav bar and it's gonna be from and then it's dot forward slash to say the current directory and then navbar we don't need to say dot js when we're using this import it figures that out itself okay so now we can nest it down here and i'm gonna nest it just above the content div right here because all of the page content will ultimately go inside here but the navbar i'm gonna place above that now to do this we just say navbar and then

[03:58](https://www.youtube.com/watch?v=undefined&t=238s)

close this tag so it's self-closing and this name is this name right here okay so this doesn't have to be self-closing you can do an opening and closing tag as well if you prefer but if you don't close the tag then you need it to be self-closed over here okay so save this and it works we can see that navbar component at the top let me just show you the other way if we were to do a closing tag instead save that and refresh this still works i generally go with the self-closing tag instead okay so that's our second

[04:34](https://www.youtube.com/watch?v=undefined&t=274s)

component now we have two we have the app root one and the nav bar which is nested inside the root component now i also want to do a component for the home page content because i don't just want to create it all inside this root component i want to make a separate component for the content of the home page so let me do that by first of all creating a new file called home.

[04:58](https://www.youtube.com/watch?v=undefined&t=298s)

js and then inside here another stateless functional components press tab and i'm going to call this home now inside these parentheses i'm going to return a template a div with a class of home and i'm applying these classes so that later on we can style them in the css and inside this we'll just do an h2 that says home page and that will do for now so again i want to nest it now inside this component so the first thing i need to do is import it so import home from dot forward slash home and then i can nest it down here inside

[05:35](https://www.youtube.com/watch?v=undefined&t=335s)

this div so i'm going to get rid of this h1 and instead i'll put the home component just as a tag and now we should see that content on the page awesome so that's how we create multiple different components and then import them into other components and nest them and if i wanted to i could also create a further component and nest it in one of these i've just created like the home or the navbar and we're going to see more of that as we go forward but next up i want to take a look at using css in our project
***
-   React components are structured in a tree, with the root component at the top.
-   Components can be nested inside the root component, as well as other components.
-   To create a new component, a new file with a function that returns a JSX template is needed.
-   The package 'simple react snippets' can be used to create a functional component.
-   Components can be imported into other components and nested within them.