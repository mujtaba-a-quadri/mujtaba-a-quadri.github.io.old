---
layout: essay
type: essay
title: !
# All dates must be YYYY-MM-DD format!
date: 2021-02-11
labels:
  - ,
  - *
  - .
---

## I have a confession to make

I thought coding standards were pretty much useless. I never used them in my code I wrote for myself, and I didn't have to start using one until a class required it. All it felt like it was doing was making code take twice as long to write (as I comb through it to make it adhere to the guidelines). 

## But then...

I started to actually have to work on other people's code. All of a sudden, I'm reading files (not unlike the ones I wrote myself with no coding standard) which seem to have no rhyme or reason. One letter variable names all over the place, functions I cannot decipher due to 0 commenting, and files with a line count surpassing the current year.

## Example of a "bad" question

[This question](https://stackoverflow.com/questions/65930525/error-converting-result-java-lang-nullpointerexception-and-json-parser-error-pa) at first appears to be quite similar to my example of a good, small, specific question, its first line reads:

```
I keep getting the following error in my logcat whenever
i try to click on "login" or "signup" on my virtual device
<long error message ommitted for length>
```

This is all reasonable, but it takes more than one line to make a good question (unless the question is rather simple). After this introduction the author should take time to talk about what he has tried, and what he was able to gather from his error message and research. But after reading past the first line (or reading the title), many red flags from the essay come up. First of all, the title is so long that it gets cut off by stack overflow, the title is just the long error message that is already pasted into the body. No one is going to read that title and think "I want to help this person". The author then committs the biggest cardinal sin of asking for help online: showing that they did no research on the topic themself, and instead simply dumping their source code for someone else to painstakingly comb through. The post does not even ask a direct question; it simply states the error is happening and dumps the code on you. That's bad enough, but they don't just dump one long function on the reader, they take it one step further by pasting the body of *three* different files. Just to recap, the entire body of this author's question is:

```
I keep getting the following error in my logcat whenever
i try to click on "login" or "signup" on my virtual device
<long error message>
Please help!
<entire body of 3 files>

```

Unsurprisingly, the author has not yet gotten a response. 

## Example of a SMART question

[This](https://stackoverflow.com/questions/2003505/how-do-i-delete-a-git-branch-locally-and-remotely) is a great example of a succinct, helpful question. It gets straight to the point right from the title and the author has the courtesy of showing what they tried themselves before asking:

```
(title) How do I delete a Git branch locally and remotely?
<failed command line attempts>
What should I do differently?
```

There is really not much to say here, it's a very effective question. It also helped many other people due to its very clear title being easy to search for. It sits as one of the highest upvoted posts on stack overflow, and has been viewed over 8 million times.

## Conclusion

It is very important to value the time of and respect other people online (and in general!) - especially those who are volunteering to help you. Acting entitled to being handed a solution is a great way of being ignored or insulted even. Websites like stack overflow are fantastic for allowing us to quickly find solutions to issues and resolve them without having to do hours of testing or combing through a manual. But it can also be used lazily as a personal tutor. It's critical to remember to ask smart questions, as they can often resolve the issue before you even finish typing them.
