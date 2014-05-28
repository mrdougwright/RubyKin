
##Hash

The next type of collection in Ruby is the _Hash_. Sometimes called a dictionary, a hash is an unordered list of key value pairs. A hash is more like a messy room than an array, which is very organized. With a hash, our list of items come in pairs, placed in any order.

In hash collections, we use curly brackets `{ }` wrapped around pairs of information separated by a comma, `{ "like" => "this" }`. The item to the left of the arrow `=>` is the _key_ and its _value_ is the element on the right.

Hashes are extremely useful when we have multiple numbers of similar items in a list. For example, if you used a hash to organize your toy chest, it might look something like this:

```ruby
toy_chest = {
  "sea_monkeys" => 12,
  "dolls" => 5,
  "legos" => 514
}
```

Each of these items is located in our toy chest, and the number of them is represented in the hash. So we have three keys (sea_monkeys, dolls and legos) with their corresponding values (12, 5 and 514). To access information in this hash, we can use brackets like we did for arrays.

```ruby
toy_chest["sea_monkeys"]
=> 12

toy_chest["dolls"]
=> 5

toy_chest["legos"]
=> 514
```

To add an item to our toy chest hash, we can simply use brackets in a similar way that we did above to retrieve information.

```ruby
toy_chest["toy_cars"] = 7
=> 7

toy_chest
=> {"sea_monkeys" => 12, "dolls" => 5, "legos" => 514,
"toy_cars" => 7}
```

By writing "toy\_cars" in brackets next to toy_chest, we’ve actually called a method on our hash, giving it a new key value pair of `"toy_cars" => 7`. To remove an element, we can call the `delete` method. Don’t worry too much about methods right now, we just want to show you how easy it is to handle data in your array or hash collections.

```ruby
toy_chest.delete("sea_monkeys")
=> 12

toy_chest
=> {"dolls" => 5, "legos" => 514, "toy_cars" => 7}
```

There are several other ways to add, remove and manipulate data in our hash collection. But before we understand these methods, we need to learn about methods in general. Check out some examples of using a Hash below, and then, onward to the next chapter!
