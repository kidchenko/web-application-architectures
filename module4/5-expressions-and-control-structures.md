# Expressions and Control Structure

### Expressions
- The ruby syntax is expression-oriented
- Everything in Ruby is treated as an expression and therefore evaluates to something
  - Control structures for conditional execution or looping, wich would be treated as statement in other languages, are treated as expression in Ruby
- In Ruby, if, case and for structure return the value of the last expression evaluated within the structure

### Conditional Structure
```ruby
if expression1
   code
elsif expression2
  code
else
  code
end
```
- There is a shortcut way of expressing if
```ruby
code if expresion
```
- Ruby also has a `?:` operator, as in C/C++
- Comparison operators `==`, `!=`, `=~`, `!~`, `===`
- There is a `case` structure in Ruby, `===` is the case-equality operator
- Ruby have the `until` statement that is equals `if` statement
```ruby
until expression
  code
end
```
- You cannot attach `else` cause in `until` expression

### Iteration
```ruby
for var in collection do
  code
end
```
```ruby
while condition do
  code
end
```
- `until` condition is same to `while`
```ruby
until condition do
  code
end
```
