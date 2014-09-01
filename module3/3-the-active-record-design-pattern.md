#The Active Record Design Pattern

###Active Record Design Pattern
- The Active Record design pattern was named by Martin Fowler in 2003 in his book Patterns of Enterprise Application Architecture
- Commonly used in Ruby as a means of persisting data
- It is used to access data stored in relational databases
- Most software applications today are written usgin some OO language, and it is necessary ti persist the objects associated with these applications
- There is a big problem: The classes and objects associated with an OO language are incompatible with the structure of relational databases.
- Active Records to the Rescue: This design pattern encapsulates that notion an object-relational mapping, a mapping between OO languages and relational databases.
- The ORM provided by Active Records automatically converts object into constructs that can be stored in a database
- This creates in effect, a "virtual object database" that can be used from within an OO language

###ORM

|OO Language|Relational DB|
|---        |---|
|Classes    |Tables|
|Objects    |Records (Rows in a Table)|
|Attributes |Record Values (Columns in a Table)|

###Active Records in Ruby
- The Active Record design pattern is provided in a Ruby module called ActiveRecord
- Using the functionality provided by this module you can
  - Establish a connection to a database
  - Create database tables
  - Specify associations between tables that correspond to associations between the Ruby classes
  - Establish an ORM between Ruby and Databases
  - Perform CRUD operations on Ruby ActiveRecord objects


###Active Records in Rails
- The ActiveRecord module is built into Rails - the functionalities above are utilized when you create a Rails app and run scaffold and model generators
- The `ActiveRecord::Base.establish_connection` method uses the information in `./config/database.yml` in order to connect a Rails application to a database
- The `ActiveRecord::Migration` object is used to incrementally envolve your database over time
- The `ActiveRecord::Schema.define` method, in `./db/schema.rb` is created by inspecting the database and then expressing its structure programmatically using a portable (database-independent) DSL. This can be loaded into any database that ActiveRecord supports.

###The ActiveRecordModule
- If you create a new class by inheriting `ActiveRecord::Base`, and call it Post, it is assumed a database table will exist that is called posts. it pluaralizes the name of the class, and then looks for a table with that name.
- The `Base` class in the ActiveRecord module will inspect the posts database, and determine that it has title and body, and it will automatically add member variables (and accessors) with these same names in the Post class
- Furthermore, a query interface is also provided - in most cases, ActiveRecord insulates you from the need to use SQL
  - Post.all
  - Post.first
  - Post.find_by
  - Post.find_by_title

###The Interactive Ruby Shell
- The interactive Ruby Shell (IRB) is an interpreter that is provided with Ruby, and allows for real-time experimentation through interactive sessions - great for debugging `$ irb`
- The Rails console allows you to interact with Rails application through the IRB command line, it starts IRB and loads the Rails environment. To use it, from the root of a Rails application directory type: `$ rails console`
