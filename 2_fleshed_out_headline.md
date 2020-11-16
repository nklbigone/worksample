# UNDERSTAND RAILS

## Course objectives

This is a course meant to give you the basics of Rails with the assumption that you'll use the resources provided for further learning.
It assumes you are familiar with basic programming concepts and the basics of object oriented programming.

# Introduction to rails

## What is Ruby on Rails & Why Is It Useful?

It is an open-source framework with an object-oriented programming (OOP) structure, known as an efficient web development tool. It has a multi-layered functional structure with the Model, View, and Controller components similar to those of many other web development frameworks. It is well known for its speed in the development process. Besides, excellent serve performance can be achieved by using Ruby on Rails.

Ruby on Rails is the most popular open-source web application framework which built with the Ruby programming language.
You can use Rails to help you build applications, from simple to complex, there is no limits to what you can accomplish using Rails!

## What is a framework?

A framework is a collection of code, tools & utilities that give you a specific structure to work with when you’re writing software.

## What Does Rails Do Exactly?

Ruby on Rails can do a bunch of amazing things. RoR has made coding much simpler for developers.
Rails is made from several components to facilitate Active Record helps you read, create & update records in your database without having to be a database genius.
While the routing mechanism allows you to easily map URLs (like /login) to specific actions.
If you had to code all of this from scratch, without a framework, it would be a MASSIVE amount of work.
But Rails handles all of these details for you.

## Ruby on Rails had made of big and complex Applications like:

Diveintocode.jp
Github
Shopify
Ask.fm
Twitch
Instacart
Zendesk
SoundCloud

## The Rails Philosophy

Ruby on Rails is an opinionated framework.
One of these opinions is that convention should be more important than configuration.

## simple assignment

1. what is rails philosphy why rails philosophy

## How does Rails fit in the big picture of a complete web application?

Rails receives requests, routes them to the appropriate action, which then interacts with the database (via ActiveRecord) to fulfill the request. Then it returns the results (HTML or JSON) back to the user.

## RAILS APPLICATIONS AND EXAMPLES

## Let's set up a local environment.

Run this command to verify which version of ruby you have in your loacal machine

`ruby -v`

you will see something like this

`ruby 3.0.0`
but the version may be defferent depend on which version installed in your local system.

