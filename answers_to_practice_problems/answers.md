#Answers to Practice Problems

<br />
__Chapter 2 - Numbers__


1) `2 + 3 + 5`
  `=> 10`

2) `10 - 3`
  `=> 7`

3) `9 / 3`
  `=> 3`

4) `4 * 2`
  `=> 8`

5) `4 ** 2`
  `=> 16`

6) What is the result of `11 % 5` ?
  `=> 1`

5 goes into 11 only twice, for a total of 10.
11 minus 10 leaves a remainder of 1

7) What is `14 % 3` ?
  `=> 2`


8) A wizard carries two numbers (one even and one odd)
in each hand. He won't open his hands to show you, but
he will let you use modulo. Your task is to find out
which hand holds an even number, and which holds the odd.


If we mark each number as "X" we can use modulo:
if `x % 2 == 0` is `true`, it’s an even number.
if `x % 2 == 0` is `false`, it’s an odd number.

<br />
__Chapter 3 - Strings__


1) puts "What is the result" + " of " + "this operation?"
What is the return result of this operation?
  `=> nil`

The above puts method concatenated the strings, putting
the result to the screen and returning nil.

2) "This string minus" - "That string"
```ruby
NoMethodError: undefined method `-' for
"This string minus":String
```

There is no '-' method for Strings, so the operation
cannot be done. Remember, `-` is for numbers!

3) `"1234.55".to_i`
  `=> 1234`

4) `"1234.55".to_f`
  `=> 1234.55`

5) `"Not a number".to_i`
  `=> 0`

6) `puts "1\n2\n3\n"`
  ```ruby
  1
  2
  3
  => nil
  ```

7) Why might it be useful that the 'to integer' (to_i)
method return zero on strings that can’t be represented
as numbers?

"to_i" can still be called on a string without numbers,
and so it returns a zero, noting the successful call
(no error) and the value zero, which could represent
zero numbers in the string.

8) What do you think the length method does?
`"Count".length`
  `=> 5`
Counts the number of letters or items in the string.

9) How about the split method?
`"Count".split("")`
  `=> ["C", "o", "u", "n", "t"]`

Calling the 'split' method with no space ("") as the
argument causes the string to be split at each character
and placed inside of an array.

10) What do you think slice does?
`"Count".slice(2)`
  `=> "u"`

Slice grabs the character from the index argument
passed in, which in this case is an index of 2. The
letter "u" is at index 2 in our string "Count".
string:  ["C", "o", "u", "n", "t"]
indexes: [ 0 ,  1 ,  2 ,  3 ,  4 ]


<br />
__Chapter 4 - Variables__


1) Store the value of 54 / 3 into the variable x. What
is the value of x?
  `x = 54 / 3`
  `=> 18`

2) Give the value of x (from problem 1) to y, a new
variable. Now make x equal to itself divided by 3. What’s
the value of x? What’s the value of y?
  ```ruby
  y = x
  => 18  # y is assigned the x value, 18
  x = x / 3   # or written as x /= 3
  => 6   # x is now the value of 18 / 3
  ```

3) What if we performed some math on our variables?
If we set x to 12, what’s x divided by 3?
  ```ruby
  x = 12
  x / 3
  => 4
  ```

4) What’s the value of x now?
  `=> 12`
  When we divided X by 3, we didn't store the result, so X's value does not change since it was assigned 12.


<br />
__Chapter 5 - If and Else__


1) Is `3 > 5` ?
  `=> false`

2) `3 < 5`
  `=> true`

3) `5 == 5`
  `=> true`

4) `10 >= 10`
  `=> true`

5) `10 <= 12`
  `=> true`

6) `10 != 10`
  `=> false`

7) `10.object_id == 10.object_id`
  `=> true`

What about strings?
8) `"dog" == "cat"`
  `=> false`

9) `"cat" == "cat"`
  `=> true`

10)
  ```ruby
  "cat".object_id == "cat".object_id
  => false
  # Numbers have object id's that don't change.
  ```
Everytime a string is created, however, a new `object_id` is created for that string.

<br />
__Chapter 6 - Loops__


1) What’s the current value of the time variable?
`=> 8`

Even though our last value outputted was 7, the next
code block (current_time = current_time + 1) is executed,
and so our variable increments by 1 to equal 8.

<br />
__Chapter 7 - Collections__


1) Create a hash for the Wizard’s magic bag. Inside the
bag, we’ll put 3 frogs, 5 herbs, and 10 scrolls. Assign
the hash to the variable "bag".
What does your hash look like?

  ```ruby
  bag = {
    "frogs" => 3,
    "herbs" => 5,
    "scrolls" => 10
  }
  ```

2) Remember, hashes consist of key value pairs of any
data, not just numbers. Let’s add a wizard’s spell and
its result (which the wizard can never seem to remember).
Add a spell to our wizard’s bag with the key: "shazam"
and the value "turns subject into a frog".
Now what's in our bag?

  ```ruby
  bag["shazam"] = "turns subject into a frog"
  bag
  => {"frogs" => 3,
      "herbs" => 5,
      "scrolls" => 10,
      "shazam" => "turns subject into a frog"}
  ```

3) Our wizard has a change of heart and decides he never
wants to turn anyone into a frog. How can we remove the
spell "shazam" from our wizard bag?

  ```ruby
  bag.delete("shazam")
  => "turns subject into a frog"
  ```

4) Our wizard has recently acquired 3 different types of
potions. 4 orange potions, 5 blue potions and 7 red
potions. How might we add another hash of potions to our
bag?
Hint: remember that we can have collections within a
collection.

  ```ruby
  bag["potions"] = {
    "orange" => 4,
    "blue" => 5,
    "red" => 10
  }

  bag
  => { "frogs"=>3, "herbs"=>5,
       "scrolls"=>10,
       "potions"=> {
         "orange"=>3,
         "blue"=>5,
         "red"=>10
        }
     }
  ```

5) Now that our bag has four keys (frogs, herbs, scrolls
and potions), we can use these keys to access our data.
In order to make a new spell, our wizard needs 2 frogs,
3 herbs, 1 scroll and 2 blue potions. How can we remove
these items from our hash?
Hint: We can set the value of a key item to itself, minus
how many items removed.

  ```ruby
  bag["frogs"] = bag["frogs"] - 2
  => 1
  bag["herbs"] = bag["herbs"] - 3
  => 2
  bag["scrolls"] = bag["scrolls"] - 1
  => 9
  bag["potions"]["blue"] = bag["potions"]["blue"] - 2
  => 3
  bag
  => {
    "frogs" => 1,
    "herbs" => 2,
    "scrolls" => 9,
    "potions" => {
      "orange" => 4,
      "blue" => 3,
      "red" => 10
      }
    }
  ```

<br />
__Chapter 8 - Methods__


1) What is the name of the method below?
  ```ruby
   def multiply(num1,num2)
     num1 * num2
   end
  => multiply
  ```

2) How many arguments does this method have?
  ```ruby
  def meeting(place, time, day)
    ...
  end
  => 3
  ```

3) What does this method return when called?
(What's its output?)
  ```ruby
  def calculus
    numbers = (25 * 37) / 42
    numbers / 12 * 25
    "Programming is not math"
  end
  => "Programming is not math"
  ```
Ruby methods return their last line by default

4) Write a method that takes a word as an argument.
Make the method return the word and the string "is awesome!".

  ```ruby
  def awesomify(word)
    word + " is awesome!"
  end
  ```


<br />
__Chapter 9 - Enumerables__


1) What numbers will the following code output?
  ```ruby
     [1,2,3,4,5].each { |num| puts num if num.odd? }
  1
  3
  5
  => [1, 2, 3, 4, 5]
  ```

2) What would this each method output from this string?
  ```ruby
  "ThisdmakesdmoredsensedwithoutdD's".split("d").each {
    |letter| puts letter
  }

  This
  makes
  more
  sense
  without
  D's
  => ["This", "makes", "more", "sense", "without", "D's"]
  ```

3) What does select do for this hash?
  ```ruby
     food = {
       "apple" => "fruit",
       "carrot" => "vegetable",
       "tomato" => "fruit"
     }
     food.select do |item, category|
        category == "vegetable"
     end
  => {"carrot"=>"vegetable"}
  ```

4) What will map do?
  ```ruby
     numbers = [1,2,3,4,5]
     numbers.map { |num| num * 5 }
  => [5, 10, 15, 20, 25]
  ```

5) Now what is the value of numbers?
  ```ruby
  => [1, 2, 3, 4, 5]
  ```

