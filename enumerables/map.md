
##Map

Last but not least, let’s check out the map method. So far we’ve seen how different methods affect elements from our collections. With map, we can select certain elements and modify them at the same time. Let’s jump into an example.

```ruby
["dog", "cat", "snake", "mouse"].map do |animal|
  animal.capitalize
end
=> ["Dog", "Cat", "Snake", "Mouse"]
```

Here we have an array of animals. We decide we want to capitalize each animal name. So we call map on the array and another built in Ruby method, `capitalize`, on each item in the array. The capitalize method takes a string and makes its first letter capitalized.

Cool, right? Map essentially finds and manipulates the data in the array, or maps your block of code to each specific element in that array. To permanently alter an array with the map feature in Ruby, simply add the exclamation point to modify the existing array.

```ruby
animals = ["dog","cat","snake","mouse"]
animals.map! { |animal| animal.capitalize }
=> ["Dog", "Cat", "Snake", "Mouse"]

animals
=> ["Dog", "Cat", "Snake", "Mouse"]
```

At this point you understand two fundamental collections in programming languages: arrays and hashes. After diving into the Enumerable module we revealed four of the most common methods used on these collections; each, each\_with\_index, select and map. Now it’s time to test your knowledge with a few more examples.

<div style="height:30px;"></div>
