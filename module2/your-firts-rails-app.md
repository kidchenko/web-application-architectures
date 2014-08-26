#Your first rails app

Create new rails app
`$ rails new my_app`

Install modules
`$ bundle install`

In rails app, start a web server
`$ rails server`

```
Rails.root/ -> is the root of my application
├── app/    -> where model, view and controller code is stored
├── bin/    -> where helper scripts (bundle, rails, rake)
├── config/ -> where you set up the application (app, database e route configuration)
├── db/     -> where database schema and migrations
├── log/    -> where application log are created
├── public/ -> root of your web application (webroot)
├── test/   -> ALWAYS TEST YOUR CODE!
└── Gemfile -> specifies the required gems
```
