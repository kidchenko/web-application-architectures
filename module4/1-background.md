# The Ruby Programming Language Background

### Ruby programming language
- Rails was built using the Ruby programming language
- Ruby code shows up in models:
```ruby
class Post < ActiveRecord::Base
end
```

### History
- Ruby was created by Yukihiro Matsumoto (Matz) in yhe mid-1990s
> I wanted a scripting language that more powerful than Perl, and more OO than Python. That's why I decided to design my own language.
- Matz developed Ruby with a focus on the programmer, rather than the machine. The design goal was to maximize programmer efficient.
> I hope see Ruby help everyone programmer in the world to be productive, and to enjoy programming, and to be happy. That is the primary purpose of Ruby language

### Ruby Design
- Matz's guiding philosophy for Ruby
  - Ruby is designed to make programmers happy
- Ruby is designed according to the **Principle of Least Astonishment' - the language should behave in a way that minimizes the confusion of experienced programmers (assuming you are experienced in Ruby, not operating with some other programming model in mind)
- Ruby is a OO interpreted scripting language - many find it intuitive, flexible and extensible

### Ruby Installation

- Check Ruby version `$ ruby --version`
- Ruby gems is a package management system. To see the gems you have installed, use: `$ gem list`
- Rails is a Ruby gem for building database-intensive web application frameworks. To install, use: `$ gem install rails`

### The Ruby Interpreter
- You place your code in a file, with a .rb extension. And tell the interpreter to execute it using: `ruby hello.rb`
- Interactive Ruby Shell (IRB) is a interpreter shell that allows you to execute Ruby code from a command prompt - a REPL
- To open a Ruby shell, type: `$ irb`
- You can invoke IRB from the root of a Rails application directory as follows: `$ rails console`
- You can directly manipulate your rails application from the console command line - add/delete  database items
- This is a very useful. and common, way to debug Rails applications

### Language Features
- Ruby is a multi-paradigm programming language
  - Scripting - it can be used to write script that automate the execution of tasks
  - Imperative/Procedural - it has the traditional control structures found in imperative programs
  - OO - everthing is an object, derived from the **Object** class
  - Functional - computation proceeds via the evaluation of functions that depend only on their input, not the program state
