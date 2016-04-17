---
title:      Idea ~ Experimental Knowledge Retrieval System
layout:     post
categories: Exploration
date:       2015-01-03 00:00:00
tags:
- Knowledge Management
nocomments: true
---

## 1. Introduction

People forget important things more often than they would believe they actually
did. Knowledge is generally gained from books, posts on Internet, thoughts and
classes. Even we take notes, we may forget the essentialness of these tiny
pieces of information in runtime of our cognitive activities. In another word,
**you probably will not use specific knowledge when you should.**

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

## 2. Domain Knowledge With A Customized Markdown

I choose to add my time tag after standard Markdown title. These time tags are
used for scheduled retrieval in a schedule program that walk through these
linked file to construct a list of command entries. These command entries are
retrieved in specific conditions according to time tags.

The format comes as the following:

```markdown

    [Title of Knowledge] [[Time for Retrieval]]

    [Content of Knowledge]

```

This is an example I construct from an answer in [What Characteristics Or
Features Make Code Maintainable]:

```markdown

    # What is Maintainability [00:60:00]

    Roughly speaking, maintainability is inversely proportional to the amount of
    time it takes a developer to make a change and the risk that change will
    break something.

    Improving readability, coupling, or consistency all contribute to
    maintainability because it won't take as long to make any given change.

    Maintainability is easier to recognize by its absence, like when something
    you thought should take an hour ends up taking a week.

```

The only difference from standard Markdown is the ``[00:60:00]``, which
indicates the repeativity of this piece of information. ``[00:60:00]`` means 0
hours, 60 minutes and 0 seconds.

Of course, this information is trivial for an experienced developer. But can you
recall it when you are upset on browsing your illy constructed code?

This piece of knowledge is linked with a bigger knowledge in a tree like manner.
Gradually, a modular knowledge framework will be constructed with similar tiny
pieces of information. A module of knowledge consists of many related knowledge
and it can be leveraged in process of particular cogntive activities.

## 3. Structured Schedule Information Parsing

And I want another type of data: schedule information. It looks like the
following:

```markdown

    [Everyday AM 7:0:0]

        Command: You must trust yourself and must be able to stand up again. This is
        the tried and proved way to clean up negative emotion!

        Music:   Stand Up Battle Formation Again!

    [Everyday AM 7:0:0]

        Command: ...

        Music:   ...

```

These command entries are supposed to be retrieved everyday on the specific
time.

## 4. Notes

Maintaining a knowledge base is hard because all of your knowledge is somewhat
contradicting with each other. You might need to constantly edit your definition
and notion of your personal best practice and retrieval strategies.

According to my personal experiment, it did have a positive effect on my work
and life. So keep this thought in your brain:

> True knowledge is retrievable runtime execution of actions and thought.

## 5. Software Example

Running case of simple implementation of given mechanics.

![Acutance Preview](/media/files/2015/01/03/Acutance Preview.png)

In upper left side is a list showing loaded modules of knowledge. In upper right
side is a list showing triggered knowledge. The bottom displays the given
knowledge.

[Sprache]: https://github.com/sprache/Sprache
[What Characteristics Or Features Make Code Maintainable]: http://programmers.what-characteristics-or-features-make-code-maintainable/questions/134855/what-characteristics-or-features-make-code-maintainable
