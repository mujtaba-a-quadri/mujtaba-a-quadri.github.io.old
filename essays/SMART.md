---
layout: essay
type: essay
title: SMART goals? No, wait; smart questions!
# All dates must be YYYY-MM-DD format!
date: 2021-01-27
labels:
  - questions
  - answers
  - goals
---

## What does any of that title mean?

After reading Eric Steven Raymond and Rick Moen's essay [*How to Ask Questions the Smart Way*](http://catb.org/~esr/faqs/smart-questions.html), I realized how similar the guidelines were to SMART goals. The essay is a long write up of how to formulate good questions to ask hackers and developers on online forums, chat rooms, or through email. SMART goals are a general guideline for how to make effective goals, SMART is an acronym that describes good goals: specific, measureable, achievable, relevant, and timely. I thought the advice given in the essay was very similar and mirrored the ideas in the SMART goals acronym. 

### More Specifically...

The SMART goals acronym in the most general sense is trying to stop you from making goals that are too big and open ended to act upon. Instead it guides you into making smaller (and probably multiple) goals which are more actionable. The essay on how to ask questions follows a similar idea. It tries to steer you away from asking questions that are too open ended and general, and really get to the heart of what you are asking. Rather than asking "How do I implement [insert complicated feature here]?" you should start working on that feature and ask a more specific and smaller question that comes up along the way, like "X issue is coming up when I do Y on Z, what am I doing wrong?". 

## Example of a "bad" question

[This question](https://stackoverflow.com/questions/65930525/error-converting-result-java-lang-nullpointerexception-and-json-parser-error-pa) at first appears to be quite similar to my example of a good, small, specific question, its first line reads:

```
I keep getting the following error in my logcat whenever i try to click on "login" or "signup" on my virtual device
<long error message ommitted for length>
```

This is all reasonable, but it takes more than one line to make a good question (unless the question is rather simple). After this introduction the author should take time to talk about what he has tried, and what he was able to gather from his error message and research. But after reading past the first line (or reading the title), many red flags from the essay come up. First of all, the title is so long that it gets cut off by stack overflow, the title is just the long error message that is already pasted into the body. No one is going to read that title and think "I want to help this person". The author then committs the biggest cardinal sin of asking for help online: showing that they did absolutely no research on the topic themself, and instead simply dumping their source code for someone else to painstakingly comb through. Even one long function would be too much to ask for random people on the internet to read through, but this author takes it a step further by pasting the body of *three* different files. Just to recap, the entire body of this author's question is:

```
<intro>
<long error message>
Please help!
<body of 3 files>

```

Unsurprisingly, the author has not yet gotten a response. 

## Example of a "bad" question

Q: python date of the previous month

I am trying to get the date of the previous month with python. Here is what i've tried:

str( time.strftime('%Y') ) + str( int(time.strftime('%m'))-1 )

However, this way is bad for 2 reasons: First it returns 20122 for the February of 2012 (instead of 201202) 
and secondly it will return 0 instead of 12 on January.

I have solved this trouble in bash with:

echo $(date -d"3 month ago" "+%G%m%d")

I think that if bash has a built-in way for this purpose, then python, much more equipped, should provide something 
better than forcing writing one's own script to achieve this goal. Of course i could do something like:

if int(time.strftime('%m')) == 1:
    return '12'
else:
    if int(time.strftime('%m')) < 10:
        return '0'+str(time.strftime('%m')-1)
    else:
        return str(time.strftime('%m') -1)
        
I have not tested this code and i don't want to use it anyway (unless I can't find any other way:/)

Thanks for your help!
```

While the heading of his question could be better, it does convey what he’s trying to figure out. Usually something as brief as “python date of previous month” is what other users would enter in as search terms on Google, making it easily found. Another good thing about the question is that it’s not just a question. The asker shows what he or she has done and that he or she has put in some effort to answer the question. And while it may not be as important as the question itself, the asker shows courtesy, which does increase the chance of getting an answer.

```
A: datetime and the datetime.timedelta classes are your friend.

1. find today
2. use that to find the first day of this month.
3. use timedelta to backup a single day, to the last day of the previous month.
4. print the YYYYMM string you're looking for.

Like this:

 >>> import datetime
 >>> today = datetime.date.today()
 >>> first = datetime.date(day=1, month=today.month, year=today.year)
 >>> lastMonth = first - datetime.timedelta(days=1)
 >>> print lastMonth.strftime("%Y%m")
 201202
 >>>

```
 
The asker received six possible answers, and he or she was successful in inciting discussion from multiple users. The answers themselves were clear and were devoid of the rumored sarcasm and hostility of “hackers.” Since I myself have referenced this page and found it useful, I can confidently say that it is a good question.

## The foolproof way to get ignored.

While there are decent questions that benefit everyone, there are those one can ask to create an entirely different effect. In the following example, a user asks how he would, in short, create a desktop application with Facebook.

```
Q: Facebook Desktop Notifier

I am a beginner programmer that have never used anything other than what's included in a language.

I am trying to create a desktop application that notifies me anytime I get an update onfacebook. 
How should go about doing this? Thanks in advance.

edit Sorry I was not clear. Is there any way to make a DESKTOP application with facebook?
```

A simple “yes” would have answered the question, but we know that’s not the sort of answer he or she is looking for. Fortunately, someone kindly responded with a link to Facebook’s developer website. The asker should have done more research on his or her potential project. Then further down the road, he or she could have asked more specific and detailed questions that wouldn’t require a thousand-paged response for a sufficient answer.

## Conclusion

When we rely on others’ generosity and expertise to provide answers to our questions, it should hold that the question we ask should be one that leads to efficient and effective help that not only benefits us, but also the people we ask and others who might ask the same question in the future. Thus, if you have a question… make it a smart one! Asking questions may not always get you the best answer, but asking them in a way that will make others want to answer them will increase the success of finding a good solution and make it a positive experience on all sides.
