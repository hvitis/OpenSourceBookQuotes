---
title: What's an open source?
image: /images/code.jpg
imageMeta:
  attribution:
  attributionLink:
featured: true
author: hvitis
date: Tue Jun 12 2018 17:50:55 GMT+0100 (IST)
tags:
---

This page is a build of buch of code that is availble to see for everyone on GitHub.
Anyone by editing or adding files to a repository can join and write posts with me.
The posts are written in a **Markdown**, let's run you through some of the basics of editing it. You can see this post [directly on github](https://github.com/stonecircle/ember-ghost/blob/master/blueprints/ember-ghost/files/content/the-editor.md) if you want to see all the Markdown we've used. (don't forget to click the _Raw_ button to see the source).


## Formatting text

The most common shortcuts are of course, **bold** text, _italic_ text, and [hyperlinks](https://example.com). These generally make up the bulk of any document. You can also make headings using `#` at the start of the line (multiple `#` symbols for h2/h3/h4/etc)

With just a couple of extra characters here and there, you're well on your way to creating a beautifully formatted story.


## Inserting images

Images in Markdown look just the same as links, except they're prefixed with an exclamation mark, like this:

`![Image description](/path/to/image.jpg)`

![Computer](https://casper.ghost.org/v1.0.0/images/computer.jpg)

If you want to add images to your Ember Ghost app you can just drop them in the `/public` folder, which you should see if you are running this locally!

_**Important Note:** Ember Ghost does not currently have automatic image resizing, so it's always a good idea to make sure your images aren't gigantic files **before** adding them to your project._


## Making lists

Lists in HTML are a formatting nightmare, but in Markdown they become an absolute breeze with just a couple of characters and a bit of smart automation. For numbered lists, just write out the numbers. For bullet lists, just use `*` or `-` or `+`. Like this:

1. Crack the eggs over a bowl
2. Whisk them together
3. Make an omelette

or

- Remember to buy milk
- Feed the cat
- Come up with idea for next story


## Adding quotes

When you want to pull out a particularly good excerpt in the middle of a piece, you can use `>` at the beginning of a paragraph to turn it into a Blockquote. You might've seen this formatting before in email clients.

> A well placed quote guides a reader through a story, helping them to understand the most important points being made

All themes handles blockquotes slightly differently. Sometimes they'll look better kept shorter, while other times you can quote fairly hefty amounts of text and get away with it. Generally, the safest option is to use blockquotes sparingly.


## Dividing things up

If you're writing a piece in parts and you just feel like you need to divide a couple of sections distinctly from each other, a horizontal rule might be just what you need. Dropping `---` on a new line will create a sleek divider, anywhere you want it.

---

This should get you going with the vast majority of what you need to do in the editor, but if you're still curious about more advanced tips then check out the [Advanced Markdown Guide](/advanced-markdown/) - or if you'd rather learn about how tags work, we've got a overview of [how to use tags](/using-tags/).

## Special formatting

As well as bold and italics, you can also use some other special formatting in Markdown when the need arises, for example:

+ \*escaped characters\*


## Writing code blocks

There are two types of code elements which can be inserted in Markdown, the first is inline, and the other is block. Inline code is formatted by wrapping any word or words in back-ticks, `like this`. Larger snippets of code can be displayed across multiple lines using triple back ticks:

```
.my-link {
    text-decoration: underline;
}
```


## Full bleed images

One neat trick which you can use in Markdown to distinguish between different types of images is to add a `#hash` value to the end of the source URL, and then target images containing the hash with special styling. For example:

![walking](https://casper.ghost.org/v1.0.0/images/walking.jpg#full)

which is styled with...

```
img[src$="#full"] {
    max-width: 100vw;
}
```

This creates full-bleed images in the Casper theme, which stretch beyond their usual boundaries right up to the edge of the window. Every theme handles these types of things slightly differently, but it's a great trick to play with if you want to have a variety of image sizes and styles.


## Reference lists

**The quick brown [fox][1], jumped over the lazy [dog][2].**

[1]: https://en.wikipedia.org/wiki/Fox "Wikipedia: Fox"
[2]: https://en.wikipedia.org/wiki/Dog "Wikipedia: Dog"

Another way to insert links in markdown is using reference lists. You might want to use this style of linking to cite reference material in a Wikipedia-style. All of the links are listed at the end of the document, so you can maintain full separation between content and its source or reference.


## Full HTML

Perhaps the best part of Markdown is that you're never limited to just Markdown. You can write HTML directly in the Ghost editor and it will just work as HTML usually does. No limits! Here's a standard YouTube embed code as an example:

<iframe width="560" height="315" src="https://www.youtube.com/embed/Cniqsc9QfDo?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

