#Rails Phylosofy

####Based upon three principles

- Convention over Configuration - common aspects of a web app are provided (preconfigured) for you. Use this convention
- Don't Repeat Yourself (DRY) - every code should have a single, unambiguous representation within a system. Duplication of code throughout an application can lead to logical contractions, and in general make the application more difficult to maintain
- Agile development - Software development methodologies on iterative and incremental development.

##Convention over Configuration

- A massive numbers of "conventions" are built into Rails, and the real trick is learning all of them.
- Rails code generators follow specific naming conventions. If you use the scaffold (MVC) generator to create a Post, you get:
  - A class called Post will be created for the model, along a corresponding table in the database that will called posts
  - A `RESTfull` controller called posts_controller will be created, and routes will be set up so that specific urls will be able to perform CRUD operations on the post table
  - A posts `view` will be created, consisting of a set of `HTML` files that can be used to render the results of the CRUD operations
  - Test fixtures, along with unit, functional, integration and performance test suite are automatically generated

##DRY

- EVERY piece of information should have a single, unambiguous, authoritative representation within a system. In Rails with `ActiveRecords`, once a model is specified, you don't need to specify database column names - they are determined from the model
  - When applied successfully, a modification to a system element does not change any other logically-unrelated system element, while elements that are logically related all change predictably and uniformly, thereby keeping them in 'sync'
- This principle makes it easier to use code generators and automatic build system
- DRY code is typically created by data transformations and code generators, allowing the software developer to avoid copy and paste operations
- Following the DRY principle makes it easier to maintain large software systems


##Agile Development

- Rails was built agile development in mind:
  - A working application is available immediately
  - In development mode, there are no recompile, deploy, restart cycles. Rails does not generally require you to stop the server; changes made to the application will be automatically picked up the server
  - Rails have a simple tools to generate code quickly
  - Testing is built into the Rails framework
- Extreme Programming is an agile approach that centers around test-driven development (TDD). Behavior-driven development (BDD), a second generation agile approach, extends TDD by writing test cases in natural language that non-programmers can read. BDD focuses on obtaining a clear understanding of desired software behavior through discuss with stakeholders
  - RSpec and Cucumber are BDD tools for ruby that well will use
