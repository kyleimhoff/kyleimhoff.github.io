---
layout: post
title:      "Game Reviews Rails Project"
date:       2020-11-15 23:28:10 +0000
permalink:  game_reviews_rails_project
---


For my rails final project I created an application that allows you to create and read reviews for your favorite games. I really enjoyed rails. This is a very powerful tool for creating web apps. With sinatra you had to set everything up manually which is fine for a smaller more barebones application. With Rails you have access to generators to get you up and running in no time. 

My biggest challenge on this project was getting Omniauth to work properly. I initially tried it with facebook and my `ENV[:FACEBOOK_ID` was returning nil. After hours of googling and trying different things, I found a video from another cohort where Jennifer went over omniauth google. She has an amazing way of explaining things so I followed along with her video and got google omniauth up and running 

Once you clone the repo from github, bundle install, and rake db:migrate, start the server with rails s. Once on the site you can login with google or set up an account. I made a conditional navbar that shows different links if you are logged in or not. Once you create an account you will be redirected to the games index page to see a list of all the games already created. This list is alphabetized through an active record scope method.  Each game is a link to the show page of that game where you can read reviews and write one of your own. 

This project has given me ideas for other applications that I would like to create including a portfolio site. I can't wait to get started working on that. 


