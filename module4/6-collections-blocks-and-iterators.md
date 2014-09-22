# Collections, Blocks and Iterators

### Collections
- Ruby contains a number of collection classes
- The most important classes are `Array`and `Hash`. In addition a `Set` class was recently added to the language
- Each of these class includes the `Enumerable` module as a mixin. Thus, they share a common methods provided by `Enumerable`
- The `Enumerable` module provides `iterator` methods that can be used to iterate through (and operate on) each element in an collection
- Arrays are used extensively in Rails controllers
```ruby
def index
  @posts = Post.all
end
```

### Arrays
- Arrays are collection of objects, that can be indexed
- In ruby you can store different types in same array
- A wide variety of methods are provided by Array class: sort, inclue?, reverse, length, first, last, <<, push, pop, etc...
- Arrays can be slice `a[0..3] # get the 0 until 3 positions of array`
- Negative index `a[-1] # the last position of array`

### Hashes
- A hash is an associative array (key-value pairs) where the key and value may be any object, separated by `=>`.You index into a hash using keys
```ruby
phone = {'home' => 1, 'mobile' => 2, 'work'=> 3 }
# or better yet:
phone = {:home => 1, :mobile => 2, :work => 3 } # using symbols
```

### Code Blocks

- A `block` consist of multiple lines of code, enclosed in curly braces, that can be passed as a parameter to a method
- Using this feature it is easy to build code libraries wich can delegate varying functionality to code blocks be build later
- **Important** A block may appear only in the source if it is adjacent to method call (on the same line as the method call is last parameter)
```ruby
def three_times
  yield
  yield
  yield
end
three_times { puts "Hello"} # will print Hello three times
```

### Iterators
- In ruby, the various loop structures are rarely used - it is more common to use iterators
- The defining feature of an iterator method is that is invokes a block of code, applying it to each element in an collection
- A collection class that includes the Enumerable module is required to supply an `each` method. This method must yield the successive members of the collection
- Iterators work because you can pass parameters into blocks
```ruby
# The each method in the Enumerable modules works something like this
def each
  for item in collection # pseudo code
    yield (item)
  end
end
a = [1, 2, 3]
a.each {|element| puts element}
# => 1
# => 2
# => 3
```
