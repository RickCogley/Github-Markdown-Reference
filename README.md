# INTRODUCTION

This is a cheatsheet for Markdown, including GFM or "Github Flavored Markdown" as Github calls it, containing syntax and examples. 

Markdown is originally by John Gruber, and you should read his [original specification](http://daringfireball.net/projects/markdown/). Markdown is ubiquitous at the time of this writing, and is the syntax of choice for many wikis, blogs, forums and website generator applications. Markdown allows you to enter markup in an easy-to-remember manner, for instance using asterisks for emphasis (``**text to be emphasized**``) or pound-signs in front of headers (``### An H3 Header``), and it then takes care of the conversion to HTML markup in in the background.   

**Request**

Please _don't edit this page_. Rather, if you have a suggestion, fork this repository and make a pull request. 

**References**

* [Markdown specification](http://daringfireball.net/projects/markdown/) by John Gruber.
* Github Help Documentation on "GFM": 
  * [Github Flavored Markdown](https://help.github.com/articles/github-flavored-markdown)
  * [Writing on Github](https://help.github.com/articles/writing-on-github)
  * [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
* Repositories regarding Markdown syntax from [dvidsilva](https://github.com/dvidsilva/MarkdownReference) and [adam-p](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).
* Adam Pritchard's [Markdown Here](http://www.markdown-here.com/livedemo.html) or the  [Markdown-it](https://markdown-it.github.io) demo sites, where you can experiment in a kind of "sandbox" environment. 
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

### <img title="octocat" alt="octocat" src="https://assets-cdn.github.com/images/icons/emoji/octocat.png" height="25" width="25" align="absmiddle"> Github Style

GFM treats line breaks in a different way from normal Markdown, treating a single press of the enter key as a line break (``<br>``), which is likely what most people intend. The regular Markdown treatment is to require two spaces after a line to add a break, which is rather counterintuitive if you do not know the trick. 

In other words, in GFM just enter naturally:

```no-highlight
Say NO to Drugs¶  
From your local police dep't.¶
```

... as opposed to having to enter two spaces (represented by •): 

```no-highlight
Say NO to Drugs••¶  
From your local police dep't.••¶
```

**N.b.** - _as of 30 Dec 2014 it appears you **do** need to add the two spaces to force a_ ``<br>``.

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax

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
 
### <img title="diamond_shape_with_a_dot_inside" alt="diamond_shape_with_a_dot_inside" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4a0.png" height="25" width="25" align="absmiddle"> Showcase

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

### <img title="octocat" alt="octocat" src="https://assets-cdn.github.com/images/icons/emoji/octocat.png" height="25" width="25" align="absmiddle"> Github Style

GFM adds strikethrough to Markdown using double tildes (``~~text to strike~~``) surrounding the text, which equates to html del tags (``<del>text to strike</del>``). GFM also gracefully handles the situation when words contain underscores, as in software development (``some_code_variable``). Furthermore, GFM allows you to emphasize part of a word using asterisks. 

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax

```no-highlight
Semantic emphasis, via *asterisks* or _underscores_. Renders as italics.

Semantic strong emphasis, via double **asterisks** or __underscores__. Renders as bold.

Combine emphasis via **asterisks and _underscores_**.

Strike mistaken text using two tildes. ~~Scratch this.~~

Emphasize parts of words using asterisks. You say to*MAH*toe, I say to*MAY*toe. 
```
 
### <img title="diamond_shape_with_a_dot_inside" alt="diamond_shape_with_a_dot_inside" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4a0.png" height="25" width="25" align="absmiddle"> Showcase

Semantic emphasis, via *asterisks* or _underscores_. Renders as italics.

Semantic strong emphasis, via double **asterisks** or __underscores__. Renders as bold.

Combine emphasis via **asterisks and _underscores_**.

Strike mistaken text using two tildes. ~~Scratch this.~~

Emphasize parts of words using asterisks. You say to*mah*toe, I say to*may*toe.
 
* * *  
<a name="lists"/>
> ## Lists
 
In Markdown, ordered lists (numbered, ``<ol>`` tag) are created using numbers followed by a period and space, then the list item. Unordered lists (bulleted, ``<ul>`` tag) are created using asterisks, pluses or hyphens, followed by a space, then the list item. You can indent any list item following the first item, to create a nested list, and you can combine list types. 

### <img title="octocat" alt="octocat" src="https://assets-cdn.github.com/images/icons/emoji/octocat.png" height="25" width="25" align="absmiddle"> Github Style

GFM lists support a "checklist" style, that can be dynamically ticked off like a todo list, without editing the Markdown document. Checklists look like ``- [ ] the item`` or ``- [x] the item``. If you add a checklist in a Github Issue (in the top, initial entry, not the replies), you will see a progress bar in your issues list. Sweet!

GFM checklists also support automatic linking to users and issues, simply by inserting @username or #1 where 1 is the issue number. 

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax
 
(In this example, leading and trailing spaces are shown with with dots: •)

```no-highlight
1. Experimental Method
••1. Ask questions about a natural phenomenon
••1. Make observations about the phenomenon
••1. Form a hypothesis, or proposed explanation.
••1. Predict logical consequences of the hypothesis. 
••1. Methodically test the hypothesis to verify or falsify, via three types of experiment:
••••* Controlled 
••••* Natural
••••* Field
••1. Gather and analyze experimental data, including uncertainty.
••1. Draw conclusions, comparing data with predictions. 

•••To intersperse text within your list, indent at least one leading space, and enough to align to your liking. This text block is a paragraph, and has blank lines above and below. 

•••You can also insert text on separate lines using line breaks. Use two trailing spaces to achieve this.••
•••Then indent again, and follow with two trailing spaces again, as in this line.••

1. Empirical Method
••* etc

#### To-do List
- [x] @somegithubuser Work on issue #1. 
- [ ] @anothergithubuser Work on issue #2. 
```
 
1. Experimental Method
  1. Ask questions about a natural phenomenon
  1. Make observations about the phenomenon
  1. Form a hypothesis, or proposed explanation.
  1. Predict logical consequences of the hypothesis. 
  1. Methodically test the hypothesis to verify or falsify, via three types of experiment:
    * Controlled 
    * Natural
    * Field
  1. Gather and analyze experimental data, including uncertainty.
  1. Draw conclusions, comparing data with predictions. 

   To intersperse text within your list, indent at least one leading space, and enough to align to your liking. This text block is a paragraph, and has blank lines above and below.

   You can also insert text on separate lines using line breaks. Use two trailing spaces to achieve this.  
   Then indent again, and follow with two trailing spaces again, as in this line.  

1. Empirical Method
  * etc

#### To-do List
- [x] @somegithubuser Work on issue #1. 
- [ ] @anothergithubuser Work on issue #2. 

* * *  
<a name="links"/>
> ## Links
 
Blah blah (``sample``) blah. There are two ways to create links.

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax
 
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

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax
 
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

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax
 
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

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> <img title="octocat" alt="octocat" src="https://assets-cdn.github.com/images/icons/emoji/octocat.png" height="25" width="25" align="absmiddle"> Syntax
 
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

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax
 
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

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax
 
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

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax
 
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

Other - you can just stick an entity in. Like &#182;

<img title="octocat" alt="octocat" src="https://assets-cdn.github.com/images/icons/emoji/octocat.png" height="25" width="25" align="absmiddle">

<img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle">

<img title="diamond_shape_with_a_dot_inside" alt="diamond_shape_with_a_dot_inside" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4a0.png" height="25" width="25" align="absmiddle">
