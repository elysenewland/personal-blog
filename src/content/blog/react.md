---
title: "A High-Level Overview of React"
author: Elyse Newland
pubDatetime: 2023-02-24T16:42:51Z
postSlug: react-overview
featured: false
draft: false
tags:
  - JavaScript
  - React
description: "Understanding what makes React so powerful and unique."
---

If you're coding in Javascript, React is pretty special. At its core, React is a Javascript library for building user interfaces. It's a unique and powerful library for several different reasons.

## Declarative

React is a declarative programming library. I learn better with analogies, so here you go 🙂

Declarative programming is like a chef knowing what a dish should look and taste like, putting the ingredients together, and letting the cooking process create the outcome. Compared to imperative programming, that same chef would work step-by-step through each recipe instruction, constantly checking if each step has been completed and if the dish is ready to be cooked.

<video class="w-full h-auto" autoplay loop muted playsinline aria-describedby="video-caption">
    <source src="https://media.giphy.com/media/K7txBCu1lvLTW/giphy.mp4" type="video/mp4">
    <div id="video-caption" class="sr-only">The Swedish Chef from The Muppet Show cooking.</div>
</video>

Essentially, declarative programming helps you work smarter, not harder! I like that.

In web development, the programmer declares what the user interface (UI) should look like rather than having to spell things out step-by-step for the computer. React updates the Document Object Model (DOM) to reflect what the UI should look like.

As someone who initially began learning to program using C (an imperative language), declarative programming has my full support.

It allows the programmer to focus on what the UI should be rather than how to update the DOM to reflect changes. React's ability to update the DOM creates a faster experience for the user and allows the programmer to develop reusable components.

## Components

React sites are built with components which you can think of like Lego blocks. We put individual blocks together to create something amazing at the end.

In React, we can create reusable components. For example, let's say we want to create submit button, and it needs to live in two places on our site. We can create the component once and then use it wherever we need to throughout our site.

Importantly, React components can also contain other components. This ability makes our code much more efficient and saves the programmer time. And if we name our components explicitly, this can decrease confusion when returning to the code or when someone new is reviewing it.

## JSX

JavaScript XML (JSX) is like a stricter HTML. However, it's not valid JS. You'll need a compiler like Babel to convert it to JS so React can use it.

Importantly, JSX isn't required in our React apps. So why do we use it? If you're already familiar with HTML, it can make your site's development process much smoother and faster. While it's not exactly like HTML, it's close enough to be pretty intuitive.

Writing JSX in React creates cleaner-looking code and spits back more helpful error messages, making it easier to debug.

## One-Way Data Flow

In React, data flows from top to bottom. Data comes in the form of properties (props) and is transferred from parent to child but never from child to parent.
The child will then either apply a change or pass it on to the next child.

Why is this helpful?

Child components can never modify data on their own, which helps to streamline the data process. This makes the code more efficient and less prone to errors.

It also makes debugging easier. If the programmer understands where the data is coming from (parent), they can go there to correct it.

### TLDR

React is pretty cool. It's a declarative programming language making it easier for the developer to make cool shit. It uses components, which are like Lego Blocks, that can be combined and reused to make an awesome end product. React uses JSX, a JS/HTML hybrid, that makes it more intuitive to write code resulting in a smoother, more efficient development process. It has a one-way data flow structure, meaning all data moves from parent to child components resulting in easier debugging and a streamlined data process.
