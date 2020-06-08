---
layout: post
title:      "Grocery List App"
date:       2020-06-08 01:49:06 +0000
permalink:  grocery_list_app
---


For my sinatra project I chose to make an applicaton that lets you create a grocery lists and save them to use again. I used the corneal gem to set up the basic structure of my application. Corneal is a ruby gem that sets up the folders gemfiles and everything else you need to start making your sinatra app. You can find the Corneal gem  [here](http://https://rubygems.org/gems/corneal/versions/0.1.0). 

Once I had the basic structure of my application set up I started with my sql tables. I created 2 migrations in the DB folder one creating the users table that stored the username and password_digest for sessions. Next I created the lists table that stored all of my data from the grocery list. 
```
class CreateUsersTable < ActiveRecord::Migration
    def change 
        create_table :users do |t|
            t.string :username 
            t.string :password_digest
        end
    end
end
```
```
class CreateListsTable < ActiveRecord::Migration
    def change 
        create_table :lists do |t|
            t.string :title
            t.string :list1
            t.string :list2
            t.string :list3
            t.string :list4
            t.string :list5
            t.string :list6
            t.string :list7
            t.string :list8
            t.string :list9
            t.string :list10
            t.integer :user_id
        end
    end
end
```

I set up a user and list controller to take care of the tasks of navigating the site. The user controller handled login and logout, and the list controller handled the creation, reading, updating, and deletion of lists, or my CRUD. 

When you first go to the homepage you are asked to sign up or login. Once you signup or login it creates a session id for you to stay logged in and redirects you to your userpage. From there you can create a new list, see all of your lists or logout.


