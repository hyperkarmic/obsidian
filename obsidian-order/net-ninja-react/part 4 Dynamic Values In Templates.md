[00:03](https://www.youtube.com/watch?v=undefined&t=3s)

so another good thing about jsx templates in react is that we can output dynamic values or variables inside it so imagine we wanted to output a blog title on the screen well yeah we could hard code it right here we could just write it in the h1 but we could also output a variable instead right here now we can create the variable inside the function before the return template so i'm going to say const and then we'll call this title and set it equal to something and by the way you can write any valid javascript inside this function

[00:34](https://www.youtube.com/watch?v=undefined&t=34s)

before we return the jsx template so all of this is fine and i'm going to set this equal to welcome to the new blog so if i want to output this value this variable inside the template i can do all i need to do is use curly braces and then the variable name so when we use curly braces like this react knows we want to output a dynamic value or variable so it's going to look for the value of this variable up here and it's going to output that right here inside the h1 so if i save this and preview we can see

[01:09](https://www.youtube.com/watch?v=undefined&t=69s)

that value on the screen awesome now we can output multiple values inside this template right here all we have to do is create them at the top so i could create another one called likes and set that equal to something like 50 and then down here i'm going to do a paragraph tag and say liked and then curly braces to output a variable and then likes and then i'll say times so it should say liked then 50 times if i save this and preview then we can see it right here now notice that this time it's a number

[01:40](https://www.youtube.com/watch?v=undefined&t=100s)

and not a string but that doesn't matter because react is going to convert whatever data type that we use to a string before it outputs it to the browser so we could use an array if we wanted to it would just convert that to a string and then output it the only thing we can't output are booleans or objects so for example if i try to create another constant called person and set it equal to an object and in here we'll have a name which is yoshi and also an age property which is going to be 30.

[02:11](https://www.youtube.com/watch?v=undefined&t=131s)

if i now try to output this down here paragraph tag and then person like so if i save this come over here i'm going to refresh notice we get an error and we cannot output this object so numbers strings and arrays fine booleans and objects we can't so let me just comment these out so they don't cause an error and save it now as well as outputting variables we can also write the dynamic values directly in the curly braces so for example i could write any kind of javascript statement inside these curly braces that returns a valid value

[02:51](https://www.youtube.com/watch?v=undefined&t=171s)

either a string a number or an array so let me just do a number like this and it outputs 10. let me do another example another paragraph tag and this time i want to output a string well we just use quotes for that and say hello ninjas like so save it and we see that string do another example i'm going to output an array so curly braces and then an array inside here i'll just say one two three four and five and save that and we can see this array all it does is bunch all of the different elements in the array together and it outputs those as a

[03:31](https://www.youtube.com/watch?v=undefined&t=211s)

string and then after this we can also output little evaluations like this i could use the math object dot random and then maybe times that by 10 like so so it's gonna evaluate this which returns us a number and then it's going to output that number as a string in the browser so if i save this we can see we get a random number if i refresh it's going to be different each time around okay so another thing we can do in jsx is use these dynamic values as attribute values in element tags so for example we could

[04:07](https://www.youtube.com/watch?v=undefined&t=247s)

have an anchor tag and this has an href attribute now normally we'd put the attribute as a string right here to a website for example http www.google.com like so i'm just going to say over here google site but in jsx this can be a dynamic value so i could cut this and store it in a variable at the top over here const link is equal to this string we just created and then down here if i want to use a dynamic value for an attribute i just use curly braces so we don't need the quotes first and then curly braces

[04:46](https://www.youtube.com/watch?v=undefined&t=286s)

it's just curly braces and then we put the dynamic value inside the curly braces so the name of the constant link for example if i save this now and come over here i'm going to inspect this to make sure we have the right href yep and it's popped in that dynamic value to the href right here now at the moment things like this might seem a little bit pointless but later on when you start to work with dynamic data then it becomes very very useful for example you might have a list of blog titles from a database and

[05:17](https://www.youtube.com/watch?v=undefined&t=317s)

each blog title must be a link now that link is going to be dynamically output for each blog because each blog title should click through to a different blog details page right so we're going to see more of this as we go forward