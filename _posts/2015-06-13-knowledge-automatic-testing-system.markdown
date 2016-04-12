---
title:      Experimental Knowledge Automatic Testing System
layout:     post
categories: Exploration
date:       2015-06-13 00:00:00
tags:
- Knowledge Management
---

## 1. Introduction

The previously introduced knowledge management system is proved to be
ineffective in terms of flexibility and effectivity after months of experiments.
Even though I later introduced audio narrative for the key sentence of the
specific piece of knowledge entry, it is still incredibly cumbersome to use. It
is like a degraded version of Google Now (without real useful data). Sometimes
it is quite annoying to hear these irrelevant notification. At some extent, I
believed it even harmfully introduces some overhead to an already
task-overloaded mind. So I hereby concluded this project is a complete failure.
I am not longer able to see any potential in it.

A week later, I felt inspired by the development workflow of TDD (Test Driven
Development) and CTTD (Continuous Test-driven Development) immensely. I found
these idea could be potentially useful as a automatic check-list like thinking
tools. Since the fundamental practice in TDD is to ensure the tests passed
over time. I could write tests using scriping languages and hook these tests
with the audio notification system, which would be a very cheap and flexible
design for a personal assistant software.

## 2. Refinement

I implemeted the initial system but not satisfied with the result I got. The
first testing system consists of a tree-view of tests. All tests are
interactively updated and aided with well understood status notification.

But it is hard for me to do any things quality-controllable to the test results.
Tests are easy to write but hard to fix. I thought I need some process
management tools that help me ensure some of effeciency. So, I prototyped a
state machine based process management interface that loads F# scripts into the
platform. The F# scripts use
[Stateless](https://github.com/slashdotdash/stateless) to construct state
machines based processes. With some interaction capability, it becomes very
handy indeed. The basic use-case would be:

    Test fails -> Process runs -> Process runs -> ... -> Test passes -> ... -> Test fails -> ...

## TO BE CONTINUED ...
