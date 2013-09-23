# Variables & Methods
There are some very fundamental concepts used throughout each and every programming language. Hopefully this lesson will help you grasp the first of these concepts.

## Variables
Think of variables as buckets that we can create to *store* information. We can call them whatever we like but it is best to follow a few rules. Ruby makes declaring and using variables extremely easy. The pattern looks like the following:

    variable_name = value

So let's look at some very simple examples of variable usage...

```ruby
tax   = 0.2
price = 100
total = price + (price * tax) # => 120
```

Using variables means we can then just a single value and that will propagate everywhere that we use the variable.

```ruby
tax   = 0.4 # changed from 0.2 to 0.4
price = 100
total = price + (price * tax) # => 140
```

Variables can store all sorts of data but making our code easy to maintain doesn't just stop at using meaningful variable names. If we knew that we would want to calculate the total price for different things in multiple places we can extract this calculation into what is known as a method.

## Methods
Methods allow us to group multiple lines of code so we can use it later without having to duplicate our work. Following on from the previous example let's create a method to calculate the total price.

The pattern for declaring a method is like the following:

```ruby
def method_name(first_argument, second_argument)
  # logic goes here
end
```

We can have multiple arguments which are values we can pass into the method. The names used in the parantheses (`(`, `)`) are the variable names that store the values passed to the method. This will become more apparant soon. These variables can then be used within the method.

So let's now create a method to calculate total price.

```ruby
def total_price(pre_tax_price)
  tax   = 0.2
  total = pre_tax_price + (pre_tax_price * tax)
end
```

Now it is important to understand that in ruby the last executed line of the method is returned to whatever called the method in the first place. So let's see how that can be used in our code...

```ruby
# define a total price method
def total_price(pre_tax_price)
  tax   = 0.2
  total = pre_tax_price + (pre_tax_price * tax)
end

# calculate the total price for some examples
total_price(100) # => 120
total_price(150) # => 180
total_price(200) # => 240
```

Awesome! So now we can generate a price what if we wanted to optionally override the tax for specific cases? We can easily do this by adding another argument (parameter) to the method. That would look like the following:

```ruby
# define a total price method
def total_price(pre_tax_price, tax = 0.2)
  total = pre_tax_price + (pre_tax_price * tax)
end

# calculate the total price for some examples
total_price(100)    # => 120
total_price(150)    # => 180
total_price(200, 0) # => 200
```

Notice how we can now remove the line where we set the value of the `tax` variable. This has moved into the arguments list. By using the `=` symbol in the arguments we are setting a *default* value which we can override as demonstrated in the examples.

That's the end of the first lesson. The next lesson we will cover a more complicated topic of Classes and Objects.
