# Using Classes & Objects
In the previous guide I covered some basics about what is a class and what is an object. Now we want to take the next step and look into how we use classes.

Classes don't just categorise the type of an object by giving it a name. They allow you to also group methods that can be performed on those objects. We'll use the Array class for all the examples in this guide. You can see the [complete method list for Array][array] on the ruby-doc site.

Methods can be called on objects by using the dot syntax (`.`). The dot indicates that anything following it is a method call for whatever the object is.

```ruby
my_list = [1, 2, 3]
my_list.count # => 3
my_list.first # => 1
my_list.last  # => 3
```

So the above example calls three methods on `my_list` (which is an Array). The methods are called `count`, `first` and `last`.

These methods work just like the others we learnt in the first lesson. This means we can pass information into certain methods. A good example of this is when we want to add something into the list.

```ruby
my_list = [1, 2, 3]
my_list.push(4) # => [1, 2, 3, 4]
my_list.push(5) # => [1, 2, 3, 4, 5]
my_list         # => [1, 2, 3, 4, 5]
```

As you can see we interact with them just like any other method.

[array]: http://www.ruby-doc.org/core/Array.html "Array RDoc"
