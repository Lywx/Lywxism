---
title: Construct A DSL(Domain Specific Language) From Customed Markdown and Parse It with Sprache
layout: post
tags:
- Markdown
- Sprache
- DSL
---

#### 1. Introduction

[Sprache] is a DSL([Domain Specific Language]) parser in C#.
With it, you can easily construct your custom data using plain text.

Since Sublime Text with [MarkdownEditint] Package is great at assisting editing Markdown. I could use Sublime Text to edit these data and they look awesome.


#### 2. Markdown With A Time Tag In Title

I choose to add my time tag after standard Markdown title. These time tags are used for scheduled retrieval in a schedule program.

{% highlight markdown %}

    ## <title of piece of knowledge> [<time for necessary retrieval>]

<paragraphs that follow after>

{% endhighlight %}

This is an example I construct from an answer in [What Characteristics Or Features Make Code Maintainable]:

{% highlight markdown %}

    ## What is Maintainability [60]

    Roughly speaking, maintainability is inversely proportional to the amount of time it takes a developer to make a change and the risk that change will break something.

    Improving readability, coupling, or consistency all contribute to maintainability because it won't take as long to make any given change.

    Maintainability is easier to recognize by its absence, like when something you thought should take an hour ends up taking a week.

{% endhighlight %}

TODO:

#### 3. Structured Schedule Information Parsing

And I want another type of data: schedule information. It looks like the following:

{% highlight markdown %}

    [Everyday AM 7:0:0]

        COMMAND: You must trust yourself and must be able to stand up again. This is the tried and proved way to clean up negative emotion!

        MUSIC:   Stand Up Battle Formation Again! - 英雄伝説 零の軌跡

    [Everyday AM 7:0:0]

        COMMAND: ...

        MUSIC:   ...

{% endhighlight %}

TODO:

[Sprache]: https://github.com/sprache/Sprache

[Domain Specific Language]: http://en.wikipedia.org/wiki/Domain-specific_language

[MarkdownEditint]: https://packagecontrol.io/packages/MarkdownEditing

[What Characteristics Or Features Make Code Maintainable]: http://programmers.what-characteristics-or-features-make-code-maintainable/questions/134855/what-characteristics-or-features-make-code-maintainable
