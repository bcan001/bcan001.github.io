---
layout: post
title: Updating Course Discuss to Rails 5
---

Today I continued my process of updating one of my applications from rails 4 to rails 5. I've found that process of switching ruby versions with rbenv has been very effective, as I can toggle between rails frameworks and projects quite easily. One of the main things I've been working on is testing in the new rails 5 application. The original rails 4 project didn't have many tests at all, so I've been reinforcing my development knowledge through writing tests with rspec. I'm using factory girl for factories with the faker gem for creating data in my tests. So far I've written all the model tests and the controller tests, as well as a feature test for logging in and logging out of the application. Capybara was required for feature testing, and I've found the syntax to be very readable and easy to incorporate with my views. I will keep updating the app and posting my updates here... so far so good :)