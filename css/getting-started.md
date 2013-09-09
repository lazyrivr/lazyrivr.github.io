---
layout: default
title: Getting Started With CSS
section: css
---

# Getting Started With CSS

By default, HTML looks really ugly. White background, black text, blue links, all in Times New Roman. Sure, it gets the job done (your content is visible), but it's not going to hold people's attention. To do that we're going to need to use CSS. CSS, short for Cascading Style Sheets, is the design part of "web design." It's way different than HTML though, so we need to start by going over how to write it.

## The Parts of CSS

*This part is based on [Brother Judkins' "Anatomy of a CSS Rule"](http://brotherjudkins.com/code/css-anatomy.html). Take a look at it for another couple of examples of CSS.*

Let's break down how CSS is written by taking a look at a couple of example pieces.

    header {
        color: white;
        text-align: center;
    }

    html {
        font-family: 'Open Sans', sans-serif;
    }

Each of those examples are called a **rule**. A complete rule tells the web browser what style to apply to which things. It'll make more sense as we go along.

Let's start by taking a look at the **selector**. In these examples, *header* and *html* are the selectors. This tells the web browser what HTML to apply the style to. There are many different ways to select things, which I get into in this article (coming soon).

Next come **statements**. Statements are a complete little chunk of style, like *color: white;*. In that particular example, the text color would be white. Each statement is ended by a semicolon so the computer knows you're moving onto a different statement. The first example above contains two statements, while the second one only has one. You can use however many statements you want in a rule.

Inside the statements, we have **properties**. In the examples above, the properties used are *color*, which defines text color; *text-align*, which sets the alignment of the text; and *font-family*, which says which fonts to use. There are many different properties you can use in CSS, but you can find a list of 19 of the most useful and common ones here (coming soon). As you can see, most of the available properties make sense, so if your code editor has code completion, you could always try typing what you think it would be and seeing if you're right!

After the properties, we have the **values**. This is what you're defining the properties as. So for *color*, I've set the value to *white*, making the text color white. With *font-family*, I've set it to use a font called "Open Sans," and, if that's not available, to use a generic sans-serif font. Properties and values are separated by a colon.

## Styling Your Pages

There are three different ways to use CSS with your HTML. All three use the same CSS properties. There are situations to use all three, but you will primarily be using the first method because it is generally considered the best way.

### The link Tag

The first way to use a link tag inside the head tag of your document. It will look something like this:

    <link rel="stylesheet" href="style.css">

This tells the browser to look for a file called "style.css" and use that as the stylesheet. Inside this file you will place all of your CSS. This allows you to keep your content (the HTML) and your style (the CSS) separate. This is considered the best method for including your CSS on your site, and should be used unless you have no choice but to use one of the other options. The way it is written above is considered the most modern way to write the link tag, however you might also see it written like below (both are valid):

    <link rel="stylesheet" href="style.css" type="text/css" />

### The style Tag

There's another way to include your CSS, and this one is also included in the head tag of your document. Take a look at this example:

    <style>
    h1 {
        font-size: 2em;
        font-family: Helvetica, Arial, sans-serif;
    }
    </style>

With the style tag, you are including your CSS right in the HTML document itself. You just write the CSS inside of the style tags. This method works, but it is including the style with the content and can be pretty inefficient, so this isn't preferable.

### Inline Style

There's one more way to include your CSS, but this one should be avoided whenever possible.

    <h1 style="font-size: 2em; font-family: Helvetica, Arial, sans-serif;">My First Headline</h1>

With this method you're including the CSS inside of a style attribute right in your HTML tag. Because you're applying it to a specific tag, you only include the statements (no need for the selectors since that's implied). This method should be avoided. This is the exact opposite of separating your content and style, which is one of the reasons CSS was created in the first place. The only time you should use this is if for some reason you can't use either of the other methods.

## Go Forth and Style

Now that you know the different parts of CSS and how to include it on your page, you know enough to start doing some CSS! You may be a little hesitant to start, but let me give you a short exercise to get going on. Here's some HTML to start with:

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>My First Bit of Style</title>
        <style>
        </style>
    </head>
    <body>
        <h1>I'm Going to Style This</h1>
        <p>This page is going to include a little style. I'll look back at this in a few weeks and be amazed that I started out here.</p>
    </body>
    </html>

For this example, I've included some style tags because it's just so simple (might as well not deal with having multiple files). There's 3 things I want you to style. I'll tell you the properties to use. Here they are:

* Change the background color of the entire page to red. The property to use is "background-color".
* Change the heading (h1) to be white and 2em in size (don't worry about what 'em's are yet). Change the text's color with "color" and the size with "font-size".
* Make the paragraph italic (yeah, it'll look weird, but this is just an exercise). You can do this with "text-style".

Having trouble? Something a little less than clear? Something I just plain forgot to cover? [Tweet me: @lazyrivr](https://twitter.com/lazyrivr)