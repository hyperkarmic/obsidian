so then components are the building blocks and the beating heart of any react application and a typical web page built with react might be made up of several different components where each component is normally a self-contained section of content for example a navbar in a website might be a component an article might be a component and a sidebar might be a component etc it's basically our job as a react developer to create these components which are then rendered to the dom and shown in the web page by react now each of these components

[00:37](https://www.youtube.com/watch?v=undefined&t=37s)

will contain all of their own templates and all of their own logic for that piece of content for example a navbar component will contain a template which makes up the html for this bit of content but also any javascript logic like a function which runs when maybe a logout button is clicked now react components allow us to do these things really really easily so to begin with in our application we only have one single component which is being rendered and that is this component right here app and by the way i'm

[01:12](https://www.youtube.com/watch?v=undefined&t=72s)

inside the index.js file inside the source folder this is the file remember which kickstarts our application and at the minute what it's doing is taking this app component right here and it's rendering it to the dom at this position so the element with an id of root so then this component right here all of the content inside that component is being rendered to the browser and that's what we're seeing right here all of this content is this content over here so this component this is known as the root

[01:44](https://www.youtube.com/watch?v=undefined&t=104s)

component now we'll talk more about what a root component means later on but essentially this is the only component at the minute which is being rendered to the dom and inside this component we can see it is basically a function called app and that returns what looks like some html code now this function could be an arrow function if you prefer but it has to start with a capital letter so this one is called app and it returns this code right here like i said it looks like an html template and this is all of the

[02:16](https://www.youtube.com/watch?v=undefined&t=136s)

stuff all of the content we're seeing over here but this is not actually html it's something called jsx now it has a syntax almost identical to html but there are some differences which we're going to talk about later on so jsx allows us to easily create these html style templates and components and in the background a transpiler called babel converts all of this jsx template into html when we save the file and it renders that html to the dom okay so you don't have to worry too much about how this happens but just know that this

[02:54](https://www.youtube.com/watch?v=undefined&t=174s)

kind of thing is going on in the background and this template code right here is jsx now one big difference between jsx and html is the way we add classes to elements because in jsx we use this attribute class name and it's also camelcase notice n is a capital now the reason we can't use just class is because class is a reserved keyword in javascript and at the end of the day we're in a javascript file right here so we can't use class we use class name in jsx and then when this is converted into html it

[03:32](https://www.youtube.com/watch?v=undefined&t=212s)

changes this attribute into just class so if we inspect this over here we're gonna see that it should have a class of apps so it doesn't say class name just class okay so that's one difference and there are other differences which we'll see later on as well now one thing i want to quickly mention is that in older versions of react less than version 17 you need to import or react at the top of the file inside components for them to work notice we don't import react anywhere up here we input these other things but not

[04:06](https://www.youtube.com/watch?v=undefined&t=246s)

react so if you're using version 16 for example and not the latest version for this to work you might see in your file something like this import react from react like this and then this file would work but in version 17 we don't need to do that okay but that's important if you're using an older version so there's one more thing i want to do in this video and that's to remove most of this template content right here so everything inside the div with the class name of app will keep this to surround

[04:40](https://www.youtube.com/watch?v=undefined&t=280s)

our code so we have to return this template inside a component right and now we have this empty div but i also want inside that a div with a class of content so i'll say div dot content and this was the emmit setup i talked about in the first video because now if i press tab it's going to create that div with a class name of content all right so inside that i'm going to do an h1 and this is just going to say app components like so and now i'm going to save this and in fact we can take away this import for the

[05:13](https://www.youtube.com/watch?v=undefined&t=313s)

logo we use that before inside the template but we don't anymore so let's get rid of that and save this file and now if we come to the browser we see this very simple template and also we can delete this logo over here we're not going to be using it in our project so get rid of that as well so then this thing right here this is just one single component and i said before that react websites can be made up of many different components so later on we will be adding more components to this as well but in

[05:43](https://www.youtube.com/watch?v=undefined&t=343s)

the next video i'd like to talk a little bit more about the template and how we can output dynamic values inside the template but before we move on just one more thing i want to mention and that is this thing right at the bottom of the file over here the export so at the end we always export our component function and that's so that we can use it in other files and right here inside the index.

[06:07](https://www.youtube.com/watch?v=undefined&t=367s)

js we're doing exactly that we import this app component from forward slash app so this file and then we're using it right here and this is then being rendered to the dom using the react dom library okay so a component in a nutshell is a function and then we always must return something inside that function and generally that's going to be a jsx template and then at the bottom we export that component so we can use it elsewhere as well