__Practice__

Let’s pretend we’re at the beach, patiently waiting for our wizard to arrive at sunset. Upon every hour we check to see if our wizard has arrived. We could represent this as a piece of code. More specifically, we could write this as a while loop. Let’s assume the sun sets around 7pm, and we start waiting on the beach at 5pm.

```ruby
sunset = 7
current_time = 5
```

We create a variable called sunset and give it the value 7. We do the same for current_time and set it to 5.

```ruby
while current_time <= sunset do
  puts "Still waiting for the wizard."
  puts "It’s now #{current_time} o’clock"
  current_time = current_time + 1
end
puts "The wizard has arrived!"
```

This while loop would result in this output:

```
Still waiting for the wizard. It’s now 5 o’clock
Still waiting for the wizard. It’s now 6 o’clock
Still waiting for the wizard. It’s now 7 o’clock
The wizard has arrived!
```

1) What’s the current value of the current_time variable?

