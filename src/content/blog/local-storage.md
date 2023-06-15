---
title: "localStorage and Next.js"
author: Elyse Newland
pubDatetime: 2023-06-15T10:30:51Z
postSlug: localStorage
featured: false
draft: false
tags:
  - Full-Stack
  - Web-Development
  - localStorage
  - Next.js
  - Javascript
  - React
  - Debugging

description: "Getting the hang of localStorage in Next.js."
---

I've been working on a new personal project, a simple todo list app, to familiarize myself with Next.js.

One of my goals for this project was to successfully utilize localStorage to persist the user's list data even if the user refreshes or closes the browser. I recognize that there are more secure ways to persist user data, but we all gotta start somewhere 🙂

## Client-Side Data Storage

There are several ways to store data on the client side: localStorage, sessionStorage, and cookies.

The main difference between localStorage and sessionStorage is that localStorage inherently has no expiration date. Both persist user data on refresh, but sessionStorage expires after one session. They both have storage limits of around 5MB. Cookies, on the other hand, only have about 4kB of storage but can be accessed both from the server side and client side.

I decided on localStorage for my app due to its lack of expiration date (compared to sessionStorage) and the fact that setting cookies is a bit more complex.

## The In’s & Out’s of localStorage

My first feat was to get a real grasp of what localStorage actually is and how it works. localStorage is simply a way to store key/value pairs in the browser. Functionally, this means that if a user refreshes the page or closes the browser, their data will remain on the browser, and they can still access it.

After some Googling on how to use localStorage, I got to work trying it out.

Some important things to note about how data is stored: in localStorage, data is always stored as a string, while in Javascript(JS), it's stored as its datatype (an object, array, etc.). We have to use `JSON.parse` to take data from localStorage and convert it to JS syntax, and alternately, use `JSON.stringify` to convert data from JS syntax to a string so that localStorage can access it.

The first step when using localStorage is to get your data from localStorage using the syntax: `localStorage.getItem("x")`. When getting data from localStorage, we use `JSON.parse` to convert the string to JS syntax.

The second step is to set your data using the syntax `localStorage.setItem("x")`. When setting or sending the data from JS to localStorage, we have to use `JSON.stringify` to convert JS syntax into a string.

## localStorage & Next.js

There is a special consideration when using localStorage and Next.js. Next.js is a React framework, and one of the reasons it's so snappy is that the first page load is done on the server side. However, when we use localStorage inside a Next.js app, we'll initially get an error that localStorage is not defined. This is because of the server-side rendering that Next.js uses. The localStorage object is only available on the client side.

So how do we get around this issue? While I found several solutions, using the useEffect hook for localStorage.getItem("value") seemed to be the most straightforward. Because Next.js is a React framework, we can access React hooks like useState and useEffect. In this specific case, the useEffect hook allows access to localStorage after the component mounts and is running client-side, which ensures that localStorage is being defined.

Using the useEffect hook allowed me to successfully access localStorage and persist my user's todo list on my Next.js todo app. My next steps in the project are to allow the user to delete their checked todo list items and begin styling!

## TLDR

localStorage is a way to persist user data even if the user refreshes the page or closes the browser. There are specific considerations to remember when accessing localStorage, including parsing the data when getting the items from localStorage and stringifying the data when moving from Javascript to localStorage. If you're using Next.js, a React framework, you'll need to use a method to access localStorage. Because Next.js initially renders server side, localStorage (only available client side) will be undefined unless a method, like the useEffect React hook, is used to access it.
