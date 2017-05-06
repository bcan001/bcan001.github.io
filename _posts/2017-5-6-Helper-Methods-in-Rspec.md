---
layout: post
title: Using Helper Methods in RSpec Tests
---

This week while I was building out Course Discuss in Rails 5 I noticed that my view tests were all failing due to insufficient access to the current_user method for checking authentication. I found this to be causing a bit of trouble, because my view logic had current_user on a lot of the view templates. In order to fix this I had to do a bit of digging and I found a way to create a method available for use in my RSpec tests that return necessary data for my view test:

[LINK TO CODE SNIPPET](https://gist.github.com/bcan001/2dedfd4687f9af7663d06dd3d8065846)

As you can see, the before clause creates a Factory Girl Stub and returns it when called in an RSpec test. I will be implementing this throughout my tests.