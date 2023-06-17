[00:02](https://www.youtube.com/watch?v=undefined&t=2s)

all right then so we have our three different components now we have the root component app.js the home component and also the navbar one as well now what i'd like to do is add some css to those components but how do we do that well if we take a look at this root component we already see this import app.

[00:21](https://www.youtube.com/watch?v=undefined&t=21s)

css and it's coming from this css file right here so when we created the boilerplate react application it came with these styles for the root component over here now anything inside this app.css file is going to be applied to not only the app.js components but also any component that is in the browser at that time that's because react just takes all of these styles and it adds them to the head of the web page so if we take a look over here if we inspect and go to the elements and take a look inside the head we're going to find a styles tag at some

[00:56](https://www.youtube.com/watch?v=undefined&t=56s)

point with all of those styles inside them it's this one right here okay so bear that in mind these styles if we import them into a component i'm not only going to style what's in that component but also anything else that is being displayed on the page at that time as well so it doesn't really scope the styles to a single component now you could use something called css modules to scope your styles or use something called styled components but that's not something i want to get into right now but maybe in the future

[01:28](https://www.youtube.com/watch?v=undefined&t=88s)

i'll do playlists about these so having separate css files for different components in our case at the minute is mainly just an organization thing for large projects i might sometimes do this but a lot of the time when i'm doing smaller projects i just have a single css file this index.

[01:48](https://www.youtube.com/watch?v=undefined&t=108s)

css file right here and add pretty much all of my css into that and this would kind of be like a global stylesheet and it would apply to all components so this index.css file is then imported into this index.js file right here and what this does then is take all of those styles and adds them inside the head again of the webpage and it's going to appear there all of the time so if we take a look at this it's the first style tag and it's this stuff right here so that's generally the approach i'm going to be taking for this project

[02:21](https://www.youtube.com/watch?v=undefined&t=141s)

so what i'm going to do is actually delete this app.css file and delete its import right here make sure you do that otherwise you'll get an error and then save it and then going forward i'm just going to use this index.css file for all of my styles so then let's flesh this out a bit the first thing i'm going to do is delete the current content and then i'm going to paste in first of all an import which is for a google font called quicksand so i got this from google fonts and by the way you can just copy

[02:51](https://www.youtube.com/watch?v=undefined&t=171s)

and paste all of these styles from my repo remember the link to this is in the description down below so that's the google font i'm going to use for this project next i'm also going to just copy and paste some bass styles because i'm pretty sure you don't want to watch me type out a load of css if you want to learn about css i've got tons of playlists on my channel about that anyway i will quickly go through them right here i'm targeting every element with the asterisks and stripping out the margin applying a font

[03:21](https://www.youtube.com/watch?v=undefined&t=201s)

family of quicksand which is this we imported and a text color of a dark gray now the nav bar right here which remember is this thing over here i'm styling that giving it some padding displaying as flex aligning the items center and that's vertically at this center not horizontally we give this a max width and a margin of zero auto we also give it a border bottom as well the h1 in the nav bar we make this already pink color the links we say margin left auto that shoots them over to the right because the parent is displayed as flex then the

[03:54](https://www.youtube.com/watch?v=undefined&t=234s)

anchor tags we say margin left of 16 pixels we take away the text decoration and give them some padding when we hover over those links we turn them that ready color and then the content which remember is right here so it's surrounding the home component at the minute we say right here give this a max width as well of 600 pixels margin 40 pixels top and bottom auto left and right to centralize it and then a padding of 20 pixels so some very simple styles now if i come over here and refresh we should see those styles take effect

[04:25](https://www.youtube.com/watch?v=undefined&t=265s)

awesome so that looks a little bit nicer so there's one more thing i want to show you and that's how to add some inline styling so let's do that inside the navbar components and we'll style this link right here so you know in regular html we can do a style property and we set it equal to a value which is a string and then add the different css properties in here now we can do a similar thing inside jsx but this time it can be a dynamic value and remember when we want a dynamic value we use curly braces

[04:55](https://www.youtube.com/watch?v=undefined&t=295s)

now the value of this is going to be an object in itself so we need another pair of curly braces inside the outer ones so the outer ones represent a dynamic value to tell react look we're using a dynamic value for the style attribute and this set of curly braces inside this is the object the javascript object okay so inside this object we do different key value pairs the key is going to be the css property and the value the css value for that property so for example i could say color for the key and then the value is always a string

[05:31](https://www.youtube.com/watch?v=undefined&t=331s)

and in our case it's going to be white so the text is white for this link then we do a comma and do another key so for example background color now this is where it gets a bit different because in css it's background hyphen color but remember we're in a javascript file and this looks a lot like a minus sign so we don't do this when we're using jsx for css we just camel case it like this background color and we set that equal to a value now i'm going to use the same hex code as this over here

[06:04](https://www.youtube.com/watch?v=undefined&t=364s)

so let me copy that and paste it in and then finally we'll do one more we'll give this a border radius again camel case and we'll set that equal to 8 pixels so 8 pixels like so all right then so this is how we do inline styling a dynamic value which is an object with key value pairs if we save this and preview now we can see this has taken effect now i'm not going to be keeping that style so i am just going to delete all of that but i did want to show you how to do it in case you want to do that

[06:37](https://www.youtube.com/watch?v=undefined&t=397s)

for some of your elements

***
- The tutorial is about adding styles to components in React.
- React takes all styles and adds them to the head of the web page, so styles in one component apply to all components on the page.
- CSS modules or styled components can be used to scope styles to a single component.
- The index.css file is used as a global stylesheet for all components in this project.
- The tutorial shows how to add inline styling to a link using JSX and dynamic values.