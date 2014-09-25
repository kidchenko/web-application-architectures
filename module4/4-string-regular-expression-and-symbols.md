# String, Regular Expressions and

### Strings

- You can create strings using single or double quotes
  - double quotes can be interpoled
  ```ruby  
  "360 degrees=#{2*Math::PI} radians"
  ```
  - single backquotes (backticks) the string will be executed as a command in the underlying OS
  ```shell
  `date`
  # Dom 21 Set 2014 13:11:01 BRT
  ```
- Strings are mutable, as in C/C++, but unlike C#/Java. Thus each time Ruby encounters a new string literal, it create a new String object. I.e., if you are a creating a string literal within a loop, each iteration will create a new String object.
- The String class contains methods wich can be used to manipulate strings.
```ruby
name = "Homer Blimpson" # => Homer Blimpson
name.length # => 14
name[6] # => "B"
name[6..14] # => "Blimpson"
```

###Regular Expression Class

- A regular expression provides a concise and flexible means for matching strings of text
- In Ruby, a regular expression is written in the form of: `pattern/modifiers` where "pattern" is the regular expression itself, and "modifiers" are a series of characters indicating various options. The "modifiers" part is optional. The syntax is borrowed from Perl.
- To test if a particular Regex matches (part of) a string, use the `=˜` operator. This operator returns the caracter position in the string of the start the match (which evaluates to true in a boolean test), or nil if no match (wich evaluates to false)
```ruby
"Homer" =~ /er/ # => return 3
```

### Symbols

- Ruby symbols are also closely related to strings
- A Ruby interpreter maintains a symbol table where it store the names of all classes, methods and variables
- You can add your own symbol to this table. Specifically, a symbol is created if you precede a name with colon
```ruby
attr_reader :row, :col
```
- Ruby symbols are used to represet names an strings; however unlike String objects, symbols of the same name are initialized and exist in memory only once during a Ruby session
- Symbols are immutable, and cannot be modified during runtime
- There is a big space advantage associated with symbols, as each unique is only stored once in memory. Multiple strings with the same name can exist in memory
```ruby
puts :name.object_id # => yields 20488
puts :name.object_id # => yields 20488 the same object
puts "name".object_id # => yields 655433576
puts "name".object_id # => yields 334545321 differents objects
```
- When should you use a symbol and when should use a string?
  - If the contents (i.e., the sequence of characters) of the object is important, if you need manipulate these characters, use a string
  - If the identify of the object is important (in wich case you probably dont want to manipulate the characters), use a symbol
