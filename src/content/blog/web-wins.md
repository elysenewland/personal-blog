---
title: "Web Dev Wins"
author: Elyse Newland
pubDatetime: 2023-06-02T14:15:51Z
postSlug: web-dev-wins
featured: false
draft: false
tags:
  - Full-Stack
  - Web Development
  - Deployment
  - Render
  - Debugging

description: "Crafting a personalized project and deploying my first full-stack app."
---

It's been a while since I've shared any of my web development journey, but that doesn't mean I haven't been hard at work.
I have a couple pieces of big news to share. First, I finished my Zero To Mastery Complete Web Dev course!

<video class="w-full h-auto" autoplay loop muted playsinline aria-describedby="video-caption">
    <source src="https://media.giphy.com/media/o75ajIFH0QnQC3nCeD/giphy.mp4" type="video/mp4">
    <div id="video-caption" class="sr-only">Erin from the Office fist pumping in celebration.</div>
</video>

## Making A Project My Own

The culmination of this course ends in a project called Smart Brain, a full-stack app. The frontend is built with React, the backend is built with node and express.js, and it utilizes PostgreSQL for the user database. It connects to the Clarifai API, which has a face-detection model.
The app allows the user to sign in and register.

Once logged in, the user can input an image URL from the web, which will connect to the face detection model on button click and then passes the image back to the user with a blue bounding box around any faces in the picture.

While this was initially part of the course, I made this project my own by:

- Renaming it to FaceFinder to more accurately describe the app
- Implementing a more modern design utilizing vanilla CSS (rather than Tachyons)
- Updating the code to check for multiple faces rather than just one
- Deleting the entry count because it didn't logically make sense in the app
- Making the site responsive
- Improving accessibility using the WAVE accessibility tool
- Adding login and image URL validation
- Resetting the image URL state upon sign-out so the previous image wouldn't display when a user logged in
- Creating a footer that displays when the user is logged in

## Deploying My First Full-Stack App

I don't know why, but each time I deploy a project, my palms are sweaty, knees weak, arms are heavy…

<video class="w-full h-auto" autoplay loop muted playsinline aria-describedby="video-caption">
    <source src="https://media.giphy.com/media/11IbChs8PTjgSQ/giphy.mp4" type="video/mp4">
    <div id="video-caption" class="sr-only">Eminem in 8 Mile rapping lyrics from Lose Yourself.</div>
</video>

So I was especially nervous attempting to deploy my FaceFinder full-stack project for the first time. For anyone out there using Render to deploy a full-stack app that includes a database, [this article](https://medium.com/@vanessavun/migrating-your-full-stack-react-app-from-heroku-to-render-9d7901d42e85) by Vanessa Vun, made the process so much easier.

The frontend deployment and connecting to a PostgreSQL database via Postico went smoothly. However, I hit a hiccup while trying to connect to my backend. I was unsure if the backend was supposed to have a build script, and Render prompted me for one. I initially tried `npm`, and then `npm run build`, which resulted in deployment failure.

After significant googling, I ran across [this article](https://www.freecodecamp.org/news/how-to-deploy-nodejs-application-with-render/) on [freecodecamp.org](https://www.freecodecamp.org/). While I was using `npm` and the author used `yarn`, they shared to enter `yarn` as the build command as it is the same as `yarn install`. After more googling, I found that Render looks for an `install` build command for backend deployment.

So I fixed this bug by running `npm install` as my build command.
I then had to update the fetch URLs on the frontend and create environmental variables on the backend to securely connect to the database.
After that, I checked out the app in its fully deployed state, only to find out that my app wouldn't sign in or register a user. Using the dev tools console, I discovered I'd made a silly mistake. I updated the fetch URLs in my app.js file but had forgotten to update them in my sign-in and register components; they were still fetching the local host URL.

Once I updated the fetch URLs in the sign-in and register files and pushed my changes to GitHub, I checked out the newly deployed app.

## Holy Sh\*t, It Works!

**It was working!!**

Wow, such a good feeling.

After playing around a bit, I did find a few bugs that I will need to update, including:

- Reducing load times from the sign in and register pages
- Adding a loading state to sign in and register as it takes a moment to log the user in
- Updating the favicon, which is still the built-in react app favicon
- Fixing the bounding box as the bottom line extends to the neck instead of ending at the chin of the faces in the images
- Fixing a button text issue on mobile. On my iPhone SE, the "Detect Faces" text in the button under the image URL form on the user's home page does not display. The button is present and working, but the text is absent
- Time permitting, figure out a way to use localStorage to persist the logged-in user on refresh

If you'd like to play around, you can visit [the site](https://facefinder-gycy.onrender.com)!

While I will need to address those bugs, I'm so excited to finally have accomplished this significant feat. Every win helps me feel a little more confident in my abilities, so I'll take the win today 🙂
