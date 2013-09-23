# Learning Ruby
I've began compiling a collection of guides and lessons to help people learn how to program ruby. To get the most out of them however there are some tips.

## Formatting
Honestly, code is much easier to read and understand if you format your work correctly. The standard style for ruby is to indent nested code by 2 spaces. Try to follow this rule as it keeps things easy to follow.

```ruby
def method_name # not indented
  # example code, indented by 2 spaces
  # more code,    indented by 2 spaces
end             # not indented
```

In many of the examples you will see a `#` symbol. In ruby this is a comment. It means whatever on that line following the symbol is ignored but visible for us to see. It makes it easy to document within the code. I use a convention of using `# => value` to indicate what is returned by a particular line. To better see what I mean follow the instructions below.

## Testing the examples
All the code examples should work if followed correctly. In order to run the code yourself do the following:

1. Make sure you have ruby installed.
2. Create a file and make sure it has the `.rb` extension.
3. Put/type the code into the file. 
4. Save it!

Now you can run the following command in either a terminal or command prompt:

```bash
ruby path/to/example.rb
```

If you wish to output a result from some of the code simply append the line with `puts`. An example of this:

```ruby
example_one = 2       # not output
puts example_one * 2  # outputs 4
```

## Struggling to understand an example or lesson
Please post an issue on github explaining the difficulties you had. I will do my best to help.

## Contributing
This collection of guides, advice and lessons are intended to be free and open source. They should be available to anyone and therefore contributions are also welcome. Submit a pull request and I will gladly accept well written, working guides.

## License
In order to ensure that this guide remains free it is licensed under GPLv2. Any duplicates or references should also refer back to the original (https://github.com/FreakyDazio/learn-ruby).
