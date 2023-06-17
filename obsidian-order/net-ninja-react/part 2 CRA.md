[00:02](https://www.youtube.com/watch?v=undefined&t=2s)

all right then so there's a few different ways to get started with react but the easiest way in my opinion is to use a tool called create react app now this is a command line tool which generates a star to react project for us and it comes fully baked then with all of the setup and config that we need like babble and webpack now we need those to compile our react code and jsx later into production ready javascript and without the tool create react app we'd have to configure all of that ourselves so we'll be using create react app to

[00:32](https://www.youtube.com/watch?v=undefined&t=32s)

create our starter project now to do this you need a modern version of node installed on your computer ideally version 5.2 or above and that's so we can use npx which comes with modern versions of node to run the create react app tool now you can check that you have node installed on your computer by opening up any terminal on windows you can use command prompt by typing cmd and opening that up i'm going to use windows terminal right here and then type in node space hyphen v and press enter now if it shows you a

[01:07](https://www.youtube.com/watch?v=undefined&t=67s)

version number like it does on mine then you have it installed if you don't see it you need to install it and also if you see a version less than 5.2 you also need to install the latest version instead so to do that you need to go to nodejs.org i'm just going to open this up in a browser over here and you need to download the current version right here so go through the installation steps and then you can carry on with this course so let's now set up our react starter project the first thing you need to do

[01:40](https://www.youtube.com/watch?v=undefined&t=100s)

is navigate into the directory where you want to create this project so to do that i'm going to type in cd for change directory space then i'm going to go into the documents folder then i'm going to cd into a folder called tuts and this is where i'm going to create my project now to do this we say npx and then create hyphen react hyphen app and then the name of our project i'm going to call this dojo hyphen blog and this will then run this code which is on the internet and that's what this npx tool allows us to do that's why

[02:14](https://www.youtube.com/watch?v=undefined&t=134s)

we need node and it runs this create react app and it installs a new react project called dojo blog for us in this location so press enter and this is just going to take a couple of minutes to create all right then so once that's done we can cd into the new project directory which is called dojo blog in my case and then i'm going to open this up in vs code by typing code space and dot and that opens up vs code in my current directory right here dojo block so the new project so this here my friends is the starter

[02:54](https://www.youtube.com/watch?v=undefined&t=174s)

project created by create react app so when you first look at all of this if you're new to react and you open these different folders and you see all of these different things you're probably thinking um looks a little bit complicated but believe me once you start working with react it really is pretty simple now i'm going to give you a brief overview now of what everything is but don't worry if you don't understand everything 100 right now because as we start to work with react more and more

[03:22](https://www.youtube.com/watch?v=undefined&t=202s)

it will just kind of fall into place but let's start with the node modules this is where all of our project dependencies live including the react library as well and any other package or library we need to install for the project later on is going to live inside this folder now you don't really ever need to go inside this folder just know that it's there and it's storing our dependencies next up we have this public folder which is where all of our public files public to the browser are going to live including this

[03:51](https://www.youtube.com/watch?v=undefined&t=231s)

index.html file so this is the one html file that is served to the browser and then all of our react code is injected into this one file right here inside this div with an id of root again you probably won't come in here much but if we do don't worry i'm going to show you how we edit things later on all right so next up we have the source folder and probably 99 of the code that you write when you're working with react is gonna go inside this source folder so all of our react components that we write are gonna live

[04:26](https://www.youtube.com/watch?v=undefined&t=266s)

inside here and there's already one created for us called app.js so this is what a component looks like at first glance we're going to come back to this later on so i don't want to spend too long here we also have some css files we have a test file which we don't actually need it's beyond the scope of this tutorial so i'm going to delete that we also have this index.

[04:48](https://www.youtube.com/watch?v=undefined&t=288s)

js file and this is the file that kind of kickstarts our application so this file is responsible for taking all of our react components and mounting them to the dom you see right here it's taking our app component and it's rendering it to the dom and it does that in that root div remember if we take a look at this again we see this has an id of root so that's where it's rendering our app component which is over here to the dom all right so now if we move on we have a logo which is currently being used inside app.js inside that component

[05:24](https://www.youtube.com/watch?v=undefined&t=324s)

this one is report web vitals it's kind of like a performance file which we don't really need either so i'm going to delete that and because we've deleted that i also need to delete this import right here inside index.js and this thing down here okay so make sure you delete those as well all right so at the end we have set up tests which again we're not going to cover in this tutorial it's kind of beyond the scope so i'm going to delete that as well all right so inside the source that's where most of

[05:53](https://www.youtube.com/watch?v=undefined&t=353s)

your code is written all of the different components and the index.js file this is what kickstarts our app and by the way this thing right here react.strict mode that means that react does additional checks during development and it gives us warnings down in the console if there are any warnings to reports all right so that's the source folder again we'll come back to all of this later on now we have a git ignore file just in case we're using version control with git and then down here we have these package files now this one right

[06:23](https://www.youtube.com/watch?v=undefined&t=383s)

here package.json does a few things first of all it lists all the dependencies of the application so anything our project depends on which all live inside node modules remember so right here these are the testing libraries we have react react dom react scripts and web vital so there are the dependencies and then down here we have some scripts as well so we can use these scripts to do things like preview our application in a browser on a local server or build our application for production or test our application or eject the

[06:56](https://www.youtube.com/watch?v=undefined&t=416s)

webpack file now i'll show you exactly how to do this in a second this is used to build the application for production and these are kind of beyond the scope of this tutorial so don't worry too much about them so that's kind of like the project overview and again please do not worry if that kind of went over your head it will all become more clear as we progress through the rest of the playlist so now what i'd like to do is show you how to take this starter project and preview it in a browser which is going

[07:25](https://www.youtube.com/watch?v=undefined&t=445s)

to be really important as we start to develop the project we want to preview as we go along so to do that we need to open up the terminal so go to terminal and click on new terminal i've got a shortcut which is ctrl t and then down here we're going to run one of those scripts we just saw and it's this one right here so to run this script all we need to do is say npm run and then the name of the script which is start so i can come down here and say npm run start that is going to spin up a local development server

[07:56](https://www.youtube.com/watch?v=undefined&t=476s)

so that we can preview the web application in a browser and once it's complete over here we should see what address it's being served so it's this one right here localhost port 3000 and that's just opened up in a browser over here for me so this is the starter project and this right here this content is coming from that app.

[08:20](https://www.youtube.com/watch?v=undefined&t=500s)

js component we very very briefly saw and it's all been injected into that one single html file inside the public folder and that's what we're seeing here if we inspect then we're going to see that div with an id of roots let me just get rid of those a little bit and scroll up and we can see this div right here with an id of roots and inside that we have this div with a class of app so this is the app component that's been injected into this div okay so let me just quickly show you that if we go into the source folder and then

[08:56](https://www.youtube.com/watch?v=undefined&t=536s)

go down here and open up app we can see this div has a class of app we see class name don't worry about that we'll talk about that later on but essentially that means an html class and that is the div that's been injected into the html file now remember it's the index.js file which is taking this app component and it's rendering it to the dom inside that root elements anyway this is a live reload server meaning if we make a change to our code inside this app component for example if we then save it it's then going to

[09:31](https://www.youtube.com/watch?v=undefined&t=571s)

auto refresh in the browser which is useful one last thing i quickly want to return our attention to is this node modules folder right here so this contains like i said all the project dependencies and it must be present for our project to work now if i was to delete this folder right here and then try to start the application let me demo this i'm going to delete it which might just take a second or two to do because it is very large in file size and currently visual studio code is not responding that's always a good sign

[10:05](https://www.youtube.com/watch?v=undefined&t=605s)

let's just give this a second okay so that took a minute but now it's gone and if i was to try and run this in a browser again by typing npm run start remember this is the command to spin up that local development server now notice we get all of these errors and that's because we no longer have the node modules folder and all of our project dependencies live inside this node modules folder including react itself but sometimes when you download a react project like from github then this node modules

[10:39](https://www.youtube.com/watch?v=undefined&t=639s)

folder is not going to be present and that's because the node modules folder is huge in file size and it contains the react.js library and many other javascript dependencies as well and if we left it in our projects when we uploaded or downloaded it to and from places like github it would take a much longer time to do and for that reason if we upload our download react projects we never include the node modules folder so if it's not present right here when you download it how do we get it once we have the

[11:08](https://www.youtube.com/watch?v=undefined&t=668s)

project downloaded how do we re-get that node modules folder well all we have to do is come down here and type in our project root directory npm install and what this will do is look inside the package.json folder which remember contains all of our project dependencies and it will install all of them and it will create that node modules folder which we can see now again and put all of the dependencies back in there so it installs all of those for us so that's why the package.

[11:40](https://www.youtube.com/watch?v=undefined&t=700s)

json file is so useful it lists all the dependencies that need to be installed if we download a project okay and then once this is done we can then run the project again by using npm run serve and it should work so if i try this again npm run serve now hopefully fingers crossed oops we get an error it's not npm run serve sorry it's npm run start to serve the application and now this should work yep it's starting the development server and pretty shortly we should see the address localhost 3000 and i can see it right over here okay so what is

[12:21](https://www.youtube.com/watch?v=undefined&t=741s)

the reason i'm telling you this well it's because the course files for this tutorial series are hosted on github and they won't include that node modules folder if you download them so if you do download them you have to run npm install down here in the terminal before you do anything else in order to get that node modules folder back so i know this was probably a pretty heavy tutorial which covered quite a lot but if anything did go over your head i promise you as we go on it's all going to click into

[12:53](https://www.youtube.com/watch?v=undefined&t=773s)

place so next up we're going to take a look at components including this one right here and how to create templates in those components