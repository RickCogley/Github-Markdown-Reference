# INTRODUCTION

This is a cheatsheet for Markdown, including GFM or "Github Flavored Markdown" as Github calls it, containing syntax and examples. 

Markdown is originally by John Gruber, and you should read his [original specification](http://daringfireball.net/projects/markdown/). Markdown is ubiquitous at the time of this writing, and is the syntax of choice for many wikis, blogs, forums and website generator applications. Markdown allows you to enter markup in an easy-to-remember manner, for instance using asterisks for emphasis (``**text to be emphasized**``) or pound-signs in front of headers (``### An H3 Header``), and it then takes care of the conversion to HTML markup in in the background.   

**Request**

Please _don't edit this page_. Rather, if you have a suggestion, fork this repository and make a pull request. 

**References**

* [Markdown specification](http://daringfireball.net/projects/markdown/) by John Gruber.
* Github Help Documentation on [Github Flavored Markdown](https://help.github.com/articles/github-flavored-markdown) and [Writing on Github](https://help.github.com/articles/writing-on-github). 
* Repositories regarding Markdown syntax from [dvidsilva](https://github.com/dvidsilva/MarkdownReference) and [adam-p](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).
* Adam Pritchard's [Markdown Here](http://www.markdown-here.com/livedemo.html) demo site, where you can experiment in a kind of "sandbox" environment. 
* Github includes the emoji from [The Emoji Cheatsheet](http://www.emoji-cheat-sheet.com).

## Table of Contents

* [Headers](#headers)  
* [Emphasis](#emphasis)  
* [Lists](#lists)  
* [Links](#links)  
* [Images](#images)  
* [Code and Syntax Highlighting](#code)  
* [Tables](#tables)  
* [Blockquotes](#blockquotes)  
* [Inline HTML](#html)  
* [Horizontal Rule](#hr)  
* [Line Breaks](#linebreaks)  
* [Youtube videos](#videos) 

# MARKDOWN REFERENCE & SHOWCASE
 
<a name="headers"/>
> ## Headers & Body Text
 
To insert header tags (e.g. ``<h3></h3>``) use hash marks followed by the text for the header (``# My H1 Header`` or ``#### My H4 Header``). Don't forget a space after the hash, and leave a carriage return between the header and the body text (you might have to vary this depending upon the site). 

### :octocat: Github Style

GFM treats line breaks in a different way from normal Markdown, treating a single line break (press of the enter key) as a real line break, which is likely what most people intend. The regular Markdown treatment is to require two line breaks between paragraphs, and that takes a bunch of getting used to. 

### :white_check_mark: Syntax

```no-highlight
# H1 Header

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 

## H2 Header

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 

### H3 Header

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 

#### H4 Header

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 

##### H5 Header

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 

###### H6 Header

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 

Alternative styles: 
# H1 Header with Closing Hash Characters #
## H2 Header with Closing Hash Characters ##
### H3 Header with Closing Hash Characters ###
and so on.

H1 Header Alternative "Underline" Style
======

H2 Header Alternative "Underline" Style
------
```
 
### :diamond_shape_with_a_dot_inside: Showcase

#### H4 Header
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

##### H5 Header
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

##### H5 Header
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
 
* * * 
<a name="emphasis"/>
> ## Emphasis
 
Add "emphasis" using asterisks (``_my italics_``) or underscores (``*my italics*``), and "strong emphasis" using double asterisks or underscores (``__my bold face__`` or ``**my bold fact**``). Emphasis gets converted to html ``<em></em>`` tags and strong emphasis to ``<strong></strong>`` tags. This style of markup is semantic (meaning it is meaningful in terms of the structure of the document) and not just cosmetic, and it's where the names of the tags come from. 

### :octocat: Github Style

GFM adds strikethrough to Markdown using double tildes (``~~text to strike~~``) surrounding the text, which equates to html del tags (``<del>text to strike</del>``). GFM also gracefully handles the situation when words contain underscores, as in software development (``some_code_variable``). Furthermore, GFM allows you to emphasize part of a word using asterisks. 

### :white_check_mark: Syntax

```no-highlight
Semantic emphasis, via *asterisks* or _underscores_. Renders as italics.
Semantic strong emphasis, via double **asterisks** or __underscores__. Renders as bold.
Combine emphasis via **asterisks and _underscores_**.
Strike mistaken text using two tildes. ~~Scratch this.~~
Emphasize parts of words using asterisks. You say to*MAH*toe, I say to*MAY*toe. 
```
 
### :diamond_shape_with_a_dot_inside: Showcase

Semantic emphasis, via *asterisks* or _underscores_. Renders as italics.
Semantic strong emphasis, via double **asterisks** or __underscores__. Renders as bold.
Combine emphasis via **asterisks and _underscores_**.
Strike mistaken text using two tildes. ~~Scratch this.~~
Emphasize parts of words using asterisks. You say to*MAH*toe, I say to*MAY*toe.
 
* * *  
<a name="lists"/>
> ## Lists
 
Blah blah (``sample``) blah.
(In this example, leading and trailing spaces are shown with with dots: ⋅)

### :white_check_mark: Syntax
 
```no-highlight
1. First ordered list item
2. Another item
⋅⋅* Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
⋅⋅1. Ordered sub-list
4. And another item.
 
⋅⋅⋅You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).
 
⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
⋅⋅⋅Note that this line is separate, but within the same paragraph.⋅⋅
⋅⋅⋅(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)
 
* Unordered list can use asterisks
- Or minuses
+ Or pluses
```
 
1. First ordered list item
2. Another item
  * Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
  1. Ordered sub-list
4. And another item.
 
   You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).
 
   To have a line break without a paragraph, you will need to use two trailing spaces.  
   Note that this line is separate, but within the same paragraph.  
   (This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)
 
* Unordered list can use asterisks
- Or minuses
+ Or pluses

* * *  
<a name="links"/>
> ## Links
 
Blah blah (``sample``) blah. There are two ways to create links.

### :white_check_mark: Syntax
 
```no-highlight
[I'm an inline-style link](https://www.google.com)
 
[I'm an inline-style link with title](https://www.google.com "Google's Homepage")
 
[I'm a reference-style link][Arbitrary case-insensitive reference text]
 
[I'm a relative reference to a repository file](../blob/master/LICENSE)
 
[You can use numbers for reference-style link definitions][1]
 
Or leave it empty and use the [link text itself]
 
Some text to show that the reference links can follow later.
 
[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com
```
 
[I'm an inline-style link](https://www.google.com)
 
[I'm an inline-style link with title](https://www.google.com "Google's Homepage")
 
[I'm a reference-style link][Arbitrary case-insensitive reference text]
 
[I'm a relative reference to a repository file](../blob/master/LICENSE)
 
[You can use numbers for reference-style link definitions][1]
 
Or leave it empty and use the [link text itself]
 
Some text to show that the reference links can follow later.
 
[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com

* * *  
<a name="images"/>
> ## Images

Blah blah (``sample``) blah.

### :white_check_mark: Syntax
 
```no-highlight
Here's our logo (hover to see the title text):
 
Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")
 
Reference-style: 
![alt text][logo]
 
[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"
```
 
Here's our logo (hover to see the title text):
 
Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")
 
Reference-style: 
![alt text][logo]
 
[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"

* * *  
<a name="code"/>
> ## Code and Syntax Highlighting
 
Code blocks are part of the Markdown spec, but syntax highlighting isn't. However, many renderers -- like Github's and *Markdown Here* -- support syntax highlighting. Which languages are supported and how those language names should be written will vary from renderer to renderer. *Markdown Here* supports highlighting for dozens of languages (and not-really-languages, like diffs and HTTP headers); to see the complete list, and how to write the language names, see the [highlight.js demo page](http://softwaremaniacs.org/media/soft/highlight/test.html).

Blah blah (``sample``) blah.

### :white_check_mark: Syntax
 
```no-highlight
Inline `code` has `back-ticks around` it.
```
 
Inline `code` has `back-ticks around` it.
 
Blocks of code are either fenced by lines with three back-ticks <code>```</code>, or are indented with four spaces. I recommend only using the fenced code blocks -- they're easier and only they support syntax highlighting.
 
<pre lang="no-highlight"><code>```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
```python
s = "Python syntax highlighting"
print s
```
 
```
No language indicated, so no syntax highlighting. 
But let's throw in a &lt;b&gt;tag&lt;/b&gt;.
```
</code></pre>
 
 
 
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
```python
s = "Python syntax highlighting"
print s
```
 
```
No language indicated, so no syntax highlighting in Markdown Here (varies on Github). 
But let's throw in a <b>tag</b>.
```
 
* * *  
<a name="tables"/>
> ## Tables
 
Tables aren't part of the core Markdown spec, but they are part of GFM and *Markdown Here* supports them. They are an easy way of adding tables to your email -- a task that would otherwise require copy-pasting from another application.

Blah blah (``sample``) blah.

### :white_check_mark: :octocat: Syntax
 
```no-highlight
Colons can be used to align columns.
 
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
 
The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.
 
Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```
 
Colons can be used to align columns.
 
| Tables        | Are           | Cool |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
 
The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.
 
Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

* * *  
<a name="blockquotes"/>
> ## Blockquotes
 
```no-highlight
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.
 
Quote break.
 
> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote. 
```
 
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.
 
Quote break.
 
> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote. 
 
<a name="html"/>
> ## Inline HTML

You can also use raw HTML in your Markdown, and it'll mostly work pretty well. 

Blah blah (``sample``) blah.

### :white_check_mark: Syntax
 
```no-highlight
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>
 
  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>
```
 
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>
 
  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>

* * *  
<a name="hr"/>
> ## Horizontal Rule

Blah blah (``sample``) blah.

### :white_check_mark: Syntax
 
```
Three or more...
 
---
 
Hyphens
 
***
 
Asterisks
 
___
 
Underscores
```
 
Three or more...
 
---
 
Hyphens
 
***
 
Asterisks
 
___
 
Underscores

* * *  
<a name="linebreaks"/>
> ## Line Breaks

Blah blah (``sample``) blah.

### :white_check_mark: Syntax
 
My basic recommendation for learning how line breaks work is to experiment and discover -- hit &lt;Enter&gt; once (i.e., insert one newline), then hit it twice (i.e., insert two newlines), see what happens. You'll soon learn to get what you want. "Markdown Toggle" is your friend. 
 
Here are some things to try out:
 
```
Here's a line for us to start with.
 
This line is separated from the one above by two newlines, so it will be a *separate paragraph*.
 
This line is also a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.
```
 
Here's a line for us to start with.
 
This line is separated from the one above by two newlines, so it will be a *separate paragraph*.
 
This line is also begins a separate paragraph, but...  
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.
 
(Technical note: *Markdown Here* uses GFM line breaks, so there's no need to use MD's two-space line breaks.)

* * *  
<a name="embed"/>
> ## HTML Embeds
 
Youtube videos have an embed code (an html iframe) which is accessible from Share, Embed on the video page. They can't be added directly but you can add an image with a link to the video like this:
 
```no-highlight
<a href="http://www.youtube.com/watch?feature=player_embedded&v=YOUTUBE_VIDEO_ID_HERE
" target="_blank"><img src="http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>
```
 
Or, in pure Markdown, but losing the image sizing and border:
 
```no-highlight
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)
```

[![Bazaar at Shinbashi Tokyo, by Rick Cogley](http://img.youtube.com/vi/ibhHk0CCYXA/0.jpg)](http://www.youtube.com/watch?v=ibhHk0CCYXA)
 

Referencing a bug by #bugID in your git commit links it to the slip. For example #1. 