Make sure that the version of ruby is 2.5 or 2.6 or higher.
(Since 2.6.1 seems to have reported a bug, let's use something else to make sure.)

Now let jump into rails installation

`gem install rails -v 6.0.3.4`

Although the version may be slightly different, there is no problem if rails-6.0.3.4 or more is installed.
To checkout which version of rails you running type this command rails -v

## simple assignment

1. install all environment needed to make rails running at your local machine

## Now let dive into rails

## Command Line Basics

There are a few commands that are absolutely critical to your everyday usage of Rails. In the order of how much you’ll probably use them are:

- rails console
- rails server
- rake
- rails generate
- rails dbconsole
- rails new app_name
  Let’s create a simple Rails application to step through each of these commands in context.

## rails new rails_sample

The first thing we’ll want to do is create a new Rails application by running the rails new command after installing Rails.

## rails server

The rails server command launches a small web server named WEBrick which comes bundled with Ruby. You’ll use this any time you want to access your application through a web browser.
With just three commands we whipped up a Rails server listening on port 3000. Go to your browser and open http://localhost:3000, you will see a basic Rails app running.

## rails generate

The rails generate command uses templates to create a whole lot of things. Running rails generate by itself gives a list of available generators:
Let’s make our own controller with the controller generator. But what command should we use? Let’s ask the generator:

All Rails console utilities have help text. As with most unix utilities, you can try adding --help or -h to the end, for example rails server --help.

- rails generate controller helloWorld hello

Check out the controller and modify it a little

## (in app/controllers/helloWorld_controller.rb):

```
 class HelloWorldController < ApplicationController

 def hello

 @message = "Hello, how are you today?"

 end

 end
```

Then the view, to display our message (in app/views/helloWorld/hello.html.erb):

```
 <h1>Hi there </h1>
<p><%= @message %></p>
```

## Fire up your server using rails server.

```
rails server

=> Booting WEBrick...
```

The URL will be http://localhost:3000/helloWorld/hello.

## simple assignment

1. create rails application and try to display record in terminal `hit use rails console to populate record in terminal`

#### Rails comes with a generator for data models too.

- For a list of available field types, refer to the API documentation for the column method for the TableDefinition class.

## rails console

The console command lets you interact with your Rails application from the command line. On the underside, rails console uses IRB, so if you’ve ever used it, you’ll be right at home. This is useful for testing out quick ideas with code and changing data server-side without touching the website.
You can also use the alias “c” to invoke the console: rails c.

## rails dbconsole

rails dbconsole figures out which database you’re using and drops you into whichever command line interface you would use with it (and figures out the command line parameters to give to it, too!). It supports MySQL, PostgreSQL, SQLite and SQLite3.
You can also use the alias “db” to invoke the dbconsole: rails db.

rails destroy
Think of destroy as the opposite of generate. It’ll figure out what generate did, and undo it.

You can also use the alias “d” to invoke the destroy command: rails d.

## Rake

Rake is Ruby Make, a standalone Ruby utility that replaces the Unix utility ‘make’, and uses a ‘Rakefile’ and .rake files to build up a list of tasks. In Rails, Rake is used for common administration tasks, especially sophisticated ones that build off of each other.

You can get a list of Rake tasks available to you, which will often depend on your current directory, by typing rake --tasks. Each task has a description, and should help you find the thing you need.

## Let's now jump into MVC structure.

## MVC

This time, you will learn about MVC , which is indispensable for developing applications with Rails.

In order to develop Web applications with Rails, it is necessary to develop it according to the development method prepared by Rails. (Although it is not definitely necessary to develop it to act in accordance, in that case the effect of using Rails will halve. )

## Therefore, you will learn about MVC.

You can see that some words you have not heard before are listed in the illustration. It may be difficult for now, but this is the whole picture of Rails.

MVC will appear several times in the future, but by the end you will need to become able to grasp it.

## Model

- In charge of business logic in the system
- Responsible for interacting with the database.
- When the model wants to work by the change of the internal state or the communication from the outside, it notifies that to the controller

## Controller

- It works by receiving notifications from models and views and giving instructions to both.
- In charge of procedure instruction to Model, acceptance of user input, alert and display of dialog

## View

- In charge of the display part.
- Responsible for sending input data to Controller, updating display, and generating HTML.

## simple assignment

1. make demo of 4 to 5 slides on about MVC and how it works

## Advantages

--Since the separation of each function is clear, independence of each is secured.
--It becomes easy to divide the labor in development.
--It is less susceptible to changes in other parts, as dependencies between components can be minimized.
--Reusability, maintainability, and extensibility increase.
--It is easy to get an estimate of work accurately.
--You can use multiple views for one model.

## Disadvantages

--Design and description are likely to be complicated.
--The more complex the feature, the more places need to change views and controllers for porting and replacement.
--Viewings and controllers are often closely coupled and dependent on the model.
--When acquiring view information, there are many places where you need to go through a controller, so it takes a long time to process.

## database

## What is a Database?

A database is a collection of related data which represents some aspect of the real world. A database system is designed to be built and populated with data for a certain task.

Since Rails cannot store data, you have to use a database to save data.
The tool to manage the database is called database management system. (Called DBMS) for this course we are going to use postgresql to connect Ruby on Rails with a database.
ActiveRecord is responsible for that, connecting database and Rails.

## what is ActiveRecord

Active Record connects classes to relational database tables to establish an almost zero-configuration persistence layer for applications. The library provides a base class that, when subclassed, sets up a mapping between the new class and an existing table in the database. In the context of an application, these classes are commonly referred to as models. Models can also be connected to other models; this is done by defining associations.

Active Record relies heavily on naming in that it uses class and association names to establish mappings between respective database tables and foreign key columns. Although these mappings can be defined explicitly, it's recommended to follow naming conventions, especially when getting started with the library.

https://edgeguides.rubyonrails.org/active_record_basics.html

In Rails, ActiveRecord is loaded by default, and you can use it from the beginning.
ActiveRecord provides connection between database and Rails, and its connection settings can be changed in config/database.yml.
https://diver.diveintocode.jp/curriculums/937

## now let us jump to how to create a database.

## run this command to create database rails db:create

Since a database is created, if you have not moved to the sample directory yet, let’s move it to the directory using the cd command.

Make sure you have two databases for development (name_of_created_database_development) and for testing (name_of_created_database_test).

now let us Flow how to create table

In Rails in particular, to create a table in ActiveRecord, you need to follow the steps below.
(Create a model and create a migration file)
Migrate
Look at db/schema.rb and check the table

## What is migrate

You have used commands such as CREATE TABLE to create tables in SQL.
Active Record uses a mechanism called migration to create a table.
First of all, in order to create a table using migration, it is necessary to create a migration file which is a blueprint for the table.

## Migration file

A migration file is a blueprint of a table written in Ruby. ActiveRecord creates a table based on this migration file.
For example, when you want to build a house (make a table), the blueprint of the house you want to build would be the migration file.
If there is no blueprint (migration file), the house (table) can not be built.

## Benefits of using migration

What are the advantages of migrating and creating tables without directly executing SQL?

## Active Record migration Rails Guide

It is not necessary to write SQL.
Since it can be described by Ruby, it is less dependent on the type of database. (Please check the following article for the difference depending on the type of database.)
Since you need to create a migration file each time you add a table or add a column, you can refer to the itinerary of the database with a migration file.
Let's understand two points in order to operate the migration file correctly
Create a new migration file when adding, deleting, or updating a table

Add table
Delete table
Add columns in table
Delete a column in the table
Whenever you want to change the column in the table, create a new migration file each time.

If you created a migration file, execute the migration command

`rails db:migrate`

rails db:migrate is a command to execute migration files and manipulate DB tables.
Note that the difference between rails g migration and​ ​is a bit confusing.

rails g migration is a command to create a Ruby file called migration file.

rails db: migrate is a command to read newly created migration file and execute the command described there (such as ”Please create a new table“) to DB.

In other words, the order of processing is as follows.

## Run rails g migration

Migration file (plan) written in Ruby file is created
The engineer writes an instruction such as “Please create a table like this” in the migration file
Run rails db: migrate
Rails reads the instructions written in the migration file and the instructions are translated into SQL and executed in DB
(An entity is created from a design drawing)

In addition, the operation of migration files requires special attention when developing a team.
When someone in the team creates or migrates a migration file to change a table, other members also need to migrate as well.

Now let's check the operation of the migration file using a concrete example.

## case Deleting the migration file trying to delete the column

For example, if you are developing as a team, you think that you need a column named title in the Blogs table, and created and migrated a migration file that adds a title column.
However, another member thought that the title column was not necessary, and edited the migration file to which the title column was added.
the team member deleted the title column by re-executing all migration files from the beginning.

## To be able to create apps with CRUD functions in Rails.

## create_table

The create_table method is a method for creating a table as its name shows.

You can create table with command create_table : Table name
It is usual to add the columns you want to create in the table in the create_table block, as follows.

## What is RESTful?

RESTful is one of the types of program call conventions (APIs) for using the Web system externally.
Also, REST is a model of design that sends and receives data by accessing URL through HTTP method (GET, POST, PATCH, DELETE).
For example, to explain the previously defined routing,
`get'/blogs', to:'blogs#index'`

## Use the resources method to define frequently used RESTful routes.

```
resources :blogs
blogs GET /blogs(.:format) blogs#index
 POST /blogs(.:format) blogs#create
new_blog GET /blogs/new(.:format) blogs#new
edit_blog GET /blogs/:id/edit(.:format) blogs#edit
blog GET /blogs/:id(.:format) blogs#show
PATCH /blogs/:id(.:format) blogs#update
PUT /blogs/:id(.:format) blogs#update
DELETE /blogs/:id(.:format) blogs#destroy
```

## let us jump to the routing

## what is routing?

The routing module provides URL rewriting in native Ruby. It's a way to redirect incoming requests to controllers and actions. It replaces the mod_rewrite rules. Best of all, Rails' Routing works with any web server. Routes are defined in app/config/routes.rb.
Think of creating routes as drawing a map for your requests. The map tells them where to go based on some predefined pattern

```
Rails.application.routes.draw do
resources :blogs
end
```

## resources

By using the resources method, seven routings along RESTful are generated.
Let's run the rails routes command at the terminal and check it.

```
/workspace/sample (master) $ rails routes
Prefix Verb URI Pattern Controller#Action
 blogs GET /blogs(.:format) blogs#index
POST /blogs(.:format) blogs#create
new_blog GET /blogs/new(.:format) blogs#new
edit_blog GET /blogs/:id/edit(.:format) blogs#edit
blog GET /blogs/:id(.:format) blogs#show
PATCH /blogs/:id(.:format) blogs#update
PUT /blogs/:id(.:format) blogs#update
DELETE /blogs/:id(.:format) blogs#destroy
```

now we are having batch of routing here

Now we implemented the routing that is necessary for the CRUD function of the blog.

## Controller

```
class BlogsController < ApplicationController
def index
 end
# Add
 def new
 end
end
```

## Create View

Next, edit the View.
First let's create a view.
If BlogsController's new action (method) is called, blogs/new.html.erb is originally called in View, so create a blogs/new.html.erb .

## form_with

You created the file, so now you are going to create the form, but since you create the form associated with the model, the form_with method is very useful.
`<%= form_with(model: Blog.new) %>`
form_with makes it easy to create forms.
View Helper
form_with is a type of view helper.
The view helper is a method for generating HTML, provided in Rails.
For example, form_with makes creating forms easier.
For example, the following HTML,

## now let us create view helper.

```
<%= form_with(model: Blog.new) do |form| %>
<div class="blog_title">
 <%= form.label :title %>
<%= form.text_field :title %>
</div>
<div class="blog_title">
 <%= form.label :content %>
 <%= form.text_field :content %>
</div>
<%= form.submit %>
<% end %>
```

## So now let us make CRUD on ruby on rails

as we tolked about priviously we controller is the one in charge of logic.
then we are going to give controller the logic of making CRUD for us

## move to app/controllers/blogs_controller.rb

```
class BlogsController < ApplicationController
def index
@blogs = Blog.al
end
def new
@blog = Blog.new
end def create Blog.create(blog_params)
redirect_to new_blog_path
end
private
def blog_params params.require(:blog).permit(:title, :content)
end
end
```

## move to views/blogs/index.html.erb

```<h1>List of blogs</h1>

<table>
<tr>
<th>Title</th>
<th>Content</th></th>
</tr>
<% @blogs.each do |blog| %>
 <tr>
 <td><%= blog.title %></td>
 <td><%= blog.content %></td>
</tr>
<% end %>
</table>
<%= link_to 'Return to blog list page', blogs_path %>
```

## Simple assignment

### 1 make slide of 6 to 8 of demo with functionalty rails gem scaffold and devise

reference https://www.rubyguides.com/2020/03/rails-scaffolding/
reference https://hackernoon.com/using-devise-in-your-ruby-on-rails-application-a-step-by-step-guide-m92i3y5s

### 2 create new blog with admin users functionalities

reference https://github.com/sferik/rails_admin
