#Blog App - Specifications

- two types of user: blog administrator and blog users
- the blog administrator should be able to enter new postings
- users should be able to visit the blog site and enter comments about particular postings
- the blog administrator should be able modify/remove any posting or comment
- user should not be able to modify posting or other user's comments

###Steps
  - create a new rails app called blog
  ```
  $ rails new blog
  ```
  - use the scaffold generator to create the MVC components need for posts and comments
  ```
  $ rails generate scaffold post title:string body:text
  ```
  
  ```
  $ rails generate scaffold comment post_id:integer body:text
  ```
  - run `$ rake db:migrate` to create your database and your schema
  - if you run `$ rake routes` a list of all url routes for your applications
  - start rails server `$ rails server`


> CRUD operations is easy
