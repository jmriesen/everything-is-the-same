---
layout: page
title: Influences
permalink: /influences/
---
This is an archive of thought provoking media I have encountered and keep coming back to.

## Design
### [Refactoring Is Not Just Clickbait - Kevlin Henney - NDC London 2023](https://www.youtube.com/watch?v=NMPeAW2RWdc)
All of Kevlin Henney's talks are worth a watch.
Impotent ideas include:
- Technical Debt doesn't just appear, it is the result of a process. He has named this process Technical Neglect.
- Neglect happens because the situation around the code changes, what once was a good decision can become problematic as the world around the problem changes.

### [The Only Unbreakable Law](https://www.youtube.com/watch?v=5IUj1EZwpJY&t=75s)
The communication channels in your organization will influence how your projects are built/organized.
So be mindful of how you set up those channels.

### [TDD Is The Best Design Technique](https://www.youtube.com/watch?v=ln4WnxX-wrw)
I think this is a good introduction to test driven development.
TDD has had a significant influence on how I prefer to code. 
The most valuable lesson I have learned from TDD is to focus on how the you as the future end user want to consume the code before deciding how to implement it.

### [In Defense of Not-Invented-Here Syndrome](https://www.joelonsoftware.com/2001/10/14/in-defense-of-not-invented-here-syndrome/)
Reuse is great for highly standardized components, however "If it is a core business function -- do it yourself, no matter what."

I often think back to this article, if your dependencies are driving what you can and can't do, if they have have bled into your core, the world is acting on you, rather than you acting on the world.
Note, this principle is not limited to software.

## Testing
### [Mutation Testing in Python • Austin Bingham • GOTO 2015](https://www.youtube.com/watch?v=jwB3Nn4hR1o)
The first 20 minutes of the above video is a good introduction to the what/why of mutation testing.
Mutation testing is an interesting idea that I first encounter in collage.
I frequently use [cargo-mutants](https://github.com/sourcefrog/cargo-mutants) to mutation test personal projects

### [Decrusting the quickcheck crate](https://www.youtube.com/watch?v=64t-gPC33cc)
Property based testing is an interesting idea because you are operating on classes of objects rather a particular objects.
This is especially useful for things like serialization and de-serialalization where one function is the inverse of the other.
```
f(x) = x*2
--- Normal Unit testing 
assert(f(0),0);
assert(f(2),4);
assert(f(100),200);

--- Property based testing
For all y:
assert(f(y).is_even())
```

NOTE: Fuzz testing is a subset of property based testing where you are asserting that:
1. There are no invalid memory access.
2. The program does not crash.


