# The Blog App - Iteration 2 (Associations)

### Associations in Rails

Because we used the sacffold generator for the posts and comments in our blog application, the Active Record design pattern is "pre-wired". This means
- A SQLlite database able to store post and comments was created when we ran the migrations
- A connection to this database was established (database.yml)
- The ORM for `Post` and `Comment` objects was set up - the M in MVC

However, there is one thing missing - we need to ensure that any comments entered for a particular post are permanently linked to that post

- We did make the association between posts and comments in the database - recall that a `post_id` can be stored with each comment
- To make our model in Rails fully functional we need to add associations - each post needs to know the list of comments associated with it, and each comment needs to know witch post it belongs to
- There is a many-to-one relationship between comments and posts - a post has many comments, and a comments belongs to a post.
- The ActiveRecord module contains a set of class methods for tying objects together through foreign keys
- To enable these, you must declare associations within your models using the following:

|Relationship |Model with no foreign key  |Model with foreign key |
|---          |---                        |---                    |
|one-to-one   |has_one                    |belongs_to             |
|many-to-one  |has_many                   |belongs_to             |
|many-to-many |has_and_belongs_to_many    |*

\* The foreign keys for each model are stored in a join table

```ruby
class Person < ActiveRecord::Base
 has_many :phones # dependent: :destroy
end

class Phone < ActiveRecord::Base
 belongs_to :person
end
```

`dependent: :destroy` - destroy in cascading, e.g., delete all of the comments that are dependent of a post

```ruby
 # routes.rb

 resources :comments

 # without association
 resources :posts
 # or
 # with association
 resources :posts do
   resources :comments
 end
```
