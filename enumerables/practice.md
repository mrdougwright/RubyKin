__Practice__


1) What numbers will the following code output?
   `[1,2,3,4,5].each { |num| puts num if num.odd? }`

2) What would this each method output from this string?
   ```ruby
     "ThisdmakesdmoredsensedwithoutdD's".split("d").each {
      |letter| puts letter
    }
   ```

   Note: We are method chaining in the above example.
   The string is being split into smaller separate
   strings at the parameter passed in. Then the each
   method is called on that array.

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
   ```

4) What will map do?
   ```ruby
   numbers = [1,2,3,4,5]
   numbers.map { |num| num * 5 }
   ```

5) Now what is the value of numbers?

