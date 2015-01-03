---
title: Construct A Knowledge Retrieval System With Markdown and Parse It with Sprache
layout: post
guid: urn:uuid:f1f1a21b-a50b-424c-9554-6e6382b6122a
tags:
- Knowledge Management
- Domain Specific Language
---

#### 1. Introduction

People forget important things more often than they thought. On the concern of
productivity, knowledge is gained from books, posts on Internet, thoughts and
classes. Even we take notes, we may forget the essentialness of these tiny
pieces of information in runtime of our cognitive activities.

I personally would forget things like "What is the current objective of this
time span?", "What is the possible strategies to solve this math problem" or
"When to examine this piece of code that is becoming messy?". I am not merely
**not remembering** things but I am **not aware of** these piece of information.
It is possible to construct a simple system that inform you in scheduled base
that enforce practice of these knowledge or mind set that you thought is
helpful.

[Sprache] is a Domain Specific Language parser in C# that is aim to construct
your custom data or a simple Domain Specific Language using plain text. It is
much easier to use it as a parser for your formatted knowledge than writing your
own parser or lexer.

#### 2. Domain Knowledge With A Customized Markdown

I choose to add my time tag after standard Markdown title. These time tags are
used for scheduled retrieval in a schedule program that walk through these
linked file to construct a list of command entries. These command entries are
retrieved in specific conditions according to time tags.

The format comes as the following:

{% highlight markdown %}

## <title-of-a-piece-of-knowledge> [<time-for-necessary-retrieval>]

<paragraphs-that-follow-after>

{% endhighlight %}

This is an example I construct from an answer in [What Characteristics Or
Features Make Code Maintainable]:

{% highlight markdown %}

## What is Maintainability [00-60-00]

Roughly speaking, maintainability is inversely proportional to the amount of
time it takes a developer to make a change and the risk that change will
break something.

Improving readability, coupling, or consistency all contribute to
maintainability because it won't take as long to make any given change.

Maintainability is easier to recognize by its absence, like when something
you thought should take an hour ends up taking a week.

{% endhighlight %}

The only difference from standard Markdown is the ``[00-60-00]``, which
indicates the repeativity of this piece of information. ``[00-60-00]`` means 0
hours, 60 minutes and 0 seconds.

Of course, this information is trivial for an experienced developer. But can you
recall it when you are upset on browsing your illy constructed code?

These knowledge is linked with a bigger concept call mode. A mode consists of
many related knowledge and it can be manually selected in runtime in cogntive
activities.

#### 3. Structured Schedule Information Parsing

And I want another type of data: schedule information. It looks like the
following:

{% highlight markdown %}

[Everyday AM 7:0:0]

    COMMAND: You must trust yourself and must be able to stand up again. This is
    the tried and proved way to clean up negative emotion!

    MUSIC:   Stand Up Battle Formation Again!

[Everyday AM 7:0:0]

    COMMAND: ...

    MUSIC:   ...

{% endhighlight %}

These command entries are supposed to be retrieved everyday on the specific
time.

#### 4. Notes

Maintaining a knowledge base is hard because all of your knowledge is somewhat
contradicting with each other. You might need to constantly edit your definition
and notion of your personal best practice and retrieval strategies.

According to my personal experiment, it did have a positive effect on my work
and life. So keep this thought in your brain:

> True knowledge is retrievable runtime execution of actions and thought.

[Sprache]: https://github.com/sprache/Sprache

[What Characteristics Or Features Make Code Maintainable]: http://programmers.what-characteristics-or-features-make-code-maintainable/questions/134855/what-characteristics-or-features-make-code-maintainable
