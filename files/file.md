# Files


__Understanding the In’s and Out’s__

So far we’ve learned a lot about the basics of programming in Ruby. We’ve learned about strings, numbers, variables, collections and methods--core concepts to all programming languages. These are the building blocks to programming. Understanding these basics will help you with Ruby and any other languages you may learn in the future.

But there is one more aspect we should cover so you can start writing your own programs. So far we have modified strings and numbers with input and output from our console. But what if we wanted to manipulate entire files instead?

We can start interacting with files using Ruby’s File Class. Here’s what it would look like to create, open and write to a file.

```ruby
the_file = File.open("my_file.txt", "w")
the_file.puts "First line of our file."
the_file.close
```

In the example above, we used the File class and the `open` method, sending in two parameters. The first, `my_file.txt` is the name of our file we are creating. The second is the `w` option, which tells Ruby we want to write to our file. On our next line we use puts to write a string of text to our file. Lastly, we close the file with the `close` method.

If you open up a terminal window and enter Ruby’s Interactive Shell (IRB), you can run each of the lines of code above. To see your file, type `exit` to leave the Ruby shell and type `ls` to list your files. You should see `my_file.txt` in your directory. Type `open my_file.txt` , to open your file and see the line we wrote earlier with the puts statement.

If we want to add to this file, we could use the same code above, but with the append `'a'` parameter passed in as the second argument to open. If we used `w`, we would overwrite all of the contents of our file. If we use the `'a'` parameter we can add to our file without overwriting it.

Now, if we wanted to read our file, there are two basic ways for us to do that. We could either read all of the lines of the file at once, or one at a time. Here’s how to read the file using the `'r'` option. The `'r'` option stands for read only.

```ruby
file = File.open("our_file.txt", "r")
entire_file = file.read
puts entire_file
> This is a text file.
> This is line 2 of the file.
> And this is line 3.
=> nil
```

By using the `'r'` option we are opening the file in _read-only_ mode. Any writing we tried to do to our file here would fail. But we can call the `read` method and store the contents of our file in the entire_file variable, and then put the variable to the screen.

If we want to read each line, we can use the `readlines` method.

```ruby
File.open("our_file.txt").readlines.each do |line|
  puts line
end
```

Though both ways of reading the file will read and output each line, there is a significant difference in what these two methods return. For our read method, the entire file is captured and `nil` is returned. For the readlines method, each line is stored inside of an array, with the entire array returned at the end of the method.

Here’s an example of what that might look like.

```ruby
file_array = File.open("our_file.txt").readlines
=> ["This is our text file.\n",
    "This is line 2 of the file.\n",
    "And this is line 3."]
```

We open our file with `File.open` and then call the readlines method. Each line of the file is added to an array until all lines have been read. Notice the `\n` new line characters inside of our strings of text. Remember, we can remove these using the each method and passing in a block with chomp.

```ruby
file_array = File.open("our_file.txt").readlines
  .each { |line| line.chomp! }

=> ["This is our text file.",
    "This is line 2 of the file.",
    "And this is line 3."]
```

Wow! Now you know how to open, write, and read files! And don’t forget to close your files in your programs with the close method. It can be a bad thing to leave them open, because the computer won’t actually write and save the file until just before its closed. Also, open files can lead to overloading your memory usage.

<div style="height:30px;"></div>
