
Let's get some practice modifying the DOM and working with our strings and numbers. Below, you're are going to see the continuation of our profile page from the previous lab. You'll notice, we are starting to build out worlds simplest version of your facebook profile. As the future brilliant founder of a new social network, you need to implement the functionality for when someone gets a new friend, and when they change their current employer. I know that this is a _very_ simplistic version, but somewhere in the code for Facebook, Twitter, Pinterest and all of the other social networks is exactly code you are about to write. Only a few lessons in and you're on your way!

<iframe height='551' scrolling='no' title='Modifying The Dom' src='//codepen.io/joemburgess/embed/OpdGKE/?height=551&theme-id=0&default-tab=html,result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='https://codepen.io/joemburgess/pen/OpdGKE/'>Modifying The Dom</a> by Joe Burgess (<a href='http://codepen.io/joemburgess'>@joemburgess</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

## Making Friends

First, let's work on adding a new friend. Use the console (right click, inspect, then change the `top` dropdown to CodePen). 

![Codepen](https://web-dev-readme-photos.s3.amazonaws.com/js/select-code-pen.gif)

One you have the console open, discover what the `id` of the friends value (10) is. To do this, select the Element Inspector icon ![icon](https://web-dev-readme-photos.s3.amazonaws.com/js/elementinspector-icon.png) and then hover over the number `10`. You should see that the `id` is `friends`. That's pretty easy. Since this is an `id` we prefix it with a `#` and know that to grab this item we will need the code `document.querySelector("#friends")`. If you try that out in the console, you should see the `friends` element! Now, to modify the number we need to change its `innerHTML`. Go ahead and change that by writing `document.querySelector("#friends").innerHTML="11"` in the console. This should immediately work.

We did the first step, but I want you to take it from here. We need to change this code from just always setting to `11`, to just adding `1` to the current value. A few steps to take:

 1. Change the modification of `innerHTML` from setting the value to just number `11`, to adding `1` to the current value. First get it working in the console, then change it in the JS section of the CodePen.
 2. Modify the starter HTML code for friend's value from 10, to some other number. The view should auto update so that it displays one plus whatever you changed the code to
 3. Extra Credit. Can you save the `document.querySelector("#friends")` line into a variable and use that variable to modify the `innerHTML`?

## Changing Employers

Now let's move onto the employer section. You're going to be a bit more independent here. Can you modify the employer to be correct? It will be fairly similar to the code from the Making Friends section. A few steps:

 1. Use the console to find out the selector for the "Flatiron School"
 2. Use `innerHTML` on that selector to change the value to a different employer.
 3. Copy-Paste that code into the JS section so it sticks. 
 4. Extra Credit: Can you add an additional employer? So it will say "Flatiron School" and "Your Employer" on the next line? Remember `<br>` is how to make a new line in HTML. Also is this a String or an Integer?


Congrats! You just built a feature for the next Social Network. 

## Solution

#### Friends

```javascript
var friends = document.querySelector("#friends")

friends.innerHTML = parseInt(friends.innerHTML) + 1
```

#### Employer

```javascript
var employer = document.querySelector("#employer")

employer.innerHTML = "IBM"
```

Extra Credit

```javascript
var employer = document.querySelector("#employer")

employer.innerHTML = employer.innerHTML + "<br>IBM"
```
