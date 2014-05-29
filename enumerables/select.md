
##Select

Okay, that might have been a little complicated to understand, but trust us, it will get easier with a little practice. Let’s look at the select method to see how it iterates (looks over the stuff) in a collection. Select works by looking at the block of code passed in, and then only returns the element if the block evaluates to be true.

```ruby
 $ [1,2,3,4].select { false }
=> []

 $ [1,2,3,4].select { true }
=> [1, 2, 3, 4]
```

In the above example, the `select` method looks at each element in the array (1,2,3 and 4) and _returns_ that element if our block of code is true. Since our block of code is the _false_ boolean, the select method does not evaluate to true and returns nothing but an empty array. In the next line we pass `true` to the block and the select method returns every item in the array.

Here’s an example of how we might use the select method in a more useful way. Imagine you have a collection of test scores and you want to select only those scores above 80 points.

```ruby
test_scores = [23,80,34,99,54,82,95,78,85]
test_scores.select do |score|
  score > 80
end
=> [99, 82, 95, 85]
```

Here we use select to look at each element in the array. This value will be temporarily stored in the `score` variable. Then each particular score is checked to see if it is greater than 80. Each of the scores that are greater than 80 will be collected and returned as an array.

```ruby
test_results = {
  "Bobby" => 80, "Jane" => 95,
  "Adam" => 99, "Doug" => 65,
  "Sue" => 89, "Kim" => 91
}

good_students = test_results.select do |student, score|
  score > 80
end
```

Here we have a test\_results hash that contains a student’s name and their test score. We can use the select method to grab each student and their score, for every student that scored higher than 80 points. If we were to run this, our good\_students hash would look like this:

```ruby
$ good_students
=> {"Jane"=>95, "Adam"=>99, "Sue"=>89, "Kim"=>91}
```

You can imagine a program that runs simple select methods for hundreds of students in many classes in order to group students by their grades. Ruby is useful for sorting, counting, classifying and organizing data. It would take a person many hours to organize hundreds of students by grade and name, but a good program can do it almost instantly!

<div style="height:30px;"></div>
