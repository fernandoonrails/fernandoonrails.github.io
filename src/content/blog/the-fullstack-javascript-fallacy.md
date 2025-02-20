---
title: 'The fullstack javascript productivity gain fallacy'
description: 'is fullstack javascript really a good idea? learn about it in this article'
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

Modern projects already use a ton of different stuff, like
- Tailwind
- some UI framework like React/Angular/Vue (dont @ me about React)
- docker

Adding just one more thing to the list will surelly not kill your productivity... Or will it?

## Javascript on the server is not the same as on the browser

We also have to consider that not only Javascript on the browser and javascript on the server have objectivelly
different APIs, and in reality, knowing Javascript on the front-end gives you virtually no real benefit
when switching over to the back-end. As people tend to say that
"you don't have the mental switch of the language",
even though the majority of languages that you use today, are heavily C-like, a lot of them are really
similar to one another, with most of them not having all of the gotchas of javascript.

We also need to consider that the type of job that the back-end does, and the one that the front-end does
are **NOT** comparable.\
If you want to learn back-end, you have to learn:

- SQL
- How to model the database tables/entities
- How to normalize the database
- Authentication
- Authorization
- How do I route my requests?
- How do I employ the best practices on my REST endpoints?
- How do I respond back with JSON?
- Which http status code should I respond with?
- ~~Since when have I became a teapot?~~
- How do I do middleware
- How do I accept a file upload?
- How do I store said file somewhere?
- Wtf is that CORS thing that my browser keeps complaining?
- How am I supposed to host it?
- How do I setup a pipeline so that it deploys automatically?

## Is code sharing really that usefull?

IMHO, you probably shouldn't, I've seen disasters ocurring on both the Js and on the .NET sides

At first, when you hear it, seems like a great idea, but it doesn't really work well in reality.
What happens all the time is that classes become too bloated and tries to do things that it **_really_** shouldn't.

This is much more apparent when classes describing database entities are part of the equation

Let's pretend we have this `User` class
that creates our User table on our Database via our chosen ORM.\
We also have the `GET /users/{userId}` endpoint, of course, we also show the posts on
our front-end, now look! We've made an amazing User class.

But wait... Things cannot possibly be that simple, Right? ... Right?\
Yeah, not quite. We also might want to add business rules to our class, like for example:

- The User's name cannot be empty
- The email gotta be unique

So we create an `Validate` function so that we can validate that, but since we are sharing code,
we also want to show it to the user, so now we somehow add some client-side attributes
(with internationalization, of course, what are we, rookies?), and look at that!
We've not got an Lovecraftian-esque creature of a class that does _way_ more than it's supposed to.

This always goes out of controll.\
**EVERY\
SINGLE\
TIME.**\
It's almost like a self fullfilling profecy

Code sharing is a common argument given while discussing about a lot of full-stack frameworks, like NextJs
or even .NET MVC, the argument goes along the lines of "You can share code and logic between front-end and back-end"
even though it can indeed, be a good argument for this, it can easily get out of hand pretty quickly

Let's imagine

## You get type safety between your front-end and your back-end

Honestly? It's not that big of a deal with modern tools like openAPI and Swagger,
for example, you could create a create a separate repository where you can store your api spec to serve
as the contract between your front-end and your back-end communication.\
You can also use [Typespec](https://typespec.io/) (not sponsored btw) where you can easily write your openAPI
spec using a DLS that is _very_ similar to typescript,
so that you don't need to worry about writing all that boring YAML
very quickly can becomes hundreds upon hundreds of lines as your project grows

## Easier deployment

That is actually true, it's way easier to deploy a single NextJs app than a Nextjs app + separate back-end
of your choice.\
However, setting up the pipelines for another project, shouldn't take you a lot of time (considering you've done it before)

## How do I chose something then?

If none of the argument that are used hold any value, how tf am I supposed to chose one?

And the answer is pretty easy\
Experiment with new languages.\
Write them, see how it feels writing them, see if you like their approach to handle X problem.

There is a lot of cool stuff, you can chose C#, Java, Python, Hell, even PHP with Laravel is amazing
(don't let the bad fame that legacy PHP has scare you, it actually pretty awesome)

## Final thoughts

The javascript ecossystem, even tho the most convoluted by far, has a lot of cool stuff, as it is arguibly
the best way to build front-ends.

It seems like there's an already built solution for most of your problems that you can just glue it together.

A lot of very smart engineers are activelly trying very hard to improve javascript on the server.
And it has indeed, became quite bearable... And that's that, nothing really more than that. Javascript
was made to become the language of the web and making cool interactivity on the client side, nothing more,
nothing less, Javascript on the server doesn't really give you the benefits of a language whose main pourpose
is to be used on the server.

Remember when I said `that you can just glue it together.`? Yeah... That's often how it feels when you're working
with different tools from different creators, Sometimes it feels like you're piecing a lot of stuff that
don't quite fit, not to shame the tool mantainers-- Tanner for example, is an impressive case of high-quality
tools that really fit well together on the react ecossystem, but unfortunelly, not every tool on the Javascript world get's the same level of care.
It can sometimes feel a bit lackluster, especially when you're forced to bootstrap something that doesn't seem to have been made with a cohesive vision.
