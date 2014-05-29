
Why do we need to speak a strange language to communicate with computers?

Computers are a bit like dogs. They are great companions, but you need to give them commands to tell them what you want them to do. There are a lot of different programming languages, just like there are a lot of foreign languages. However, just as there are similarities in German, French or Spanish, there are similarities across programming languages, like JavaScript, Ruby or Python.

This book will help you learn the basics of programming, using the Ruby language. The building blocks you learn in this book will help you learn any other programming language.

Each chapter will go into more detail with basics at the beginning and more complicated material at the end. For now, let’s get started with some simple ideas.


__Integers, Floats and Strings__...and maybe Ice Cream

![Art by Vixuong Hong](http://rubykin.com/images/rootbeer_float.png)

Before we can understand how to write programs, we need to understand data. Data is simply information that you can input (give), output (get), store or manipulate with a computer. The two fundamental types of data used in almost every programming language are _numbers_ and _strings_.

Numbers come in two tasty flavors. Integers, which are whole numbers without a decimal point, and floats, numbers that contain a decimal.

For example, these are integers:

  ```ruby
  1, 7, 0, 13, 2000
  ```

And these are floats:

  ```ruby
  1.2, 3.14, 5.12345, 0.35
  ```

Every time you see a whole number like 8 or 19 you will know they are integers, and every time you see a number with a tasty sprinkle, or decimal, they will look like this: 3.4 or 8.1 and you will know they are (root beer) floats.

Simple, right? Ok, let's keep going.

The second type of data, or information given to a computer, are called _strings_. What’s a string? "Anything between quotes is a string." Since that last sentence was inside of quotes, it was technically a string! You probably see strings all the time without even realizing it!

For example, have you ever seen an alert message on your computer saying something like this:

![example alert message](http://rubykin.com/images/alert_message.png)

Somewhere inside a program or web application, an engineer wrote the sentence "File does not exist!" and put it in quotes to create a string. When you were alerted with the pop up box, that string was printed to the screen.

Strings are a little bit like backpacks or lunch pails, they are great for storing all the stuff we care about in an easy-to-carry container. Except with a string, the straps are the quotes. We use strings to store words, sentences, and even files. Here are some examples of strings:

```ruby
"I'm a string!"
"And_so_am_I"
"9"
"This long paragraph is even a string.\nAnd it has these
strange \n things that we'll explain later."
```

9 is such a joker. Did you notice we put the number nine as a string? This is very different than the actual number nine, but we will get to that later.

Now that you know the two most fundamental pieces of data the computer uses (numbers and strings), it's time to dive a bit deeper into each of these data types.
<div style="height:30px;"></div>
