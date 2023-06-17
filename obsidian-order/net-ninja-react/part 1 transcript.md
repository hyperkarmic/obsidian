  
hey gang and welcome to your first step to become a react ninja [Music] now just really quickly before we start the tutorial for those of you who want to support the channel and join the gang officially you can do by clicking that join button right here it's just 99 cents or pence per month and you get these cool little ninja loyalty badges next to your name in the comments down below when you leave a comment you can also join by clicking the button right beneath the video if you're watching one now which i'm guessing you

[00:33](https://www.youtube.com/watch?v=undefined&t=33s)

are it does exactly the same thing all right so now that's at the way let's get on with the tutorial so i do have an older react tutorial already on my channel right here but that's now about two and a half years old so i wanted to do a complete refresh of the course with more modern ways of working with react including the use of built-in hooks custom-made hooks and also functional components so the course that i'm making right here and that you're watching is meant to be a complete replacement for this older

[01:04](https://www.youtube.com/watch?v=undefined&t=64s)

one and we're going to start at the very beginning so there's no prior knowledge of react needed and we're going to learn how to create react applications in a more modern and a cleaner way but first of all what is react well react is a javascript library that we use to create interactive websites and use interfaces and it makes it really simple to create something called a single page application or an sba for short now by single page i mean that the server only ever needs to send a single html page to the browser for

[01:37](https://www.youtube.com/watch?v=undefined&t=97s)

the website to run fully and then react takes over and manages the whole website in the browser including any kind of website data or user interactivity such as click events and even routing from page to page so users can still navigate from page to page by clicking links in the website but those new pages are not then sent to the browser from the server instead react changes all the content in the browser depending on the route of the url of the link that the user clicks for example if a user clicks on a contact link

[02:11](https://www.youtube.com/watch?v=undefined&t=131s)

then react will look at that url forward slash contact and then maybe inject a contact form onto the page so this process of react doing all of the work in the browser means that the new pages are loaded in really quickly and it results in a very speedy user experience now this process is in contrast to traditional websites whereby every link a user clicks sends a request to the server for a new html page so if you click on a contact link traditionally without react it would send a request to the server the server would look at this url

[02:45](https://www.youtube.com/watch?v=undefined&t=165s)

and then it would send back an html page to the browser and this will be the same for every page so during this playlist we're going to be making this mini micro blog whereby we can list different articles we can delete articles and we can also add new articles over here and it's a pretty small and simple project but by making this you're going to learn all of the fundamentals of react from using state the react router how and where to fetch data and how to use react hooks like you state and use effect

[03:17](https://www.youtube.com/watch?v=undefined&t=197s)

as well as creating a custom hook as well so by the end of this course you're going to be in a good place to start making your own bigger react applications now before you do start i would suggest that you at least know html and css because we're going to be using this to basically create templates for our different react components so i've got a complete html and css crash course on this channel if you want to brush up on that first of all the link is going to be down below i'd also strongly suggest that you understand at least the

[03:48](https://www.youtube.com/watch?v=undefined&t=228s)

basics of javascript as well because we will be using that in our react components too and again i've got a full playlist on modern javascript right on this channel the link will be down below so i'm going to be using vs code to create my project in you don't have to use it but all the cool kids do and you can install a package called simple react snippets which is going to be really helpful to you when you're creating react applications as well basically gives us all of these different shortcuts that we can use in

[04:15](https://www.youtube.com/watch?v=undefined&t=255s)

our files to generate boilerplate react components and other react things so definitely install that and also i want to show you this inside settings if you want to use emit inside react components when you're creating your templates then you need to edit the settings for emit so just type in emit and then you want to come down here see where it says include languages and add this item by clicking this button right here the key is javascript and the value is javascript react and that allows us to use emit inside

[04:48](https://www.youtube.com/watch?v=undefined&t=288s)

react components when we're generating the templates in jsx now emit is that little shortcut where we can say something like dot hello and that will create us a div with a class of hello you'll see more about that later on when we come to work with react templates but definitely adding this value for now finally before we start i just wanted to show you where to get all of the course files so it's this repo right here on my github complete react tutorial the link to this repo is going to be down below

[05:19](https://www.youtube.com/watch?v=undefined&t=319s)

in the description and if you want to see the code for a specific lesson you have to select that lesson from the branch drop down right here for example to see lesson 10 code click on this branch and you're going to see all of the code right here if you want to download lesson 10 then you go to code and then download the zip or you can clone this repo to your local computer whichever you're more comfortable with so that's the introduction out of the way in the next video we're going to go ahead and create our first react

[05:47](https://www.youtube.com/watch?v=undefined&t=347s)

application if you enjoyed this series my friends please don't forget to share subscribe and like the videos that really means a lot and i'm gonna see you in the next one