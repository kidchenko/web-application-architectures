# Objects and Variables

### Objects

- **Everything in Ruby is an object**, the `Object` class is the parent of all classes in Ruby. It is methods are therefore avaliable to all objects unless explicitly overriden
- An important method in the `Object` class is `class()`. It return a type of an object
```ruby
> 1.class() # => Fixnum
> 1.class # => Fixnum parentheses are optional - they are commonly ommited
```
- Ruby is sensitive to the capitalization of identifiers, in most cases treating capitalized variables as constants

### Variables

- Ruby does not use variable declaration, if you assign a value of a literal, an 'appropriate' variable method after that literal is created. (similar to python)
- **Important**: all assignments are done by reference in Ruby
- Ruby support parallel assignment
```ruby
  a = 2
  b = 1
  puts a, b
  a, b = b, a
```
- Ruby uses simple naming conventions to denote the scope of variable:
  - `name` could be a local variable
  - `@nome` an a instance variable
  - `@@name` a class (static) variable
  - `$name` a global variable
The @ and $ sigils enhance readability by allowing the programmer to easily identify the roles of each variable
- Furthermore, local variables must begin with a lowercase letter, and the convention is to use underscores, rather than camel case, for multi-word names
- Constants are any name that starts with an uppercase letter, and the convention is to use underscore
- Classes and modules are treated as constants, so they begins with uppercase letters, and the convention is to use camel case
