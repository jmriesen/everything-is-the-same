---
layout: post
title:  "Stability though testing"
date:   2024-09-26 15:05:46 -0500
categories: jekyll update
---

## Stability
The more I reflect on life the more I value stability. 
My current philosophy regarding stability was largely influenced by my time learning Yagyu.
Yagyu is a Japanese martial art and one of the core principles is: We do not lose, we may not win, but we will not lose.

I found stability in this context means:
1. I am safe.
2. I know I am safe.
3. Regardless of what my opponent does, I can respond in such a way that I remain stable.

I have found this notion of stability to be quite meaningful when applied to software development.
1. The code is correct.
2. I know the code is correct. 
3. Regardless of what modifications I am making, I work in such a way that I remain stable.

The big draw I see to cultivating stability is point #3, being able to move with confidence and correctness.

In both contexts stability is incredibly empowering, but is impotent to call out that stability is not an all or nothing proposition.
Stability is something that is cultivated and grows in a positive feedback loop.

We cultivate stability by working on our foundation, learning how to be safe, and learning to know if we are in danger.

## Programming and Stability
There is one big difference between being a martial artist and an engineer: engineers build tools.

This means we can we build tools that help us cultivate stability.
In particular we can write unit tests to help us *know* that our code is correct.
Additionally we can use Continuous Integration / Continuous Delivery (CICD) to re-certify this knowledge every time we make a change.

However, this does bring up another problem: how do we know that the unit tests are correct?
## Meta Testing Techniques
### Testing the tests
It is impotent to call out that meta testing techniques **do not** verify the correctness of our application code.
The goal of meta testing is to validate that our unit tests exercise the code under test in some meaningful way. 

Personally I have found the following techniques useful: 
- Mutation Testing

    Mutation checks how well our unit tests define the behavior of a systems.

    This is accomplished by mutating (changing a || to a &&, replacing a < with a <= extra) the application code before running the unit test suite.
    A code base passes Mutation Testing if all the mutations result in a failing unit test, 
    i.e. your unit tests can catch all the generated mutations.

- Code Coverage 

    Code coverage involves measure what lines of application code are executed when the unit tests are run.

    This helps identify code that is not under test.
- Test Driven Development.

    The main TDD workflow is:
    - Write a minimal failing unit test.
    - Write the minimum amount of code required to get all unit tests to pass.
    - Refactor your code.

    TDD can be viewed as the programmer's Double-Entry Bookkeeping.
    Any chance in the applications behavior is recorded in two locations, in the application code, in the unit test code.
