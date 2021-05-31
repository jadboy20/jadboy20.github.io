---
title: "My code review checklist"
layout: post
date: 2021-05-31
categories: productivity review
---

Let me just put this out here. I've been coding professionally for about 4 years now, 2 of which I have been doing code reviews. Just to put it out there, I am not the best when it comes to reviews. I have always struggled to review code effectively. I always end up looking at the code as if it were a Lovecraftian ancient language.

Now if you're a potential employer looking through my posts, please know that I intend on changing that. In fact, in this post, I will list out a checklist that I have put together to help me with my review process, and hopefully you can take a bit out of it too.

I should start off saying that I got a lot of my ideas from [Jason C. McDonald's 10 Principles of a Good Code Review][0], which provided really good tips for a good code review.

So here goes the checklist:


## 1. Get Context

* Understand the original problem the code is trying to solve. You can do this by **Reading the ticket**.
* Ask questions to your colleagues. If the ticket doesn't have the information you're looking for, they may be able to provide more information to you.


## 2. Read the implementation review

Where I work, prior to implementing our code, we write up what we plan on doing to address the issue, and then we provide a list of tests we think would be appropriate to test the changes that were made, and ensure no regression occurs.

So this item would involve:

* Does the logic address the problem stated in the ticket?
* Are the tests exercising the changes?
* Are there any regression tests to ensure that no bugs have been introduced, or that existing code has been broken?


## 3. Read through the code

You need to understand the code before you can suggest any improvements to the code. This doesn't mean to understand the entire code base, but to understand at least the intent of the changes, and the impact they have.

Here are some suggestions:

* Can logic be improved?
* Does the logic achieve the goal, or match the implementation documentation?


## 4. Check comments

Comments should describe the intent of the code it is paired with. It must:

* Make sense
* No typos
* Match to the code

If the comment is just saying what the code is doing, then it should be removed, as it doesn't serve any purpose further than rehashing what the code is saying.


## 5. Check readability

Is the code readable? Code should be:

* Self documenting -> Variables should be self explanatory and functions should have appropriate names
* Correct style (follow style guidelines)


## 6. Check out the code and check that it builds

This is a quick way of seeing if the code is actually working or not. Especially with languages that are either compiled or transpiled, this can be used to ensure that the code is correct, and that there are no errors.

Also lint the code. This will check if there are any wrong or vulnerable bits of code.

You can also do a quick test on it if it doesn't take up too much time.


## 7. See if code can be optimised

Now that you have:

1. Understood the code
2. Ensure that it is readable

Now you can check if it can be optimised. Only do this if you feel that it needs to. Never try to optimise before the above two. This is because there is no point in optimising the code if its messy and hard to follow. That will allow bugs to slip into the code.



[0]: https://dev.to/codemouse92/10-principles-of-a-good-code-review-2eg?fbclid=IwAR3aY8LW6Q7gMT2RQCmmPgZJTRny8D4xdtgxZ1MlM0af1L96_z3GGlEkHCo
