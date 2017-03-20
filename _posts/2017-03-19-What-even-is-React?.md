---
layout: post
title: "What Even is React? Pt. 1: The Ecosystem"
categories: journal
tags: [React, NPM, Babel, Webpack, JavaScript, React Router]
<!-- image:
  feature: sewing.jpg
  teaser: sewing-teaser.jpg
  credit:
  creditlink: -->
---

I began learning React in early March and dove head-deep with Tyler Mcginnis' comprehensive guide to React.  My experience with JavaScript has mostly been in building front end web apps, reading Eloquent JavaScript, and working on toy problems from sites such as Code Wars.  While I knew that React manipulates the view layer of a website, I was introduced to several new tools that I had yet to use: React Router, NPM, Babel, and Webpack.

As a beginner, the leap in tooling was overwhelming.  I made it roughly halfway through the tutorial before I stopped to backtrack and learn more about the ecosystem that React exists within.  I was honest with myself: I was lost in the sauce of the ecosystem.  I knew having a high level understanding of all the tools would allow me to understand the smaller things, so here's what I learned:
#### NPM (Node Package Manager)

  NPM is a great tool for building JS apps.  Seriously, this thing still blows my mind.  NPM stores different JS modules, makes it easy to download different modules, and to upgrade upgrade them as well.  The modules are downloaded into a node_modules folder and tracked in a package.json file.  This allows us to store the package.json file on someplace like Github and then others can use that package.json file to run `npm install` to download depndencies locally.

  NPM also allows script aliases so that long commands can be condensed down to something like `npm run test`.  Neat.

#### React Router

  React Router provides a way to map React components to URLs.  When you are at a URL such as mysite.com, React Router allows you to activate some components such as Main and Home, and as you traverse through the app, different components can be activated.  

#### Webpack

  Webpack allows you to take all your code, do some transformations on it, bundle it into one file, and then spit that file out to a directory.  Up to this point, I had to pay attention to the ordering of the JS files e.g., jquery.js has to come before bootstrap.js.  As apps get more complicated, it's easy to see how this dependency issue can get out of hand.  

  Webpack can also be used on non-code files, making it so you won't deploy an app with missing images or outdated CSS.  You can read more about it in [Andrew Ray's great explanation][Andrew Ray Webpack].

#### Babel

  React is usually written in JSX and since the browser cannot understand JSX, we need something to transform it into regular, old JavaScript.  That's exactly what Babel does and it's used with Webpack in the build step (many JSX files come in, one vanilla JavaScript file comes out).

I feel a lot better about my grasp on the function of these tools and will be diving deeper into the details of how they work.  I hope you have left with a better understanding of the React ecosystem as well.  :smile:

[Andrew Ray Webpack]: http://blog.andrewray.me/webpack-when-to-use-and-why/
