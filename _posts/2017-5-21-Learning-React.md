---
layout: post
title: Learning React JS
---

The past few weeks I've been going through some tutorials to learn React JS. I'm really interested in React because of its speed. With Rails we're used to a lot of defined structure and organization, but since Javascript is the only language in the browser, its imperative to keep up with the most advanced Javascript libraries and frameworks. The first tutorial I went through is the Tic Tac Toe game tutorial on the Facebook website. Here is where my code lives:

[LINK TO CODE SNIPPET](https://github.com/bcan001/reactjs-tic-tac-toe)

What was really interesting for me was how React is a top down framework. Props (which are essentially variables) and State (which is constructed on initial page render) of each React Class Object are passed down to child objects. So in the example of a Tic Tac Toe game, the Game object passes down to the Board object, which passes down to the Square objects. The tricky part is identifying which object should hold the state of the game. Since the Board needs to know if someone wins, for instance, it holds all the information as to which squares are used and what player used them. I'm not currently done with the tutorial yet, but I will keep this up to date on what I learn. In the meantime, happy coding!