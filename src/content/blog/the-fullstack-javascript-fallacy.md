---
title: 'The fullstack javascript productivity gain fallacy'
description: ''
pubDate: '17 Feb 2025'
heroImage: '/blog-placeholder-3.jpg'
---

Is Javascript really the best language for creating modern full stack web applications? In this blog, we'll be discussing about it.

## Do we really need to add more dependencies?

We already know that the web sometimes feel very bloated and overly complex, do we really need to add yet, ANOTHER
layer of complexity to our project with another language?

I've seen a lot of arguments about it on the past years with the popularization of Fullstack frameworks on the JsLand
such as NextJs and NuxtJs (wow, very creative names!), 
or even adding another full-fledged framework to the stack, 
such as NestJs (Some of y'all really are creative geniuses on the naming aspect)

Modern projects already use a ton of different stuff, such as:

- A framework like React/Angular/Vue (dont @ me about react)
- Containers
- CI/CD Pipelines

## Is code sharing really that usefull?

IMHO, you probably shouldn't, I've seen disasters ocurring on both the Js and on the .NET sides

At first, when you hear it, seems like a great idea, but it doesn't really work well in reality. 
What happens all the time is that classes become too bloated and tries to do things that it **_really_** shouldn't.

This is much more apparent when classes describing database entities are part of the equation 

Let's pretend we have this `User` class that creates our User table on our Database via our chosen ORM.

We


Code sharing is a common argument given while discussing about a lot of full-stack frameworks, like NextJs
or even .NET MVC, the argument goes along the lines of "You can share code and logic between front-end and back-end"
even though it can indeed, be a good argument for this, it can easily get out of hand pretty quickly

Let's imagine

## Javascript on the server is not the same as on the browser

Baz Daz