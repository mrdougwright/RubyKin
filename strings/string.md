# Strings


Congratulations! You are halfway through learning the two most fundamental 'blocks' of programming code--Numbers and Strings.

Remember that a string is simply a piece of data (usually words) wrapped in quotes.

In Ruby, we can perform some math-like operations using our friends, the strings. For example, we can multiply a string like so:

```ruby
"repeat " * 3
=> "repeat repeat repeat "
```

In the above example we have a string: `"repeat "` that we multiply `*` by three. When Ruby performs the `* 3` method it actually just copies the string three times and pastes the result together. Sort of like this:

```ruby
"repeat " + "repeat " + "repeat "
=> "repeat repeat repeat "
```

In fact, you can write either of these lines of code and the result will be the same. Much in the same way that writing `3 + 3 + 3 = 9` yields the same result as `3 * 3 = 9`. When the computer adds strings together we call it concatenation.

```ruby
"Cat and " + "Dog"
=> "Cat and Dog"
```

In the example above, there are two strings, one is `"Cat and "` and the second string is `"Dog"`. By giving the command to add the two strings `+`, we are able to join both strings together using the magic of concatenation. (Concatenation is just a fancy old Latin word for join together).

![Art by Vixuong Hong](http://rubykin.com/images/cat-dog.png)

Ready to try it out?

Open Terminal again (or http://repl.it/languages/Ruby) and try multiplying and adding a few strings yourself to get the hang of it.

Now try adding a number with a string. It didn’t work did it? Remember that joker `"9"` string from our previous example in chapter one? Ruby doesn’t see this as the actual number 9, instead it sees a string.

To Ruby, anything that is inside the quote isn’t just a word or a number anymore. Everything inside the quotes is a string. So when we try to add a string with a number, Ruby gives us an error:


```
"9" + 9
=> TypeError: can't convert Fixnum into String
```

In the above example, we would see `"9" + 9` and think the answer is 18. But Ruby doesn’t see it like that. Ruby sees `"STRING" + NUMBER`. And you can't add strings and numbers, because they are different _types_ of data.

This doesn’t mean we can’t do this sort of equation, it just means we need to use a trick to make sure Ruby understands what we want. Of course, there are lots of interesting methods or _actions_ we can perform to get Ruby to do what we want.

We’ll look at some of those _actions_ a bit later, but for now, you could solve the above problem by using the _to integer_ method, or `to_i`. This would convert the string to a number (more specifically, an integer). And with two numbers, Ruby can do the math:

```ruby
"9".to_i + 9
=> 18
```

Remember those `\n` characters from the first chapter? This is what the computer uses to note a _new line_ in your string. So the following string:

```ruby
print "One line.\nAnother line.\nAnd another.\n"
```
Would print like this:

```
One line.
Another line.
And another.
```
In this way, Ruby can store sentences or even whole files inside just one string. Now that you have a better understanding of strings, check out some examples below.

<div style="height:30px;"></div>
