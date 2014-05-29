# If and Else


"If you clean your room then you can play, or else you won’t." - Mom

_If_ and _else_ statements help Ruby understand what you want her to do and when you want her to do it.

So far, we’ve learned how Ruby can perform basic math on numbers, store words and sentences as strings, and place these types of information into memory stored in variables. Now that we know how to store information and interact with it, we need a way of telling the computer what to _do_ with that information.

One way we do that is with conditionals. This is why your parents say they love you unconditionally, because there is no _if_ or _else_, there is only 100% love, no matter what. Ruby doesn’t love anything unconditionally, Ruby needs to be convinced by conditions.

A conditional is something that depends on other factors. If this _something_ happens, do _that_, otherwise, do something _else_. For example, if you are hungry, eat a sandwich, else, don’t eat a sandwich!

![Art by Vixuong Hong](http://rubykin.com/images/eat-sandwich.png)

Here’s how an If Else conditional might look in Ruby.

```ruby
# set an x variable to the value 5
x = 5

# start the if / else conditional
if x <= 10
  puts x
else
  puts "Number is greater than 10"
end
```

In a conditional, the computer checks to see that the code after the _if_ is true. We call this code a block, which just means a small piece of code that has some function. In this case, our block is
`X <= 10`.

So, _if_ our block is _true_ (if X is less than or equal to 10), the computer will perform the action in the next line below the if statement. Since X is equal to 5, it _is_ less than 10, and the value 5 is _put_ on the screen. If X were 11, the conditional (X <= 10) would realize this was a false statement, and the string "Number is greater than 10" would be outputted (shown) on the screen.

When the computer moves through an if-else conditional, it will follow the instructions under the _first_ if statement that evaluates to true. It then ignores all other conditions in the if-else conditional.

<br />
__What is a boolean?__

We've just learned how a conditional checks to see if something is `true` or `false`. A true or false value is called a _boolean_ in programming. We could write another conditional in a different way using booleans.

```ruby
if false
  puts "false"
elsif true
  puts "true"
else
  puts "This won’t print"
end
```

Let’s walk through each step to get a better understanding. `Nil` and `False` are the only objects in Ruby that are considered _falsy_. Something is falsy when it has a false value. `Nil` is Ruby’s way of representing nothing--nada, zip, zero! No value stored here whatsoever!

In the example above, the conditional checks to see if _false_ is true. Since the `false` object will never be true, the computer moves on to the next line to see if `true` is true. It is, so Ruby puts the string _true_ to the screen!

The final `else` will never print, because true will always evaluate to true and so the program exits before getting to the _else_ line. Remember, Ruby is only looking for the _first true_ if statement, ignoring everything else.

Here are the basic elements used to evaluate conditionals:

```ruby
<   # less than
>   # greater than
<=  # less than or equal to
>=  # greater than or equal to
==  # equal to
!=  # not equal to
```

When checking if an object is _less than_ or _greater than_, we use the same symbols found in math. When checking if some object is equal to another object, we use two equal signs. In Ruby, like many programming languages, one equal sign is used to assign or _give_ a value to a variable. If we want to check that an object is _not equal_ we use an exclamation mark before the equal sign. In Ruby, we could also simply use the word `not`.

<br />
__What's an object?__

You may have noticed that we keep talking about things as _objects_. To understand a _code object_ think about an object in real life. A ball, a book, or even your dog--these are all different types of objects or physical things. In programming, we try to represent real life objects with code objects.

For example, if you walk the dogs in your neighborhood, you may know their names in your head. Rex, Sparky, and Spot. But how would a computer know their names? Well, we could represent each _dog_ as a _string_ object in Ruby, like so:

```ruby
["Rex", "Sparky", "Spot"]
```

In fact, this line of code is actually four objects! Can you see why? We have Rex, Sparky and Spot, that makes three objects. But we also have the list of dogs, which is another object! This is the neat thing about Ruby, _everything_ is an object. Let me say that again.

<br />
<div style="text-align: center;">
__*Everything is an object*__
</div>
<br />

That means that every thing you have learned so far was a type of object. Numbers, strings, variables, if statements, booleans and even code blocks (such as X < 10)...these are all objects!

Next chapter we'll learn about Loops. (Yep, loops are objects too). Don’t worry, these aren’t the roller coaster type of loops.

<div style="height:30px;"></div>
