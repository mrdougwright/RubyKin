# Loops


At its most basic level, a loop is when a computer repeats a specific task. A computer is kind of like a robot, because you can make it do lots of things very quickly. When you give it a loop, you're telling the computer to repeat a task over and over. Since the computer can perform thousands of operations within a second, loops become very powerful. Let’s look at a previous code example again to help us understand loops.

```ruby
x = 0
while x < 5
  puts x
  x = x + 1
end
puts "Finished the while loop."
```

This is called a `while` loop. The statement after the word _while_ must be true for the loop to continue running. In this example, we set x to the value zero. Our _while_ loop checks to see if our statement is true: `x variable is less than 5` and it is! So, the computer executes the code (follows our block of instructions) between _while_ and _end_ until X is no longer less than 5.

This loop tells the computer to perform a task _WHILE_ certain things are happening. Your parents would tell you to look both ways, _while_ you cross the street. In a way, you are being programmed to perform the task of looking both ways before crossing the street. If there are no cars, it's safe to cross.

The word `puts` is a method that simply "puts" the following content to the screen. Technically, it means `put string` and takes a string argument to put on the screen.

Here is some pseudo code to see what's happening in our _while_ code.

```
# pseudo code
1) x is 0
2) Is 0 less than 5? True. puts x. x = 0 + 1. x is 1.
3) Is 1 less than 5? True. puts x. x = 1 + 1. x is 2.
4) Is 2 less than 5? True. puts x. x = 2 + 1. x is 3.
5) Is 3 less than 5? True. puts x. x = 3 + 1. x is 4.
6) Is 4 less than 5? True. puts x. x = 4 + 1. x is 5.
7) Is 5 less than 5? False. Loop ends.
8) "Finished the while loop." is printed to the screen.
```

In this example, the x variable is set to zero outside the while loop. When the while loop begins, the computer checks to see if x is less than 5. Since 0 is less than 5, this is a true statement and the computer moves on to puts x, which displays the value of x to the screen. The next operation is to assign x the value of x + 1 (in this case 0 + 1). When it gets to the end, the loop repeats to see if x is still less than 5. Since 1 is less than 5, we put 1 to the screen and assign x the value of 1 + 1, and the process continues. Once x is equal to 5, the loop stops because the statement (5 < 5) is no longer true, it's false. After exiting the loop the computer executes the final puts statement.

The end result looks something like this:

```
0
1
2
3
4
Finished the while loop.
```

![Art by Vixuong Hong](http://rubykin.com/images/roller-coaster.png)

<br />
_While_ loops are great for counting, but they can be used in other ways as well. For example, what if we played a game that wouldn’t let the player move forward unless they got the right answer?

```ruby
answer = ""  # creating an empty String variable
while answer != "Ruby"
  puts "Sorry, wrong answer." unless answer == ""
  puts "What is the best programming language?"
  answer = gets.chomp
end
puts "That's right!"
```

We are using a few new Ruby vocab words, or methods: `gets` and `chomp`. Don't worry, we will get to methods later, but here's what's happening.

In the example above, the computer will continue to prompt the user for "the best programming language" until the answer equals "Ruby". We assign the users answer to the variable `answer` using the built-in Ruby method `gets`. Gets is like a little helper monkey that helps the computer "get" a piece of information that is entered into the terminal.

Chomp is also a method. Its special task is to remove the last _new line_ character. When you hit _enter_ the `\n` new line character get stored, but chomp will remove it.

Gets and chomp are merely methods we use to cleanly assign the user’s input to the answer variable (without that strange new line character). Once the user enters the right answer, the computer exits the loop and ‘That’s right!’ is printed to the screen.


We can look at another example using a _for loop_.

```ruby
for number in 1..5 do
  puts "The current value is #{number}"
end
```

The for loop starts without a true condition being met. This loop will execute the code block between _do_ and _end_ once for every number in the range 1 through 5 (that's the 1..5 part). The word `number` is just a temporary variable that represents each item within our _for loop_ range. For example, a range of 2 through 8 would be written 2..8. A range of 1 through 25 would be written 1..25. Easy, right?

The funny number sign and curly brackets is a string interpolation. We will cover this later, but all you need to know right now is that it places the value of our _number_ variable inside the string. The output would look like this:

```
The current value is 1
The current value is 2
The current value is 3
The current value is 4
The current value is 5
```

Hopefully you are beginning to see the power of loops in Ruby. There are a few other loops, but _while_ and _for_ are the standard ones to start with. When we combine loops with collections, our programs become even more valuable!

Imagine a comic book collection, or a marble collection, or a toy collection. They are full of individual comics or marbles or toys. Imagine how much easier it would be to count, sort and organize our collections if we had the super fast computers helping us while we do other things! Next, we’ll show you how to get Ruby's help in handling collections. For now we'll finish the chapter with some examples.

<div style="height:30px;"></div>
