# Styleguide-Driven Development

--

## OR

--

# Design as a Dependency

---

### Chris Coleman  
Senior Web Developer  
AAAS/<i>Science</i>

[github.com/freshyill](https://github.com/freshyill)  
[@freshyill](https://twitter.com//freshyill)

---

## Design tends to drift

![Drift](img/drift.gif)

Note: This isn't the huge problem it once was. We're all using source control these days. That's the biggest thing you can do to keep design in check on a single site.

But what if you're *not* building a single site? It's completely common for one site to be composed of several different applications. The example I'm going to focus on, however, is when you have one design that powers multiple sites.

---

## Machines to the rescue

![Iron Man 1](img/tank.gif)

--

### Sass

![Sass](img/sass.png)

Note: This is *hardly* a new technology at this point. But it is still exciting and constantly evolving. For many developers, Sass started out as a way to avoid design drift. The variables in Sass are one of the easiest things to grasp, especially when you're not coming from a programming background. Anybody has ended up with a slightly-off shade of red can appreciate the power us just saying `color: $highlight` instead of trying to remember an RGB or hex value.

--

### Pattern Lab

![Pattern Lab](img/pl.gif)

Note: You've heard of this, right?

This can't *possibly* be the first time you've heard of Pattern Lab. I've seen plenty of presentations on it—some are good, some are kind of "meh". Pattern Lab is just one of the things I'm going to touch on in this talk. It's an important part of *my* workflow, but there are alternatives.

--

### Gulp

![Gulp](img/gulp.png)

Note: You've heard of this too, right? Gulp can do pretty much anything. You could just as easily use Grunt for all this, but I prefer Gulp.

--

### BrowserSync

![BrowserSync](img/bs.png)

Note: You've heard of this too, right? It's basically a thing that automatically (and very quickly) reloads changes in your browser, and keeps multiple browsers in sync. It's invaluable for building responsive designs.

Incendiary opinion alert: This is way better than LiveReload.

--

### Jenkins

![Jenkins](img/jenkins.svg)

Note: If you're not familiar with Jenkins, it's a continuous integration tool. Generally, it's always running and waiting for your code to show up so it can build it and deploy it. There are many other similar tools such as Hudson and Travis CI. You can also press a button to run a build.

Fair warning: Jenkins is getting into next-level territory for a CSS presentation. I'm not a Jenkins expert, and this is where my own examples will get a little less precise. But you don't need to be an expert. The cooperation of your friendly neighborhood devops engineer will probably be necessary for the last mile of this workflow. If Jenkins isn't an option, the Gulp workflows I show you will help get us pretty close.

---

## A real life example

![David](img/david.gif)

Note: So now it's time to look at a real life example.

--

## Science Redesign

Note: Since 2007 or so, Science has only seen evolutionary design changes, including a small homepage refresh we launched just over a year ago.

--

## Out with the old

<div class="screenshots">
  <img src="img/thumb-oldscience.jpg" alt="Old Science" class="fragment" data-fragment-index="1">
  <img src="img/thumb-oldnews.jpg" alt="Old News" class="fragment" data-fragment-index="2">
</div>

Note: Believe it or not, this won a design award. We rushed this out, and in many ways it shows. A contractor put this together while we launched a small redesign on our news site.

But now we're back to design drift. These sites were both designed by the same guy, but there's lots of things that are just *a little bit off*.

These sites are built on completely different platforms. One is Drupal, which is often an uphill battle to get things *just right*, and the other is a legacy journal platform, which makes Drupal look like an absolute dream for a front-end developer, by comparison.

We knew this wasn't exactly what we wanted, but we learned to live with it because we knew it had a very limited lifespan.

--

## In with the new

<div class="screenshots">
  <img src="img/thumb-science.jpg" class="fragment" data-fragment-index="1">
  <img src="img/thumb-signaling.jpg" class="fragment" data-fragment-index="2">
  <img src="img/thumb-stm.jpg" class="fragment" data-fragment-index="3">
  <img src="img/thumb-advances.jpg" class="fragment" data-fragment-index="4">
  <img src="img/thumb-blogs.jpg" class="fragment" data-fragment-index="5">
  <img src="img/thumb-ghp.jpg" class="fragment" data-fragment-index="6">
</div>

Note: As soon as we launched that design, we started on the new one. And unlike the last one, it wasn't just a coat of paint. This was an entirely new house. Or six new houses, to be more precise.

Scholarly publishing is not like regular publishing. It's not just a matter of putting some content into a CMS and hitting the publish. Content needs to be converted into very specific formats, and there are a lot of very precise metrics involved. So we rely on various vendors to help us with this. Our scholarly content is hosted with a vendor, but many other parts of our web site are built with more familiar technologies, primarily Drupal and WordPress.

The design process leading up to the implementation of this redesign was anything but modern. You know the joke about homepage-final-revision-6-final-FINAL.psd—well, well it's not a joke. That's what we were given. And that's what our vendor was given. Stacks and stacks of PSDs. So while we started implementing these PSD comps on our homepage and blog sites—using Drupal and Wordpress, our vendor started implementing the same designs on their specialized Drupal platform.

It wasn't far into the implementation before we realized our vendor was having problems. The first site using the redesign launched during the AAAS Annual Meeting in February. There was a board meeting happening at the time of the launch, and when the board members tried to open the newly-launched Science Advances site on their phones, the results weren't pretty. It was completely unusable on mobile devices.

But I had a solution…

---

## Pattern Lab to the rescue

![Science PL](img/science-pl.png)

Note: From the very start, I had gone all-in on a Pattern Lab and Gulp-based workflow. Our vendor got their best front-end developer on the job and we started working closely together. She forked my Pattern Lab project and she began making pull requests to implement elements that I hadn't needed to create yet. Within about two weeks, we had ported the entire design to our vendor's Drupal theme.

This worked because we were using the very same CSS codebase.

--

## Get to know your design

![War Room](img/war-room.jpg)

Note: I hate to bring ink and paper into this, but it can be useful to have something physical to help you really understand what you're getting into.

--

## Getting started

<div class="whiteboard">
  <img src="img/whiteboard-1.jpg" alt="Whiteboard 1" class="fragment" data-fragment-index="1">
  <img src="img/whiteboard-2.jpg" alt="Whiteboard 2" class="fragment" data-fragment-index="3">
  <img src="img/whiteboard-3.jpg" alt="Whiteboard 3" class="fragment" data-fragment-index="2">
  <img src="img/whiteboard-4.jpg" alt="Whiteboard 4" class="fragment" data-fragment-index="4">
  <img src="img/whiteboard-5.jpg" alt="Whiteboard 5" class="fragment" data-fragment-index="5">
  <img src="img/whiteboard-6.jpg" alt="Whiteboard 6" class="fragment" data-fragment-index="7">
  <img src="img/whiteboard-7.jpg" alt="Whiteboard 7" class="fragment" data-fragment-index="6">
  <img src="img/whiteboard-8.jpg" alt="Whiteboard 8" class="fragment" data-fragment-index="8">
  <img src="img/whiteboard-9.jpg" alt="Whiteboard 9" class="fragment" data-fragment-index="9">
  <img src="img/whiteboard-10.jpg" alt="Whiteboard 10" class="fragment" data-fragment-index="11">
  <img src="img/whiteboard-11.jpg" alt="Whiteboard 11" class="fragment" data-fragment-index="10">
  <img src="img/whiteboard-12.jpg" alt="Whiteboard 12" class="fragment" data-fragment-index="12">
  <img src="img/whiteboard-13.jpg" alt="Whiteboard 13" class="fragment" data-fragment-index="13">
  <img src="img/whiteboard-14.jpg" alt="Whiteboard 14" class="fragment" data-fragment-index="15">
  <img src="img/whiteboard-15.jpg" alt="Whiteboard 15" class="fragment" data-fragment-index="14">
  <img src="img/whiteboard-16.jpg" alt="Whiteboard 16" class="fragment" data-fragment-index="16">
</div>

Note: Remember all those PSDs I mentioned?

The very first order of business is to make sense of them! A little bit of planning goes a long way. If you are going to be the steward of a design, you need to truly *understand* it.

If you're implementing a design that was given to you after going through a "legacy" design process—that is, one with lots of PSDs, you're going to quickly start to notice inconcistencies.

Knock these out. Seriously.

Make an executive decision or get an answer out of your designer and decide which is the right one. In a large enough project, you're going find plenty of elements that either don't have a clear purpose, or serve essentially the same purpose as another element. Don't create more elements than you need to. Every one-off element adds overhead to your project. Do you really want to maintain three different carousels or tabbed elements? If it turns out the similar-but-different elements actually have different *meanings*, then build both—but understand the differences and document them. Pattern Lab provides methods to help you easily create and maintain variations on elements, when you know you need them.

The next order of business is to get these things into Pattern Lab. I could go on and on about the details of using Pattern Lab, but that's already been done plenty of times, and besides that, the documentation is excellent. I'm going to discuss it, but I won't get too far into the weeds.

---

## Using Pattern Lab

![Pattern Lab](img/thumb-patternlab.jpg)

Note: So let's talk about Pattern Lab. Pattern Lab is really easy to use. There's a learning curve, but you can be productive in pretty much no time.

Dave and Brad tell you that you should start by tossing the demo files. Before you do that, study them a bit. It's the best resource you've got to help you understand how all of this is put together. Even though you should pull them out of your project, you should consider keeping a copy of them handy to refer back to.

---

## Gulp time

    $ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    $ brew install node
    $ npm install -g gulp

Note: So you've got Pattern Lab installed. Remember how we're pulling pretty much everything out of it? Well, we need to replace it with something. And in this case, we're starting with the styles. And because we're not savages, we're using Sass.

You might already be familiar with Gulp. If not, don't worry. It's not hard to get up and running. Here it is in just a few commands.

Without getting too detailed, what we're doing here is installing Homebrew, Node and Gulp.

--

![Fork](img/mermaid.gif)

    $ npm install

####[sdd-pl-demo](https://github.com/freshyill/sdd-pl-demo)

Note: We're on the cusp of turning this into a Node project. Normally you'd start a Node project by typing `npm init`. You could do that, but I've got a starter project on GitHub for you to fork. Fork it, pull it down locally, type `npm install`, and you should be all set.

This is going to be out of date as soon as Dave Olsen makes a change to Pattern Lab. So while you probably don't want to use this repository to start your own projects, you can still use the package.json, Gulpfile, and a few other things to help get you started.

--

## Wait&hellip; what?

<code class="fragment">

    $ gulp

</code>

Note: Yeah we just did a whole lot. Let's recap: You've got a Pattern Lab site, with Gulp, Sass and BrowserSync all set up.

These things aren't terribly difficult to get up and running, but this basic Gulpfile gives you a few common things to help you get up and running. I've already taken the liberty of installing the Pattern Lab demo files, but I deleted all of the styles and replaced them with the necessary files to get started with Sass.

Now, all you need to do is type `gulp`.

Let's check it out in action.

---

### Demo time

Note: [Show Sass/BrowserSync in action]

---

![Unimpressed](img/unimpressed.jpg)

Note: OK, that was pretty basic. Let's do something a little more interesting.

--

## Try this

    $ gulp --projectA

<span class="fragment">Or this</span>

<code class="fragment">

    $ gulp --projectA --projectB --projectC

</code>

Note: Now we're getting somewhere. We're using `gulp-util` to tack on some flags to our gulp command.
