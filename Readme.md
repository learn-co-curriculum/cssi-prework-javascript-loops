# Loops
A loop is a set of commands that executes repeatedly until a specified condition is met. JavaScript supports the for, do while, and while loop statements. They generally accomplish the same thing but their syntax is different.

##Objectives
* Loops vs forEach Method
* While Loops
* Do/While Loops
* For Loops


## Loops vs forEach Method
Arrays have a built in method, `forEach` which can also repeat an action. However you cannot break out of a forEach loop. Using the forEach method is also a little bit slower than using a for loop. To loop over an array, you can use forEach or a for loop to accomplish the same task.

In general, loops are more flexible and they can be used with datatypes besides arrays - they are a more versatile tool.


##While Loops
A while statement executes its statements as long as a specified condition evaluates to true (*While* condition is true). While loops are generally used when the number of iterations is unknown.

A while loop checks the condition, then executes the loop.

```javascript
while (condition){statement}
```

Let's say we want to make a while loop that multiplies every number in our numbers array by 5.

```javascript
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

* `i = i + 1` is where we increment our counter. In this case, we increase it by one, so it works as a counter, but it doesn't have to. This is important! If you don't increment your counter, your while loop will continue for ever, as your counter will always be under the length of the array!

Try using console.log(numbers); both before and after the loop to see how our array has changed. Try using alert(numbers); instead

## Do/While Loops
A do/while loop executes the statement first and then checks the conditions. It is very similar to the while loop, except that it is guaranteed to **run at least once**.

```javascript
do {statement} while (condition);
```
Example:
```javascript
var numbers = [0, 1, 2, 5, 9];
var i = 0;
do {
  numbers[i] = numbers[i] * 5;
  i = i + 1;
} while(i < numbers.length);

```
##For Loops
A `for` loop repeats until a specified condition evaluates to `false`. It accomplishes the same thing as a while loop, but is generally used when the number of iterations is known.  In a for loop, you can initialize the counter variable, define how to increment the counter variable and check your condition all in one line.

```javascript
for ([initialExpression]; [condition]; [incrementExpression]) {statement}
```

For example:
```javascript
var numbers = [0, 1, 2, 5, 9];
for(var i = 0; i < numbers.length; i = i + 1)
{
  numbers[i] = numbers[i] * 5;
}
```
In a for loop, our initialization, exit condition, and increment all happen in one line separated by a semicolon `;`.

These parts for the for loop are similar to the while loop:
+ `for` is the keyword that we use to set up a loop
+ Inside of the parentheses is where we set up the conditions of our loop:
  +   `var i = 0` - A counter variable **i** is set to 0. It’s convention to use the variable i because i is short for index
  + `i < numbers.length`- In the next part of the conditions, we set up the exit condition for our machine : our variable i must be less than numbers.length. If this is not met, the loop is exited.
  + `i = i + 1`- The last condition of the for loop are instructions for how to keep our machine moving. Here we are saying - at the end of each iteration in the loop add one to var i. This can be shortened to `i++`.

+ Inside the curly brackets are instructions for what should happen to each element that we loop through
  + `numbers[i] = numbers[i] * 5` - For each element, reassign that element a value that is five times greater.

###Loop Summary
Loops allow code to be repeated until a certain condition is met.
* While loops - the number of iterations is unknown,  the condition is checked before the statement is executed
* Do While loops - the number of iterations is unknown, the statement is executed before the condition is checked, so there will always be at least one iteration
* For loops - the number of iterations is known, condition is checked before any code is executed 
