---
title: "Div-orce: The Power of Semantic HTML"
author: Elyse Newland
pubDatetime: 2023-12-22T13:05:51Z
postSlug: semantic-html
featured: false
draft: false
tags:
  - Web-Development
  - HTML
  - Semantic-HTML
  - Progress
  - Accessibility
  - SEO

description: "The simple solution to write better code."
---

What if I told you that one of the secrets to becoming a better web developer isn't mastering complex algorithms or memorizing every CSS property? It's something much simpler and often overlooked: Semantic HTML.

Semantic HTML means intentionally using specific tags to give meaning and structure to your code.

So let go of the “div-for-everything” mindset, and get back to the basics.

## Elevate Your Code

How will using semantic HTML help you become a better web developer?

### Accessibility

Developers code sites that a variety of users will touch. Semantic HTML creates more accessible code. For visually-impaired or low-sighted users, HTML tags allow screen readers to more accurately navigate and communicate the site’s layout by giving meaning to each section of a page. For example, using `<header>` with a `<nav>` tag indicates to the screen reader that there is a primary navigation menu. If someone places the navigation menu within a div, that div provides no context as to the content it contains.

### SEO

Search engines use the structure of HTML documents to understand the content and context of websites. Semantic HTML helps search engines interpret the significance of different parts of a web page, potentially improving search rankings. Search engines are increasingly prioritizing user experience in their algorithms. By using semantic HTML, you not only make your code accessible to assistive technologies but also create a site with better search rankings.

### Marketability

Using semantic HTML makes you look better! If you’re applying for jobs, semantic tags allow you to demonstrate your understanding of web development best practices. If it comes down to two job candidates but one places everything in divs and you appropriately use semantic HTML, you’re more likely to get that position.

### Cleaner Code

You’ll inherently create cleaner code using semantic HTML. It creates an easily understandable and readable layout. In addition to being more marketable, you’ll be appreciated by your fellow developers if you write clean, easily maintainable code.

## Use Cases

Even if you're new to web development, you’ve likely learned HTML. And if you're a seasoned developer, go back to basics and ensure that you’re using markup in a way that demonstrates clean code and benefits more users.

### Examples

Semantic HTML tags include `<header>`, `<main>`,`<footer>`, `<nav>`, `<article>`, `<section>`, `<aside>`, `<a>`, `<h1>`, `<h2>`, etc.

#### Structural Tags

`<header>`: Indicates the introductory content of the site.  
`<main>`: Used for the primary content of the site.  
`<footer>`: Represents the footer of a site which might include links, contact, and copyright information.  
`<section>`: Used to group sections of related content, e.g., chapters in a book.  
`<article>`: Used to denote an independent, stand-alone section of a site, e.g., the book itself.

#### Heading Tags

_Don't_ use heading tags for their style properties. Instead use each one appropriately based on the heading level and style with CSS.

`<h1>`: The headline of your site. There should only be one `<h1>`.

For each subheading, you’ll move down a heading level:  
`<h2>`: Indicates the first subheading after the main headline.  
`<h3>`, `<h4>`, etc.: Indicates further subtopics.

### Divs & Spans

Does this mean you should never use divs or spans?

No! Divs and spans have their place. There are times when it’s appropriate and necessary to use them. The important thing to remember when crafting your code with semantic HTML is to create meaning using appropriate tags and not throw _everything_ in a `<div>` or `<span>`.

So get back to basics with semantic HTML. Div-orce using divs for everything. Create cleaner, more accessible code that improves the user’s experience and makes you more hireable.

## TLDR

Instead of throwing everything in a `<div>` or `<span>`, use semantic HTML to give your site’s content structure and meaning. Semantic HTML can help developers level up their skills and become more marketable by creating cleaner, more accessible code with better SEO.
