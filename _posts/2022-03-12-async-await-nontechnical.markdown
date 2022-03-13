---
layout: post
title: 'The Idea Behind Async/Await'
date: 2022-03-12 6:05:00 -0600
categories:
---

# Background

A common interview question we ask candidates is to explain the problem async/await in .NET aims to solve. The kicker of the question - we ask for an explanation as though it'd be given to a spouse or parent. Typically candidates go into a spiel around how the async state machine works or they will start talking about how the feature lends itself towards _parallelism_. While true, both the miss the point of the question.

## A Little Background

Task and async/await at their core are meant to be the answer to managing _concurrency_ within a programming language. Concurrency can best be thought of the ability to work on multiple tasks simultaneously. Parallelism (delegating the tasks to multiple workers to solve the problem), is a related extension of concurrency.

Commonly these two concepts are confused as interchangeable and they are not. The distinction between the two is one of part of what we're trying to see if the candidate understands.

## Example Answer

One of the best answers to the this question is as follows.

It's Sunday. You have the Sunday Scaries - including but not limited to: feeding yourself, laundry, feeding the cat, milking the cows, setting up the date for tomorrow, taxes, etc. In your existential despair, you decide to order a pizza. You pick up your cell phone and order the pizza. You have some options at this point. Either you can: sit in front of the door waiting for the pizza or start to tackle the remaining chores you have to do.

As a human, you probably scoffed at the idea of sitting in front of the door waiting patiently for the pizza delivery guy to tell you he's at the door. Some guy named Doug. Of course you're going to do something else while waiting because sitting in front of the door would be a blatant waste of time.

This is what concurrency is. Rather than waiting for some process to complete outside of your control (an API call, a SQL query, etc), do something else and when the delivery guy, Doug, calls you get the pizza.

When you're writing code that accesses an external resource, why would you want to block your CPU waiting on something else to complete that's out of your control? Accomplish another set of tasks and pick the result of the external resource up when it's ready for processing. Chungus 👀👀👀
