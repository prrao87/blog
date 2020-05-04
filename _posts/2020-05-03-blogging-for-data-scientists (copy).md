---
title: "Blogging for Data Scientists: Moving Away from Medium"
description: "Thoughts and reflections on writing technical blog posts using fastpages and GitHub"
toc: true
comments: true
layout: post
image: "images/posts/laptop.jpeg"
author: Prashanth Rao
categories: [blogging, learning, fastpages]
hide: false
search_exclude: true
permalink: /blogging-for-data-scientists/
---


![](../images/posts/laptop.jpeg)


I recently began using [`fastpages`](https://github.com/fastai/fastpages), a blogging platform based on GitHub Pages and Jekyll, that makes it easier to write technical blog posts using Jupyter notebooks. Over the years, I'd become accustomed to the familiarity and simplicity of Medium's interface. Although migrating to a custom static blog site is quite intimidating for someone like me who's never done it before, I decided to go ahead with it anyway. I also began thinking about what it is that makes me blog in the first place. And the more I thought about it, the more I realized Medium wasn't the right platform for me any more. If you're a Data Scientist, or anyone in computing who likes writing blog posts with code snippets and discussing workflows, seriously, please, reconsider using Medium as your default option. 


## What's wrong with Medium?
Okay, so you already have a Medium account, are comfortable with its interface, and have been happily publishing posts for months without any problems. But just take a step back for a moment and think about it, and you'll see there are a number of problems.

### Free isn't free
As a data scientist and otherwise computer-savvy person, you'll have spent countless hours on stackoverflow and other blogs, all of which provided you that knowledge for *free*. No strings attached (alright, some of them did come with ads, I'll admit). On the other hand, Medium's exasperating drive to promote starred posts that are behind a paywall has proven its goals are the exact opposite. Your posts will be pushed to the top of Medium's recommendation list if it has the most click-baity, contrarian title, commonly used tech jargon, and of course, the famous 🟊 icon. If most Data Science and computing-related posts on Medium were written by people who acquired their knowledge (largely) through free portals, why should Medium be a gatekeeper to spreading more knowledge in this space? 

Note, I say this *having been a paid subscriber* to Medium for more than two years. As time went on, I found myself getting less and less value from my subscription. Yes, I'm aware that one can view paywalled Medium articles for free in incognito mode, but the sheer inconvenience of having to bypass a paywall each time I need to take a quick glance at possibly useful information is a huge disincentive on its own. Not to mention the annoyance of having to see that "subscribe to Medium" message every time I open a post (I know, because I've been there, done that and and **still** not changed the world)!

### Poor user experience with code-formatting
Because Medium wasn't written from the ground up to support code-strewn blog posts (including inline code-formatting was a [mere afterthought](https://medium.engineering/inline-code-cc32ff2d463)) - this leads to a lot of Medium posts being written with just bland code snippets, without syntax-highlighting. A significant burden is placed on the writer to convert individual blocks of [code to GitHub gists](https://sigdelsanjog.com.np/github-share-github-gists-on-medium/) and embedded into a Medium post for a decent-looking code snippet that can be read and understood easily. Most writers choose not to use gists due to the inconvenience factor (or are simply unaware of how to use them), instead publishing code snippets using Medium's inbuilt code formatter without syntax-highlighting - this makes for a poor user experience from the reader's *and* writer's perspective.

### Non-existent support for mathematical symbols
You're limited to posting ugly images of mathematical symbols and equations on Medium. While this may look okay at the time of writing your post, it's almost guaranteed to compromise quality when viewed on a host of different devices (try loading a math-heavy Medium post on a device with dark-mode enabled). Quality aside, it's generally considered poor practice to post mathematical symbols as images ([for accessibility reasons](https://www.washington.edu/doit/how-do-i-create-online-math-content-accessible-students-who-are-blind)).


### Reliance on a single platform for content
As Medium's user base has grown, more and more people are writing content for its top publications (in Data Science and machine learning), which is not in itself a bad thing. However,  encouraging users to subscribe to a publication and providing a "one-stop-shop" for all things Data Science/ML-related means that users are pigeon-holed into obtaining their information from a single website. In the long run, great information is self-selected by a decentralized system (such as Google's search algorithm), so it's highly likely that your post will show up at the top of a relevant Google search anyway. 


