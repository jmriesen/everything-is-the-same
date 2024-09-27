---
layout: post
title:  "Not All Languages Are Typed, But All Programs Are"
date:   2024-09-26 15:05:46 -0500
categories: jekyll update
---
Types are everywhere, normal non programmers use them every day.
Types are just constraints we impose on the underlying data so that when we interact with the data we get meaningful results.


Say we have the social security number 123-45-6789 and 987-65-4321 there is a lot we could do with this information. 
We could verify someone is who they say they are, or alternatively we could commit identity fraud.
But there is (at least) one thing we can't do... add them. 

Oh sure we can through the underlying bits though an arithmetic logic unit, and get the output of 222111110 but what does that mean?
That is not a social security number.
It's 222111110 ... apples?, pairs?, a user id?
I will tell you what that is, its meaningless.
There is no meaningful way to add social security numbers. 

So if type just define the valid use cases for some bit of data - does everything have a type? Yes, by (my) definition.

If everything has a type then why are there typed/untyped languages? 
Typed programming languages like C, Java, Rust extra allow us to encode type information in a way the compiler understands. 
This allows the compiler to enforce that our types are used properly.

Not all type systems are equal. 
Some are more expressive than others, and thing that can't be enforced by the compiler, must be enforced by the programmer.
For example in Rust you can use the Pin&lt Foo&gt type to indicate that Foo's memory address must not change.
There is no way for to encode this same invarient in C's type system. 

Untyped languages occupy one extreme of the spectrum. 
Untyped languages offer little if any type enforcement by the compiler, so the programmer must enforce any invariant.

I have heard the argument that vary strongly typed languages require a lot of boiler plate and are overly pedantic. 
However I would almost always preferring in a strongly typed language and work with the compiler, rather then try and hold everything in my head.
But everything in moderation.

Now there is a place for both compiler enforced and programmer enforced type systems.
The compiler, can catch all the instances of type misuse (for the constraints the compiler is ware of), but it takes time to encode those type semantics.
On the other hand humans are error prone, but if the type system only exists in our head it can almost instantaneously be updated.
Programmer enforced is great for small reaped prototyping, where compiler enforced excels once I know what my solution should be. 


