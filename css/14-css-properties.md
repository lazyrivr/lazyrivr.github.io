---
layout: default
title: 14 CSS Properties to Get You Started
section: css
---

# 14 CSS Properties to Get You Started

*This article is based on [Brother Judkins' "21 CSS Properties To Get You Started"](http://brotherjudkins.com/code/introcss.html). I try to expand a bit on it.*

While there are many CSS properties, there are a few you'll be using very often. Below I've made a few categories so it should be easier for you to find what you're looking for!

## Typography

One of the most powerful ways to make your website stand out is with some great typography. Look at the typical webpage: it's full of words. Making those words easy to read and beautiful will make your site stand out from the crowd.

### font-family

font-family determines what font your text is in. Here's how you write it:

    font-family: fonts in your preferred order

Generally speaking, the fonts you list here are going to need to be on the user's computer ([though that's not always true](#)). Of course, you don't have control over which fonts your visitors have and it's certainly unreasonable to expect them to go out and install a font just to make your site look better. That's why you specify a list of fonts you want to use: that way you have some backups! Here's an example:

    font-family: Arial, Helvetica, sans-serif;

In this example, Arial is the font that should be used first. Most people have Arial, so this is a pretty safe choice. However, some users may not have Arial (for example, some Macs). If the user doesn't have Arial, the browser will use Helvetica if they've got it.

But what about that last part? You should always finish with either "sans-serif" or "serif". This is the last resort option. The browser will choose the most generic, default font it can find of that category. That way it will at least look correct-ish. For a list of the "web safe" fonts that are on most people's computers, check out [this article at w3schools.com](http://www.w3schools.com/cssref/css_websafe_fonts.asp).

### font-size

font-size does exactly what it says: it changes how big your text is. It's used like this:

    font-size: size;

You can either use a numerical value or a keyword. The valid keywords are: xx-small, x-small, small, medium, large, x-large, xx-large, smaller, and larger.

You don't see the keywords used a lot though. Generally you want to use some kind of number with a unit of measure, like this:

    font-size: 2em;

There's a lot of [different ways to measure things in CSS, so check out this article](#).

### font-style

Want to make your text italic? This is how you do it:

    font-style: italic;

Have some italic text you need to make non-italic? Just do this:

    font-style: normal;

### font-weight

You actually have a surprising number of options with font-weight, but there are only two you'll really use. To make your text bold do this:

    font-weight: bold;

If you have some bold text that you need to turn normal, just do this:

    font-weight: normal;

### text-align

Just like the text alignment options you have in a word processor, you can align text on your webpages. You have three main options: center, left, and right. Here's how you write it:

    text-align: right;

As you'd guess, this makes your text right aligned. However, this may not always work like you'd expect. This is due to the way that CSS layout works, so you may need to experiment.

### text-decoration

Decoration may not be quite what you think it is. This is mostly about lines, and where they are. This is how you underline stuff.

    text-decoration: underline;

This is what you'll mostly be using it for. Here are your valid options: underline, overline, line-through, none. None is the important one here. By default, links are underlined. If you don't want them to be, you can change that with this:

    text-decoration: none;

### text-indent

text-indent indents text. Makes sense, right? It's important to note that it only indents the first line of text, like you might do for each paragraph in an essay. This is also often used to move text without moving its containing box. Write it like this (and [read about the different units of measurement you can use](#)):

    text-indent: measurement;
    /* Practical example: */
    text-indent: 20px;

### text-transform

Sometimes you might want things to be all capitalized for effect. BUT DON'T TYPE IN ALL CAPS LIKE THIS! You can use CSS to achieve the same thing!

    text-transform: uppercase;

You have 4 options for this:

* none: this is the default. It leaves your text exactly like you wrote it.
* uppercase: THIS MAKES ALL THE TEXT UPPERCASE. EVERY SINGLE LETTER.
* lowercase: this makes all the text lowercase. every single letter.
* capitalize: This Generally Makes Every First Letter Of Every Word Uppercase.

### letter-spacing

This changes how much space is between each letter. Sometimes adjusting the letter spacing can make your text so much easier to read, especially if the font is a little crowded. You'll want to refer to [units of measurement](#) to know how to write it:

    letter-spacing: measurement;
    /* Practical example: */
    letter-spacing: 0.2em;

### line-height

line-height is one of the most underused properties in CSS. Increasing the line height from its default can make text look so much better than the default. line-height changes how tall each line is, but it doesn't affect the actual size of your text. Instead, it serves to add additional space between each line of text. For this, you'll generally just use a number. 1 is the default. Try 1.2 (think of it as 120% of default) as a starting point!

    line-height: 1.2;

### color

color is how you set the color of your text (though it also affects a few other things). There's a few [different ways to define the color](#), but the basics of writing the color property are easy:

    color: #ffffff;
    /* that color is pure white */

## Backgrounds

Let's start putting decoration *behind* your content! This can really starting to bring some color into your page and make it look great! On this site, I mostly use background colors as the decoration!

### background-color

background-color sets a color as the background for whatever you've selected. There are several different ways to define a color, so you'll want to read up on that. By default, a page's background is white, but it is possible to change that default, so you'll want to set a background color, even if it is white.

    background-color: #000000;
    /* that color is black */

### background-image

You can also use an image as your background! There are some things you'll want to pay attention to though! By default, the image will repeat until it completely fills the space it has. You should try to use an image that will "tile," or, in other words, won't have any visible seams when repeated. (You can change the repeating behavior with background-repeat.) Let's take a look at how it's written:

    background-image: url(images/cssbg.png);

You need to tell the computer where the image you want to use is. You do that with url(), and inside there you put the path to the image, just like you would in an href attribute in HTML. The path is not relative to the webpage, but to where the CSS is. So if your page is at http://comm310.com/css/properties.html, but your CSS is at http://comm310.com/style.css, it would look for the image at http://comm310.com/images/cssbg.png, not http://comm310.com/css/images/cssbg.png.

## list-style

You know how your lists have those little dots or numbers? You can change those! First, let's change how they're positioned:

    list-style: inside;
    list-style: outside;

The best way for me to explain these is to have you try them out. Outside is the default and it keeps the number or dot separated from the text. Inside keeps them together. In particular, if your list item is more than one line long on the page, the text doesn't look indented.

You can also change the look of the dots or numbers:

    list-style: disc;
    /* this is the default for unordered lists */
    list-style: decimal;
    /* this is the default for ordered lists */
    list-style: circle;
    /* this creates an unfilled circle */
    list-style: square;
    /* this creates a filled circle */
    list-style: lower-roman;
    /* lowercase roman numerals */
    list-style: url(images/bullet.png);
    /* you can also use an image! */

For the different pre-defined options, check out this [list-style-type article on w3schools.com](http://www.w3schools.com/cssref/pr_list-style-type.asp).

The color matches the color of your text, so to change the color, use [color](#color).

## Where Do I Go From Here?

There are still some important CSS properties you'll use a lot that you need to know, but they deserve their own article because you need to know about boxes, so go check out the CSS box model to learn how your browser lays your webpage out!

* The CSS Box Model

You'll also be using floats a lot, but those also deserve their own article!

* Floating Things

*Confused? [Tweet me](https://twitter.com/lazyrivr) and I'll try to help (and make this page more clear)!*