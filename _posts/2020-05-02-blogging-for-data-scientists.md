---
title: "Blogging for Data Scientists: Moving Away from Medium"
summary: "Thoughts and reflections on writing technical blog posts using fastpages and GitHub"
toc: true
comments: true
author: Prashanth Rao
categories: [general]
hide: true
search_exclude: false
permalink: /blogging-for-data-scientists/
---


I recently began using [fastpages](https://github.com/fastai/fastpages), a blogging platform based on GitHub Pages and Jekyll, that makes it easier to write technical blog posts using Jupyter notebooks. Over the years, I'd become accustomed to the familiarity and simplicity of Medium. While migrating to a self-hosted service can be quite intimidating for someone used to off-the-shelf solutions, I decided to go ahead and do it anyway (once I learned how simple it was to do using fastpages). I also began thinking about what it is that makes me blog in the first place. And the more I thought about it, the more I realized Medium wasn't the right platform for me any more. If you're a Data Scientist, or anyone in computing who likes writing blog posts involving code snippets, seriously, please, reconsider using Medium as your default option. 


## What's wrong with Medium?
Okay, so you already have a Medium account, and you've been happily publishing posts for months without any problems. But if you just step back for a moment and think about it, you'll see there are a number of problems.

### Free isn't free
As a data scientist and otherwise computer-savvy person, you'll have spent countless hours on stackoverflow and other blogs, all of which provided you that knowledge for *free*. No strings attached (alright, some of them did come with ads, I'll admit). On the other hand, Medium's exasperating drive to promote starred posts that are behind a paywall, has proven it's doing the exact opposite. Your posts will be pushed to the top of its recommendation list if it has the most click-baity, contrarian title, commonly used tech jargon, and of course, the famous **⭐** icon. If most Data Science and computing-related posts on Medium were written by people who acquired their knowledge (largely) through free portals, why should Medium be a gatekeeper to spreading more knowledge in this space? 

Note, I say this *having been a paid subscriber* to Medium for more than two years. As time went on, I found myself getting less and less value from my subscription. Yes, I'm aware that one can view paywalled Medium articles for free in incognito mode, but the sheer inconvenience of having to bypass a paywall each time I need to take a quick glance at possibly useful information is a huge disincentive on its own. Not to mention the annoyance of having to see that "subscribe to Medium" message every time I open a post (I know, because I've been there, done that and and **still** not changed the world)!

### Poor user experience with code-formatting
Because Medium wasn't written from the ground up to support code-filled blog posts (including inline code-formatting was a [mere afterthought](https://medium.engineering/inline-code-cc32ff2d463)) - this leads to a lot of Medium posts being written with just bland code snippets, without syntax-highlighting. This places a significant burden on the writer to convert individual blocks of [code to GitHub gists](https://sigdelsanjog.com.np/github-share-github-gists-on-medium/) and embedded into a Medium post for a decent-looking snippet that can be read and understood easily. Most writers of posts choose *not* to use gists (due to the inconvenience factor, or simply because they are unaware), instead publishing code snippets using the inbuilt code formatter without syntax-highlighting, making it a poor user experience from both the reader's *and* writer's perspective.

### Non-existent support for mathematical symbols
You're limited to posting ugly images of mathematical symbols and equations on Medium. While this may look okay at the time of writing your post, it's almost guaranteed to lose quality once it's rendered onto Medium's template and viewed on a host of different devices (try loading a math-heavy Medium post on a device with dark-mode enabled). Quality aside, it's generally considered poor practice to post mathematical symbols as images ([for accessibility reasons](https://www.washington.edu/doit/how-do-i-create-online-math-content-accessible-students-who-are-blind)).


### Reliance on a single platform for content
As Medium's user base has grown, more and more people are writing content for the top publications (in Data Science and machine learning), which is not in itself a bad thing. However,  encouraging users to subscribe to a publication and providing a "one-stop-shop" for all things Data Science/ML-related means that users are pigeon-holed into obtaining their information from a single website. In the long run, great information is self-selected by a decentralized system (such as Google's search algorithm), so it's highly likely that your post will show up at the top of a relevant Google search anyway. 

> Note:  From my experience writing on Medium for Data Science-related topics, most traffic in the longer term comes through Google searches and external referrals, so why not just publish high-quality posts with insightful, relevant content on your own blog instead?


