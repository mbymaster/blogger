
     ,-----.,--.                  ,--. ,---.   ,--.,------.  ,------.
    '  .--./|  | ,---. ,--.,--. ,-|  || o   \  |  ||  .-.  \ |  .---'
    |  |    |  || .-. ||  ||  |' .-. |`..'  |  |  ||  |  \  :|  `--, 
    '  '--'\|  |' '-' ''  ''  '\ `-' | .'  /   |  ||  '--'  /|  `---.
     `-----'`--' `---'  `----'  `---'  `--'    `--'`-------' `------'
    ----------------------------------------------------------------- 


Welcome to your Rails project on Cloud9 IDE!

To get started, just do the following:

1. Run the project with the "Run Project" button in the menu bar on top of the IDE.
2. Preview your new app by clicking on the URL that appears in the Run panel below (https://blogger-2-anacrust.c9users.io/).

Happy coding!
The Cloud9 IDE team


## Support & Documentation

Visit http://docs.c9.io for support, or to learn more about using Cloud9 IDE. 
To watch some training videos, visit http://www.youtube.com/user/c9ide

Notes:
$ rails new blogger
  The generator has created a Rails application for you. Let’s figure out what’s in there. Looking at the project root, we have these folders:
  -app - This is where 98% of your effort will go. It contains subfolders which will hold most of the code you write including Models, Controllers, Views, Helpers, JavaScript, etc.
  -bin - This is where your app’s executables are stored: bundle, rails, rake, and spring.
  -config - Control the environment settings for your application. It also includes the initializers subfolder which holds items to be run on startup.
  -db - Will eventually have a migrations subfolder where your migrations, used to structure the database, will be stored. When using SQLite3, as is the Rails default, the database file will also be stored in this folder.
  -lib - This folder is to store code you control that is reusable outside the project.
  -log - Log files, one for each environment (development, test, production)
  -public - Static files can be stored and accessed from here, but all the interesting things (JavaScript, Images, CSS) have been moved up to app since Rails 3.1
  -test - If your project is using the default Test::Unit testing library, the tests will live here
  -tmp - Temporary cached files
  -vendor - Infrequently used, this folder is to store code you do not control. With Bundler and Rubygems, we generally don’t need anything in here during development.

$ bin/rails console   #to get to the console

$ bin/rails server  #to get the server going

$ bin/rails generate model Article
  We’re running the generate script, telling it to create a model, and naming that model Article. From that information, Rails creates the following files:
  -db/migrate/(some_time_stamp)_create_articles.rb : A database migration to create the articles table
  -app/models/article.rb : The file that will hold the model code
  -test/models/article_test.rb : A file to hold unit tests for Article
  -test/fixtures/articles.yml : A fixtures file to assist with unit testing

#After editing the db/migrate/(some_time_stamp)_create_articles.rb to add your model fields
$ bin/rake db:migrate
  
$ bin/rails generate controller articles
  The output shows that the generator created several files/folders for you:
  -app/controllers/articles_controller.rb : The controller file itself
  -app/views/articles : The directory to contain the controller’s view templates
  -test/controllers/articles_controller_test.rb : The controller’s unit tests file
  -app/helpers/articles_helper.rb : A helper file to assist with the views (discussed later)
  -test/helpers/articles_helper_test.rb : The helper’s unit test file
  -app/assets/javascripts/articles.js.coffee : A CoffeeScript file for this controller
  -app/assets/stylesheets/articles.css.scss : An SCSS stylesheet for this controller

$ bin/rake routes #shows all the IP routes