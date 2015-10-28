---
layout: post
title: What Happens in Four Years
category: writing
description: "A lot has happened since I built the last iteration of my portfolio in 2011. Here's a look at some of the decisions I made when rebuilding my portfolio for the modern day."
---

A lot has happened since I built the last iteration of my portfolio in 2011. Looking back at it, I see a time capsule of web development four years ago. Web typography was still just taking off with Cufon and sIFR were the de facto methods of custom typefaces. Wordpress was your only option for a blogging platform. Pixels were still something you can discern on a screen and websites were built for a single dominant width.

Fast forward to present day and the playing field has completely changed. @font-face has taken off and [font](https://typekit.com/") [hosting](http://www.webtype.com/") [services](http://www.typography.com/") offer robust and legal means of beautiful web typography. The mobile market explosion has mean that [responsive web design](http://alistapart.com/article/responsive-web-design") is the only way to work these days. Retina screens are a thing and we now have to hack our way around [responsive images](http://alistapart.com/article/responsive-images-in-practice"). Static site generators have become a popular means of serving up performant websites. Transitions and animations have helped to make the web more fluid and interactive. And, of course, pre-processors like [Sass](http://sass-lang.com/") and [LESS](http://lesscss.org/") exist (how did we ever work without them?).

I’ve been keeping up with a lot of these changes at my previous job at [Inkling](https://www.inkling.com/") and was delighted to finally have the time and opportunity to update my portfolio to modern web standards. I wanted to share some of my decisions here.

## Website Platform

For the last 4 iterations of my portfolio, I used Wordpress. It served me well over the years but I decided I finally needed to ditch it as it offered way more power and way less performance for what I needed in my personal site. I found that for my basic purposes, [Jekyll](http://jekyllrb.com/") provided all the functionality I needed and it also allowed me to host my website on GitHub. I have found it super intuitive to use and way more performant.

## Responsive Images

With more and more views coming in from mobile devices over cellular data, the size of images are a [huge concern](http://timkadlec.com/2013/06/why-we-need-responsive-images/") both in terms of data transfer speed and processing power of those devices. This is especially true when you also take into account retina screen optimized images. Luckily, there are responsive image solutions with <code>srcset</code> and <code>&lt;picture&gt;</code> element and, while these are still far from widespread support, polyfills exist so that we can use them today.

For my current portfolio, I utilized the [picturefill.js](https://github.com/scottjehl/picturefill") and the [Jekyll Picture Tag](https://github.com/robwierzbowski/jekyll-picture-tag") plugin. It was amazing how easy it was to set up and, as Jekyll was compiling my site, my jaw dropped at how much time I would have had to spend creating all the image size variations by hand. The most satisfying aspect was noticing how much it improved site loading speed across devices.

## Hosting

Instead of going with custom hosting, I decided to host my website on [GitHub Pages](https://pages.github.com/") this time around. I was already using it for version control and it made sense to keep it all in one place, especially since it supports Jekyll. The one trade off with Github Pages is that it doesn’t allow third party Jekyll plug-ins which meant that I couldn’t rely on GitHub’s server-side Jekyll compiler to generate my site. As a small inconvenience, I am now hosting my source website in one repo and rsyncing it to my compiled website in another. It’s a little frustrating but totally worth the responsive images.

## Styling

I do all of my work in Sass these days and I can’t imagine having to ever write vanilla CSS again. The use of partials, variables, and mixins have allowed me to keep my CSS DRY and well-structured. Of course it’s important to keep in mind what your compiled CSS looks like and to make sure you don’t go overboard with selector nesting. For this purpose, I use my former colleague Tom Genoni’s [css-dig](http://cssdig.com/") chrome extension to keep myself in check.

Everything is built responsively so that the website should be a pleasure to read no matter what device you are on. CSS animations and transitions help to make interactions more smooth and obvious.

In terms of browser prefixing and a flexible grid system, I opted in for [Bourbon](http://bourbon.io/") and [Neat](http://neat.bourbon.io/") from the guys at [Thoughtbot](https://thoughtbot.com/"). It’s an elegant and lightweight library that does what I need and doesn’t come with the rest of the cruft. Bourbon also plays better with Jekyll’s built in compiler than Compass does.

## Web Typography

I’ve always been in love with the typefaces from [Hoefler &amp; Co](http://www.typography.com/"). I’ve used their typefaces in a lot of my print work and work at Inkling and finally decided to bite the bullet to personally pay for their webfont service. The typefaces used are [Mercury](http://www.typography.com/fonts/mercury-text/overview/") and [Whitney](http://www.typography.com/fonts/whitney/overview/") - a pairing I’m absolutely obsessed with right now. My only complaint with this service is that you certainly have to sacrifice a bit of performance for beauty.

Phew. That’s it for now and I’m pretty proud of the technology stack that I’ve used to build this website. There’s no sign that the industry of web development is slowing down and I can’t wait to see what will change in the next four years. Personally, I’m hoping to see more of a convergence between web design and native app designs. I believe natively digital conceptual models like Material Design are here to stay and the capabilities of web design will need to catch up.