## `fastpages` - what does it offer?
For those of you who are intimidated by building your own blog site and hosting it (for free), `fastpages` ([built by Jeremy Howard and Hamel Husain](https://fastpages.fast.ai/fastpages/jupyter/2020/02/21/introducing-fastpages.html)) lets you do all of this from within the comfort of GitHub. Because it's based on [GitHub Pages](https://pages.github.com/) - a free service that lets you build and host your own website, it doesn't come with any hidden baggage (all you need is a GitHub account, which you'll already have, or will consider getting if you're coding on a regular basis). 

Jeremy provides a summary in his Tweet thread (with the linked blog post inside): 

> twitter: https://twitter.com/jeremyphoward/status/1232059428238581760?s=20

But in addition to those points, here are a few more reasons why you should consider using your own blog site.

### Pre-built user interface
A large part of the hassle of building your own blog site is designing and implementing your own UI. With `fastpages`, all the initial heavy lifting is done for you - a more than decent UI is provided by default, which contains all the essential components that one might ask for in a personal blog site:

* Ability to use a personal domain name (`myname.dev`) instead of `myname.github.io/blogname`
* Cleanly organized posts with image previews
* An "About" section describing who you are and your background
* Tags for searching blog posts by topic
* Badges that link visitors to your GitHub/Twitter pages


### Ready-made code formatting and syntax-highlighting
Posts in `fastpages` are written in directly in a Jupyter notebook, or using regular markdown, using a feature-rich editor (like [VS Code](https://code.visualstudio.com/docs/languages/markdown)). Depending on the language you're highlighting, it's a walk in the park to include code snippets that look exactly as you intended them to.


### Support for LaTeX-style equations
`fastpages` goes the extra mile and allows you to type in LaTeX-style mathematical symbols and equations, rendering them on your blog for you. This works with inline as well as stand-alone equations.

Example inline equation: $\alpha + \beta = \gamma$


### Keeps code and the related blog all in one place
Because Jupyter notebooks are essentially self-documenting blog posts themselves, `fastpages` turbo-charges their use by offering custom syntax hints to directly publish a Jupyter notebook as a blog post (using an extension of the [`nbdev`](https://github.com/fastai/nbdev) project). This is extremely useful, because it essentially reduces the labour of describing your Data Science workflow and experiments by allowing you to document your thought process *along with the code* itself. This is a radical shift from the way you'll have been conventionally blogging about such workflows (e.g. via Medium), where you'll have had multiple browser tabs open for copy-pasting code, GitHub gists and more. 


#### Additional thoughts: My own experience blogging with notebooks

Personally, this is one aspect of using `fastpages` that has changed the way I think about blogging. Earlier, writing a blog post was always a significant upfront planning effort on my part - I'd lay out snippets of code that I'd need to publish in the blog beforehand. Then, I'd painstakingly create GitHub gists for each snippet so that I could embed them into my Medium post in between parts of the workflow where I was trying to explain a point. With notebooks, the whole process is organic, because you're testing code snippets on the fly *along with the text for your blog* side-by-side! 

Even when using pure Markdown to write a blog post (as I did with this one), it's as simple as working in a text editor and using `nbdev` syntax to render effects such as highlighted tips and code folding (as shown in the [original blog post](https://fastpages.fast.ai/fastpages/jupyter/2020/02/21/introducing-fastpages.html)).


## Examples of customizing `fastpages`

### Change syntax-highlight colours

### Change the default font-size

### Adding the *Disqus* comment system

### FAQs

#### What about viewership? Will I get significantly fewer readers?


#### Won't my productivity be affected if I have to make a commit each time?
If you're writing blog posts about data-manipulation workflows with code snippets, it's very likely you're already committing the code *somewhere*. Also, if you're looking to increase your credibility in the field by publishing insightful, thought-out software development workflows, committing your blog to GitHub can only bring you more brownie points (by having an active commit history). 

#### Can I save drafts of my post before actually publishing it?


## Conclusions

### Why do you write blog posts in the first place?

I've learned firsthand that writing about complex technical workflows cements those concepts in my brain. The more you do it, the better you become at conceptualizing those workflows for new, unseen situations. Using a service like Medium offers you *the wrong reward functions* - that is, to increase viewership and receive more "claps". Again, from my firsthand experience, having a decent number of claps on a Medium post did nothing to enhance my portfolio (after a point, receiving a clap meant nothing). Real jobs in the real world come from networking and talking to the right people, and a large part of that is how you *communicate* your thought process. What better way to do so than getting your ideas out there in your own blog, without the pressure of virtual "pats on the back" from an online system! 

> Note: Online abuse and toxicity is a very legitimate concern, so disabling comments on your posts using `fastpages` or any other service is a valid, viable option for many.

The goal of writing a technical blog post, in my view, should be to provide at least *some useful insight* to the reader. Even if it just benefits five people in the entire world, that's a worthy reward in itself - because it is knowledge that was likely gained through a free and open portal (such as someone else's blog), and is shared with someone else through another free portal (this also aligns well with the [overall goals of the world wide web](https://webfoundation.org/about/vision/history-of-the-web/)). 

The key to writing good posts is to find a reward function that works for *you*.


### Where to from here?
- In the long run, you're not tied to hosting on GitHub and using `fastpages` - you can save the intermediate Markdown generated in the backend, so you can always migrate to another service if you choose to.
- As you upskill, you'll find better ways to add new features, colours and functionality to your blog, and eventually, you'll not be limited to relying on someone else's template. 


