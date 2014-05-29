
##Each\_with\_index

This enumerable method works much like each, except that it captures the index of the specific array its called on as well. Remember that an array is an ordered collection that uses an index (sorting system) to organize the data or information in the array. An array with five items has five indexes, from 0 to 4, and each index notes the location of each element.

```ruby
my_array = ['ball', 'bat', 'hat']
my_array[2]
=> hat

my_array[0]
=> ball
```

In the example above, each item in the my\_array can be called by its index. The ball is located at index 0, the bat at index 1, and our hat at index 2. If we only want to print every other item, we might use the each\_with\_index method like this:

```ruby
my_array = ['ball', 'bat', 'hat', 'uniform', 'shoes']
my_array.each_with_index do |item, index|
  if index % 2 == 0
    puts item
  end
end
```

Remember that a modulo is a way of looking at the remainder (left over part) of a number. So here, we put the item to the screen if the index of the item has a remainder of zero when divided by 2. Since the indexes 0, 2, and 4 give no remainder when divided by 2, we only call the puts method on items at these particular indexes.

We could use the `even?` method and curly braces to simplify our enumerable method.

```ruby
my_array.each_with_index do |item, index|
  puts item if index.even?
end

ball    #item at index 0
hat     #item at index 2
shoes   #item at index 4
```

Ruby's `even?` method allows us to skip the modulo part altogether. `Even?` will return true if the number it is called upon is an even number. Here is a way to see how the computer executes (carries out) each step in the each\_with\_index method.

```ruby
my_array = ['ball', 'bat', 'hat', 'uniform', 'shoes']
my_array.each_with_index do |item, index|
  puts item if index.even?
end

|'ball', 0| if 0 is even?, then puts 'ball'
true => puts 'ball'

|'bat', 1| if 1 is even?, then puts 'bat'
false

|'hat', 2| if 2 is even?, then puts 'hat'
true => puts 'hat'

|'uniform', 3| if 3 is even?, then puts 'uniform'
false

|'shoes', 4| if 4 is even?, then puts 'shoes'
true => puts 'shoes'

```

The method starts out with an item and its index from the array. It then performs the block of code we specified between the `do` and `end` wrappers. In this example it will only put the name of the item if the index is an even number. Otherwise, the if statement will return false and Ruby will not put anything to the screen for that particular block of code.

<div style="height:30px;"></div>