## What does `fastpages` offer?
For those of you who are intimidated by the thought of building your own blog site from scratch, `fastpages` ([built by Jeremy Howard and Hamel Husain](https://fastpages.fast.ai/fastpages/jupyter/2020/02/21/introducing-fastpages.html)) lets you do all of this from within the comfort of GitHub. Because it's based on [GitHub Pages](https://pages.github.com/) - a free service for building and hosting custom websites - it doesn't come with any hidden baggage. All you need is a GitHub account, which you'll already have, or are considering getting if you're coding on a regular basis. 

Jeremy provides a summary in his Tweet thread (with the linked blog post inside): 

> twitter: https://twitter.com/jeremyphoward/status/1232059428238581760?s=20

But in addition to his points, here are a few fundamental reasons why it makes sense to consider using your own blog site.

### Pre-built user interface
A large part of the hassle of building your own blog is designing and implementing a decent-looking UI. With `fastpages`, all the initial heavy lifting is done for you - a more than decent UI is provided by default, which contains all the essential components that one might ask for in a personal blog site:

* Ability to use a personal domain name (`myname.dev`) instead of `myname.github.io/blogname`
* Cleanly organized posts with image previews
* An "About" section describing who you are and your background
* Tags for searching blog posts by topic
* Badges that link visitors to your GitHub/Twitter pages


### Ready-made code formatting and syntax-highlighting
Posts in `fastpages` are written directly in a Jupyter notebook, or in Markdown using a feature-rich editor (like [VS Code](https://code.visualstudio.com/docs/languages/markdown)). Depending on the language you're highlighting, it's a walk in the park to include code snippets that look exactly as you intended them to.


### Support for LaTeX-style equations
`fastpages` goes the extra mile and allows you to type in LaTeX-style mathematical symbols and equations, rendering them on your blog for you. This works with inline as well as stand-alone equations.

Example inline equation: $\alpha + \beta = \gamma$


### Keep code and the related blog explaining it all in one place
Because Jupyter notebooks are essentially self-documenting blog posts themselves, `fastpages` turbo-charges their use by offering custom syntax hints to directly publish a Jupyter notebook as a blog post (using an extension of the [`nbdev`](https://github.com/fastai/nbdev) project). This is extremely useful, because it essentially reduces the labour of describing your Data Science workflow and experiments by allowing you to document your thought process *along with the code* itself. This is a radical shift from the way you'll have been conventionally blogging about such workflows (e.g. via Medium), where you'll have had multiple browser tabs open for copy-pasting code, GitHub gists and more. 


> Note: Additional thoughts from my own experience blogging with notebooks

Personally, this is one aspect of using `fastpages` that has changed the way I think about blogging. Earlier, writing a blog post was always a significant upfront planning effort on my part - I'd lay out snippets of code that I'd need to publish in the blog beforehand. Then, I'd painstakingly create GitHub gists for each snippet so that I could embed them (with full syntax-highlighting) into my Medium post in between parts of the workflow where I was trying to explain a point. With notebooks, the whole process is organic, because you're testing code snippets on the fly *along with the text for your blog* side-by-side! 

Even when using pure Markdown to write a blog post (as I did with this one), it's as simple as working in a text editor and using `nbdev` syntax to render effects such as highlighted notes and code folding (as shown in the [original blog post](https://fastpages.fast.ai/fastpages/jupyter/2020/02/21/introducing-fastpages.html)).

## Some FAQs on using `fastpages`

#### What about viewership? Won't I get significantly fewer readers?
It's important to remember that viewership is just a vanity metric when it comes to personal blogs. It really doesn't matter how many people see your posts on a weekly basis - what matters more is the value you derived by taking the time to write the post in the first place (by applying existing skills and learning new ones). A few readers might take the effort to react or post comments, but almost all are "silent" visitors - this is true regardless of the blogging platform used, so just focus on your own learning and writing skills!

> Note: Having been writing articles on Medium for almost two years, I've noted that Google searches and external referrals are the biggest contributors to new viewers in the long term. Content that is insightful and well-written should inevitably be found via the relevant keyword searches over time.

#### Won't my productivity be affected if I have to make commits on GitHub each time?
If you're writing blog posts involving code snippets, it's very likely you're already committing the code *somewhere*. Also, if you're just starting off in the field and are looking to increase your credibility by publishing insightful, well-crafted software development workflows, hosting your blog on GitHub can only bring in more brownie points (by improving your active commit history). 

#### Can I work on drafts of my post before actually publishing it?
A simple way to do this is to create a new folder `ideas` and simply write your posts in notebooks/Markdown files while committing to this directory. Only posts that are in the `_notebooks`, `_posts` and `_word` directories are published; all posts in other directories are ignored (but are still backed up on GitHub). Another alternative is to use the Front Matter option `hide: true` so that Jekyll doesn't render the post on the web page (see the full description of Front Matter [in the `fastpages` documentation](https://github.com/fastai/fastpages#customizing-blog-posts-with-front-matter)).


## Conclusions

### Why do you write blog posts in the first place?

I've learned firsthand that writing about complex technical workflows cements those concepts in my brain. The more you do it, the better you become at conceptualizing those workflows for new, unseen situations. Using a service like Medium offers you *the wrong reward function*, such as receiving appreciation through claps. It also creates the delusion that having more views (or claps) on your post matters in any tangible way. Real jobs in the real world come from networking and talking to the right people, and a large part of that is how you *communicate* your thought process and showcase your portfolio and skills online. What better way to do this than getting your ideas out there using your own blog site, with its own quirks and colour schemes, and most importantly, *without* the pressure of expecting virtual "pats on the back" from an online system! 

The goal of writing a technical blog post, in my view, should be to provide at least *some useful insight* to the reader. Even if your post just benefits five people in the entire world, that's a worthy reward in itself - because it contains knowledge that was likely gained through a free and open portal (such as someone else's blog), and is shared with someone else through another free portal (this also aligns well with the [overall goals of the world wide web](https://webfoundation.org/about/vision/history-of-the-web/)). 


### Where to from here?
While `fastpages` is a great introduction to deploying and maintaining your own custom site, in the long run, you're not tied to hosting your site on GitHub and the `fastpages` platform. `fastpages` allows you to save the intermediate Markdown files generated for each of your posts, so you can always migrate your blogs to another service if you need to.

If you're a Data Scientist, the great thing about using a tool like `fastpages` is that there's already a [community forum](https://forums.fast.ai/t/fastpages-github-pages-blog-using-nbdev/62828) with questions on commonly faced problems and great answers on functionality. It's never too late to start working on your own blog, so keep writing and happy blogging!

---

## Appendix: Examples on customizing `fastpages`
Even if you don't know all that much about CSS (I don't either), it's not that hard to customize some aesthetics.

### Change syntax-highlight colours
The default version of `fastpages` comes with dark syntax-highlighting for code, based on the popular Dracula theme. If you don't particularly like all the colours in this theme, it's relatively straightforward to customize via CSS. 

In `_sass/minima/custom-styles.scss`, copy  the existing `minima/custom-styles.scss/fastpages-dracula-highlight.scss` file (containing the Dracula colours) and create a new file `custom-code-colors` in the same directory. Point to this new file in `minima/custom-styles.scss` as follows.

```css
/* @import "minima/fastpages-dracula-highlight"; */
@import "minima/custom-code-colors"; 
```
To change the colour definitions at the top, replace the relevant Hex code for the `$dt-purple` or `$dt-pink` colours with new colour shades (VS Code has a really nice [colour picker built-in](https://mspoweruser.com/visual-studio-code-now-really-useful-color-picker-built/)). In my case, I chose a lighter purple definition. Next, I changed the keyword colour scheme under the `.highlight` selector.

```css
$dt-purple: #c792ea;

.highlight {
    .k,
    .o,
    .cp,
    .kc,
    .kn,
    .kp,
    .kr,
    .nt,
    .ow {
      color: $dt-purple;
    }
```
Other properties of the selector can be customized with new colours the same way.

### Change the font and default font-size
If you want to tweak the fonts and font sizes used by `fastpages`, this can be done as follows.

#### Code font
I noticed that on my Linux machine, the code fonts that were being requested were not actually available - this was rendering code in the live blog using sans-serif fonts, which in my opinion looks rather ugly. I changed it to a monospace font (DejaVu Sans Mono) using the same `minima/custom-styles.scss` created in the previous example:

```css
.input_area pre, .input_area div {
    margin-bottom:2rem !important;
    margin-top:1.5rem !important;
    padding-bottom:0 !important;
    padding-top:0 !important;
    background: #323443 !important;
    -webkit-font-smoothing: antialiased;
    text-rendering: optimizeLegibility;
    font-family: DejaVu Sans Mono, monospace;
    border-radius: 5px;
    font-size: 100%;
}
```

#### Main blog font
To change the content font size globally for all blog posts, edit the `minima/fastpages-styles.scss` file. Styles for non-headings are modified using the `post-content` selector:
`
```css
/* make non-headings slightly lighter */
.post-content p, .post-content li {
   font-size: 18px;
   color: #515151;
}
```

### Adding the *Disqus* comment system
The `fastpages` documentation recommends using the *utteranc.es* service within GitHub for ad-free, non-trackable comments. While this is a great, light-weight option to allow users to comment on your post, it does require users to sign up for a GitHub account in order to comment. 

An alternate option is to use *Disqus*, which allows users to sign in using their social Media accounts and post comments instead. However, Disqus isn't ad-free, and does involve some anonymous tracking, so it's worth considering this before going ahead and enabling it for your site.

In my case, I wanted to allow comments from users who may not be comfortable signing up for a GitHub account just for this purpose, so I went ahead and enabled Disqus comments using the instructions [shown here](https://desiredpersona.com/disqus-comments-jekyll/).
