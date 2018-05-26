---
layout: post
title: Blocks vs. Procs in Ruby
---

Today I was reading an article that outlined the differences between blocks and procs in ruby. I thought it was really interesting because most of the time I use blocks and after doing more research on procs and how useful they are, I can definitely see cases where a proc would have been more beneficial. One difference is that procs are objects, whereas blocks are not. A proc, such as @proc = Proc.new {/x/ puts x} can be called again by invoking the 'call' method (@proc.call(2)). Being able to store a procedure and use it again is very beneficial, and something that you can't accomplish with blocks. Another difference is that multiple procs can be passed in an argument list to a method, whereas only 1 block at most can be used in the argument list of a method.