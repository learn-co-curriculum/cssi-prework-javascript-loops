---
tags: cssi, javascript
level: 1
languages: javascript
---
# Loops
####After the lesson, you'll be able to:
+ Understand how loops run an operation multiple times
+ Understand how an exit condition stops a loop
+ Iterate over arrays using for loops and while loops
+ Convert repeatable tasks into loops

####Key Points:
+ Loops let you repeat a bit of code until an exit condition is met
+ A loop's exit condition is a boolean statement that is evaluated during each loop; if it's false, the loop stops
+ Loops can be very useful for iterating (stepping through) an array and doing something to each element
+ A loop that doesn't have a valid exit condition will run forever and is called an infinite loop. These are bad, most of the time

##Concept
A loop is one of the foundational tools in any programmer's toolkit. It allows a bit of code to be repeated many times. 

This can be useful in many circumstances but is often used with arrays. Arrays can have any number of elements and a loop allows us to access each one of those elements and do something with it.

Let's start with an example array of numbers. 
```
var numbers = [0, 1, 2, 5, 9]
```
Ok, what if we want to do something to each number. Like multiply each number by 5. We could do it manually:
```
numbers[0] = numbers[0] * 5;
numbers[1] = numbers[1] * 5;
number[2] = numbers[2] * 5;
```
This would take forever.

A better way to do this is to set up a little machine with instructions on how to iterate (go through) every number in the array and do something specific to each one. We call this a loop.
There are two basic types of loops in JavaScript: for loops and while loops. They generally accomplish the same thing but their syntax is different.

##While loop
Let's say we want to make a while loop that multiplies every number in our numbers array by 5. It would look like this:
```
var numbers = [0, 1, 2, 5, 9];
var i = 0;
while (i < numbers.length)
{
  numbers[i] = numbers[i] * 5;
  i = i + 1;
}
```

* `var i = 0`; is the initialization of our counter variable. We will use it to keep count of which iteration (or cycle) we're on.

* `i < numbers.length`; is our exit condition. This is evaluated at the beginning of every loop, if it isn't true we stop looping and move to the code after the loop.

* `numbers[i] = numbers[i] * 5`; is the code we execute on every loop. This multiplies each number in the array by five.

* `i = i + 1` is where we increment our counter. In this case, we increase it by one, so it works as a counter, but it doesn't have to.

Try using console.log(numbers); both before and after the loop to see how our array has changed. Try using alert(numbers); instead

##For loop
We can accomplish the exact same thing with the more concise for loop. It would look like this:
```
var numbers = [0, 1, 2, 5, 9];
for(var i = 0; i < numbers.length; i = i + 1)
{
  numbers[i] = numbers[i] * 5;
}
```
In a for loop, our initialization, exit condition, and increment all happen in one line separated by a semicolon `;`.

Let’s walk through each part of this.
+ `for` is the keyword that we use to set up a loop
+ Inside of the parentheses is where we set up the conditions of our loop: 
  +   `var i = 0` - A counter variable **i** is set to 0. It’s convention to use the variable i because i is short for index 
  + `i < numbers.length`- In the next part of the conditions, we set up the exit condition for our machine : our variable i must be less than numbers.length. If this is not met, the loop is exited.
  + `i = i + 1`- The last condition of the for loop are instructions for how to keep our machine moving. Here we are saying - at the end of each iteration in the loop add one to var i.

+ Inside the curly brackets are instructions for what should happen to each element that we loop through
  + `numbers[i] = numbers[i] * 5` - For each element, reassign that element a value that is five times greater. 

## Student Practice
Create a iteration.js doc. 

###Part 1, A Loop with  Numbers
Set up a _for_ loop with a numbers array -  print out each number, doubled.

Next, wrap your loop in a function, doubleNumbers that accepts a numbers array instead of hardcoding one specific array into the function. 
.
###Part 2, A Loop with String Methods
Create an array of your top 5 favorites movies. Now create a function called myFavorites().

This function should
+ take in an array of favorites
+ for each favorite, it should alert to the screen something like “The Shawshank Redemption? That is my favorite too!”

Now create a new array of your favorite songs. Try calling the myFavorites() function with the songs array.

###Stretch: The Movie Critic
Change myFavorites() into a _while_ function.  The condition  should check to make sure that the movie is not Demon Islan, Gigli or Santa with Muscles. 
