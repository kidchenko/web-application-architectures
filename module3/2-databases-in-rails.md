#Databases In Rails


###Database Migrations
- Each time we ran the scaffold generator in our blog application, Rails created a `database migration` file and placed it in the `db/migrate` directory
- Rails use the `rake` command to run these migrations
- Because migrations can also be used to undo the work of previous migrations, they are timestamped, and executed in order they were created

###Rails Environments

-Rails automatically sets up appliactions to run in one of three prebuilt enviroments (you can add your own)
  - Development - For the developing the application
  - Test - Used when your run tests
  - Production - Used when you deploy your application
- By default, when you run `$ rails server` Rails runs in the development environment
- To force rails run in a different environment, use `$ rails server -e <name>`
- In production mode, if you make a change in your source code, it is not reflected in the running application immediately. Another thing, Rails optimezes the delivery assets, for example CSS, HTML and JavaScript


One of the architectural elements most likely to differ between environments is the database
- During development, you (the developer) are the only one accescing the database
- Rails sets up the development environment to use SQLite
- The databases that Rails with use in diferrent environments is specified in: `db/database.yml`
