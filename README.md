# INTRODUCTION

This document is a cheatsheet for Markdown, with emphasis on the "GFM" or "Github Flavored Markdown" as Github calls it, containing syntax and examples intended to help authors writing on Github. Markdown is a text formatting syntax designed to be easy to input by people, yet be converted to HTML by an application code library of the same name. 

Markdown and its variants are ubiquitous at the time of this writing, and are the syntax of choice for many wikis, blogs, forums and website generator applications (Github, Reddit, Stack Exchange, Source Forge etc). Markdown allows you to enter easy-to-remember markup, for instance using asterisks for emphasis (``**text to be emphasized**``) or pound-signs in front of headers (``### An H3 Header``), and it then takes care of the conversion to HTML markup in the background.   

Markdown is originally by John Gruber, and you should read his [original specification](http://daringfireball.net/projects/markdown/), and the [wikipedia article](https://en.wikipedia.org/wiki/Markdown) on the same. 

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
* Wikipedia article on [Markdown](https://en.wikipedia.org/wiki/Markdown).

## Table of Contents

* [Headers](#headers)  
* [Emphasis](#emphasis)  
* [Lists](#lists)  
* [Links](#links)  
* [Images](#images)  
* [Code and Syntax Highlighting](#code)  
* [Tables](#tables)  
* [Other Formatting](#otherformatting)  
* [HTML](#html)  

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
 
Add "emphasis" using underscores (``_my italics_``) or asterisks (``*my italics*``), and "strong emphasis" using double underscores or asterisks (``__my bold face__`` or ``**my bold fact**``). Emphasis gets converted to html ``<em></em>`` tags and strong emphasis to ``<strong></strong>`` tags. This style of markup is semantic (meaning it is meaningful in terms of the structure of the document) and not just cosmetic, and it's where the names of the tags come from. 

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

GFM lists support a "checklist" style, that can be dynamically ticked off like a todo list _in the case of Issues_, without editing the issue. Checklists look like ``- [ ] the item`` or ``- [x] the item``. If you add a checklist in a Github Issue (in the top, initial entry, not the replies), you will see a progress bar in your issues list. Sweet! In the case of ``.md`` files like this one, checklists are static, but you can still edit the file, and add and x between the square brackets. 

GFM checklists also support automatic linking to users and issues, simply by inserting @username or #1 where 1 is the issue number. 

![cogley github issue progress 2014-12-30_17-47-06](https://cloud.githubusercontent.com/assets/512328/5577453/9ecdd4bc-9054-11e4-9f69-dc8cbfc413a0.png)  
![cogley github issue dynamic checklists 2014-12-30_19-21-23](https://cloud.githubusercontent.com/assets/512328/5577659/9be1f1d4-9059-11e4-9d71-0ce456565f96.png)  


### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax
 
Necessary leading and trailing spaces are indicated with dots: ••

```no-highlight
1. **Experimental Method**
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

1. **Empirical Method**
••* etc

#### To-do List In an Issue
- [x] @RickCogley Work on issue #2. 
- [ ] @anothergithubuser Work on issue #3. 
```

### <img title="diamond_shape_with_a_dot_inside" alt="diamond_shape_with_a_dot_inside" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4a0.png" height="25" width="25" align="absmiddle"> Showcase
 
1. **Experimental Method**
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

1. **Empirical Method**
  * etc

#### To-do List in an Issue
- [x] @RickCogley Work on issue #2. 
- [ ] @anothergithubuser Work on issue #3. 

* * *  
<a name="links"/>
> ## Links
 
Markdown allows you to create inline or reference links. Inline links have all the information for the link included inline in the document (``[eSolia Inc.](http://www.esolia.com)``), whereas reference links simply refer to a code elsewhere in the document (``[eSolia Inc.][1]``). The point to reference links is to allow you to keep your document tidy, so that it's easier to read. 

### <img title="octocat" alt="octocat" src="https://assets-cdn.github.com/images/icons/emoji/octocat.png" height="25" width="25" align="absmiddle"> Github Style

GFM supports automatic linking in a number of convenient cases. You can autolink an URL simply by entering the URL, or in Issues, you can autolink SHAs, @usernames, Issue Id numbers (like #1, #2), or various specific combinations of user/repo@sha or user/repo#issuenum.  

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax

Notice that inline links use the syntax ``[]()`` whereas reference links use ``[][]``.
 
```no-highlight
* _Inline link_: visit [eSolia](http://www.esolia.com) for Tokyo IT support...  
* _Inline link with title_: eSolia [PROdb](http://www.esolia.com/prodb "eSolia PROdb cloud database") is a rock-solid cloud database... (hover over the link to see a tooltip with the title text)
* _Inline link with relative path_: See the [license](../../blob/master/LICENSE.md) for this project...
* _Reference link with number_: visit [eSolia][1] for Tokyo IT support... 
* _Reference link with text_: eSolia [PROdb][Cloud Database PROdb]...
* _Reference link to reference text alone_: See eSolia's [Cloud Database PROdb]...

[1]: http://www.esolia.com
[Cloud Database PROdb]: http://www.esolia.com/prodb

#### In Issues: 

* SHA: ad251b871766f269af97d9c2be4228f0beb6c04f
* Short SHA: ad251b (does _not_ work)
* User@SHA: rickcogley@ad251b871766f269af97d9c2be4228f0beb6c04f
* User/Repository@SHA: rickcogley/Github-Markdown-Reference@ad251b871766f269af97d9c2be4228f0beb6c04f
* Issue Number: #3
* Issue "GH" Number: GH-3
* User#Num: rickcogley#3
* User/Repository#Num: rickcogley/Github-Markdown-Reference#3
```
 
### <img title="diamond_shape_with_a_dot_inside" alt="diamond_shape_with_a_dot_inside" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4a0.png" height="25" width="25" align="absmiddle"> Showcase

* _Inline link_: visit [eSolia](http://www.esolia.com) for Tokyo IT support...  
* _Inline link with title_: eSolia [PROdb](http://www.esolia.com/prodb "eSolia PROdb cloud database") is a rock-solid cloud database... (hover over the link to see a tooltip with the title text)
* _Inline link with relative path_: See the [license](../../blob/master/LICENSE.md) for this project...
* _Reference link with number_: visit [eSolia][1] for Tokyo IT support... 
* _Reference link with text_: eSolia [PROdb][Cloud Database PROdb]...
* _Reference link to reference text alone_: See eSolia's [Cloud Database PROdb]...

[1]: http://www.esolia.com
[Cloud Database PROdb]: http://www.esolia.com/prodb

#### In Github Issues: 

The below links won't work in this README.md file, but you can see them working in [this issue](https://github.com/RickCogley/Github-Markdown-Reference/issues/2). 

* SHA: ad251b871766f269af97d9c2be4228f0beb6c04f
* Short SHA: ad251b (does _not_ work)
* User@SHA: rickcogley@ad251b871766f269af97d9c2be4228f0beb6c04f
* User/Repository@SHA: rickcogley/Github-Markdown-Reference@ad251b871766f269af97d9c2be4228f0beb6c04f
* Issue Number: #3
* Issue "GH" Number: GH-3
* User#Num: rickcogley#3
* User/Repository#Num: rickcogley/Github-Markdown-Reference#3

* * *  
<a name="images"/>
> ## Images

For images, Markdown uses similar syntax to links. Just add a ``!`` in front of the link (``![eSolia Chicklet Logo](http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_GoldBlue.svg)``). A reference link style works as well. 

### <img title="octocat" alt="octocat" src="https://assets-cdn.github.com/images/icons/emoji/octocat.png" height="25" width="25" align="absmiddle"> Github Style

GFM uses the same syntax as regular Markdown for images. However, note that if you need images for a README.md file like this one, there are a couple ways you can do prepare them for use: 

1. Upload the image to a Github Issue, and use its URL in the image markdown in the README.md. 
1. Create a Github Pages page (like [the one for this project](http://rickcogley.github.io/Github-Markdown-Reference)), and upload the images to the resulting gh-pages branch of the repository. Gh-pages are served via a fast ngnix instance, via an URL like ``http://myuser.github.io/myrepo/path/to/myimage.png``. 
1. Upload the image to your repository, and reference it from there. This is _not a good idea however_, because the image will be served via the Github application layer. Raster images (.gif, .png, .jpg) work, but vector images (.svg) won't even be displayed when referenced in this manner, instead appearing as the underlying code instead of the image. Compare [this .png image](https://raw.githubusercontent.com/RickCogley/Github-Markdown-Reference/master/Assets/eSOLIA_Square_BlueBrown.png) with [this .svg image](https://raw.githubusercontent.com/RickCogley/Github-Markdown-Reference/master/Assets/eSOLIA_Square_BlueBrown.svg) served directly from the repository. 
1. Serve the images from another service like Imgur or Dropbox.

The above concepts hold true for other assets as well, such as javascript assets. 

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax

Notice that inline images use the syntax ``![]()`` whereas reference images use ``![][]``. If you need to resize images, use HTML. 
 
```no-highlight
_eSolia SVG Logo as an Inline link_:  
![eSolia Chicklet 01 Alt Text](http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_YellowGreen.svg)

_eSolia PNG Logo as an Inline link with hoverable title_:  
![eSolia Chicklet 02 Alt Text](http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_GreenPurple.png "eSolia Chicklet 02")

_eSolia PNG Logo as a Reference link with hoverable title_:  
![eSolia Chicklet 03 Alt Text][eSolia-Chicklet-03]

[eSolia-Chicklet-03]: http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_BlueBrown.png "eSolia Chicklet 03"

_eSolia SVG Logo as sized HTML img tag_:  
<img title="eSolia Chicklet 04" alt="eSolia Chicklet 04 Alt Text" src="http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_YellowBlue.svg" height="40" width="40" align="absmiddle"><img title="eSolia Chicklet 04" alt="eSolia Chicklet 04 Alt Text" src="http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_YellowBlue.svg" height="100" width="100" align="absmiddle"><img title="eSolia Chicklet 04" alt="eSolia Chicklet 04 Alt Text" src="http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_YellowBlue.svg" height="200" width="200" align="absmiddle"><img title="eSolia Chicklet 04" alt="eSolia Chicklet 04 Alt Text" src="http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_YellowBlue.svg" height="400" width="400" align="absmiddle">
```
 
### <img title="diamond_shape_with_a_dot_inside" alt="diamond_shape_with_a_dot_inside" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4a0.png" height="25" width="25" align="absmiddle"> Showcase

We'll serve these via our Github Pages [project site](http://rickcogley.github.io/Github-Markdown-Reference).

_eSolia SVG Logo as an Inline link_:  
![eSolia Chicklet 01 Alt Text](http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_YellowGreen.svg)

_eSolia PNG Logo as an Inline link with hoverable title_:  
![eSolia Chicklet 02 Alt Text](http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_GreenPurple.png "eSolia Chicklet 02")

_eSolia PNG Logo as a Reference link with hoverable title_:  
![eSolia Chicklet 03 Alt Text][eSolia-Chicklet-03]

[eSolia-Chicklet-03]: http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_GoldBlue.png "eSolia Chicklet 03"

_eSolia SVG Logo as sized HTML img tag_:  
<img title="eSolia Chicklet 04" alt="eSolia Chicklet 04 Alt Text" src="http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_YellowBlue.svg" height="40" width="40" align="absmiddle"><img title="eSolia Chicklet 04" alt="eSolia Chicklet 04 Alt Text" src="http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_YellowBlue.svg" height="100" width="100" align="absmiddle"><img title="eSolia Chicklet 04" alt="eSolia Chicklet 04 Alt Text" src="http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_YellowBlue.svg" height="200" width="200" align="absmiddle"><img title="eSolia Chicklet 04" alt="eSolia Chicklet 04 Alt Text" src="http://rickcogley.github.io/Github-Markdown-Reference/images/eSOLIA_Square_YellowBlue.svg" height="400" width="400" align="absmiddle">

* * *  
<a name="code"/>
> ## Code and Syntax Highlighting
 
When writing about programming or source code, Markdown lets you create code blocks by indenting the lines of the block by 4 spaces or 1 tab. Indented blocks are wrapped by Markdown in both ``<pre>`` and ``<code>`` tags. Within a code block, Markdown will convert ampersands ``&`` and angle brackets ``<>`` into HTML entities, making it easy to simply paste HTML source code into a Markdown document. 

### <img title="octocat" alt="octocat" src="https://assets-cdn.github.com/images/icons/emoji/octocat.png" height="25" width="25" align="absmiddle"> Github Style

Github not only supports "fenced" code blocks, which are easier to use compared to indents, but also syntax highlighting via [Linguist](https://github.com/github/linguist). To use fenced code blocks, insert three backticks before and after the block. To specify a language to highlight, specify the language name after the initial backticks, referring to Linguist's [Languages YAML](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml) file (<code> ```javascript </code>).

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax

For quick code references inline, surround the snippet with two backticks on either side. Otherwise, enclose your code in fenced blocks per the below, specifying either the language to be highlighted, or, "no-highlight" to turn off syntax highlighting (<code>```no-highlight</code>). 
 
<pre lang="no-highlight">
<code>
Display hidden files in the Linux shell using this command: ``ls -la``. 

A shell script to return reference times in various timezones:  
```shell
echo == Reference Times ==
echo -e "Tokyo - \t" `TZ=Asia/Tokyo date "+%Z (%z) %R %a %e %b %Y";`
echo -e "Hong Kong - \t" `TZ=Hongkong date "+%Z (%z) %R %a %e %b %Y";`
echo -e "Calcutta - \t" `TZ=Asia/Calcutta date "+%Z (%z) %R %a %e %b %Y";`
echo -e "Berlin - \t" `TZ=Europe/Berlin date "+%Z (%z) %R %a %e %b %Y";`
echo -e "London - \t" `TZ=GMT date "+%Z (%z) %R %a %e %b %Y";`
echo -e "New York - \t" `TZ=US/Eastern date "+%Z (%z) %R %a %e %b %Y";`
echo -e "Chicago - \t" `TZ=US/Central date "+%Z (%z) %R %a %e %b %Y";`
echo -e "Denver - \t" `TZ=US/Mountain date "+%Z (%z) %R %a %e %b %Y";`
echo -e "San Francisco - \t" `TZ=US/Pacific date "+%Z (%z) %R %a %e %b %Y"`
```
 
A square root function in javascript by John Carmack:  
```javascript
/*
================
SquareRootFloat by John Carmack
================
*/
float SquareRootFloat(float number) {
    long i;
    float x, y;
    const float f = 1.5F;

    x = number * 0.5F;
    y  = number;
    i  = * ( long * ) &y;
    i  = 0x5f3759df - ( i >> 1 );
    y  = * ( float * ) &i;
    y  = y * ( f - ( x * y * y ) );
    y  = y * ( f - ( x * y * y ) );
    return number * y;
}
```
 
Some basic Markdown markup:  
```markdown
Use asterisks for emphasis (``**text to be emphasized**``) or pound-signs in front of headers (``### An H3 Header``) in Markdown.   
```
 
An unhighlighted tag:  
```no-highlight
Here's a tag: < xml >.
```
</code>
</pre>

### <img title="diamond_shape_with_a_dot_inside" alt="diamond_shape_with_a_dot_inside" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4a0.png" height="25" width="25" align="absmiddle"> Showcase

Display hidden files in the Linux bash shell using this command: ``ls -la``. 

A shell script to return reference times in various timezones:  
```shell
echo == Reference Times ==
echo -e "Tokyo - \t" `TZ=Asia/Tokyo date "+%Z (%z) %R %a %e %b %Y";`
echo -e "Hong Kong - \t" `TZ=Hongkong date "+%Z (%z) %R %a %e %b %Y";`
echo -e "Calcutta - \t" `TZ=Asia/Calcutta date "+%Z (%z) %R %a %e %b %Y";`
echo -e "Berlin - \t" `TZ=Europe/Berlin date "+%Z (%z) %R %a %e %b %Y";`
echo -e "London - \t" `TZ=GMT date "+%Z (%z) %R %a %e %b %Y";`
echo -e "New York - \t" `TZ=US/Eastern date "+%Z (%z) %R %a %e %b %Y";`
echo -e "Chicago - \t" `TZ=US/Central date "+%Z (%z) %R %a %e %b %Y";`
echo -e "Denver - \t" `TZ=US/Mountain date "+%Z (%z) %R %a %e %b %Y";`
echo -e "San Francisco - \t" `TZ=US/Pacific date "+%Z (%z) %R %a %e %b %Y"`
```

A square root function in javascript:  
```javascript
/*
================
SquareRootFloat by John Carmack
================
*/
float SquareRootFloat(float number) {
    long i;
    float x, y;
    const float f = 1.5F;

    x = number * 0.5F;
    y  = number;
    i  = * ( long * ) &y;
    i  = 0x5f3759df - ( i >> 1 );
    y  = * ( float * ) &i;
    y  = y * ( f - ( x * y * y ) );
    y  = y * ( f - ( x * y * y ) );
    return number * y;
}
```
 
Some Markdown code:  
```markdown
Use asterisks for emphasis (``**text to be emphasized**``) or pound-signs in front of headers (``### An H3 Header``) in Markdown.   
```

An unhighlighted tag:    
```no-highlight
Here's a tag: <xml>.
```

* * *  
<a name="tables"/>
> ## Tables
 
Markdown does not include a way to format tables, and to address this, several enhanced versions of Markdown are available such as [PHP Markdown Extra](https://michelf.ca/projects/php-markdown/extra/). 

### <img title="octocat" alt="octocat" src="https://assets-cdn.github.com/images/icons/emoji/octocat.png" height="25" width="25" align="absmiddle"> Github Style

To add tables to your Github document or issue, use pipe characters to indicate columns in a given row (``| this col | that col |``), and colons in the second row to align text within a column. You can also use Markdown formatting within the table.  

Try the [Markdown Tables Generator](http://www.tablesgenerator.com/markdown_tables) to get some assistance in building your tables. 

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> <img title="octocat" alt="octocat" src="https://assets-cdn.github.com/images/icons/emoji/octocat.png" height="25" width="25" align="absmiddle"> Syntax

When creating GFM tables keep in mind: 

* outer pipes are not required but you can add them if you like that better
* row-by-row pretty alignment is not needed, but do it if you prefer that
* they include no fancy Excel-like features such as sums or averages - it's strictly DIY
 
```no-highlight
Cost per ticket over three year period: 

| Year | Num Tickets Handled | Helpdesk Cost Per Annum in JPY | Cost Per Ticket in JPY |
|-----:|--------------------:|-------------------------------:|-----------------------:|
| 2012 |                5675 |                     12,000,000 |                   2115 |
| 2013 |                6576 |                     12,200,000 |                   1885 |
| 2014 |                9779 |                     15,150,000 |                   1549 |

Popular Compact Camera Comparison:
 
   **Camera** |  **Sensor**  |  **Cost** 
-------------:|:------------:|----------:
 **Fujifilm** |    _APSC_    | USD 1,300 
     **Sony** | _Full Frame_ | USD 2,000 
    **Leica** | _Full Frame_ | USD 8,000 
```
  
### <img title="diamond_shape_with_a_dot_inside" alt="diamond_shape_with_a_dot_inside" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4a0.png" height="25" width="25" align="absmiddle"> Showcase

Cost per ticket over three year period: 

| Year | Num Tickets Handled | Helpdesk Cost Per Annum in JPY | Cost Per Ticket in JPY |
|-----:|--------------------:|-------------------------------:|-----------------------:|
| 2012 |                5675 |                     12,000,000 |                   2115 |
| 2013 |                6576 |                     12,200,000 |                   1885 |
| 2014 |                9779 |                     15,150,000 |                   1549 |

Popular Compact Camera Comparison:
 
   **Camera** |  **Sensor**  |  **Cost** 
-------------:|:------------:|----------:
 **Fujifilm** |    _APSC_    | USD 1,300 
     **Sony** | _Full Frame_ | USD 2,000 
    **Leica** | _Full Frame_ | USD 8,000 

* * *  
<a name="otherformatting"/>
> ## Other Formatting
 
Markdown supports other formatting as well, namely horizontal rules and block quotes. For a horizontal rule enter three or more hyphens, asterisks or underscores. For a blockquote, enter a ``>`` before the line, and you can include Markdown inside a blockquote, as well. There is no special GFM syntax for these. 

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax

```no-highlight
You could format a famous quotation in blockquote style, including inline Markdown, as follows: 

> #### _If passion drives you, let reason hold the reins._ — Benjamin Franklin, 1706 - 1790

Three or more hyphens, asterisks or underscores will be converted to a horizontal rule: 
***
----
____
```

### <img title="diamond_shape_with_a_dot_inside" alt="diamond_shape_with_a_dot_inside" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4a0.png" height="25" width="25" align="absmiddle"> Showcase
 
You could format a famous quotation in blockquote style, including inline Markdown, as follows: 

> #### _If passion drives you, let reason hold the reins._ — Benjamin Franklin, 1706 - 1790

Three or more hyphens, asterisks or underscores will be converted to a horizontal rule: 
***
----
____
  
<a name="html"/>
> ## HTML Code

Markdown also allows you to enter raw HTML code, such as entering definition lists or image tags as we have explored above. 

### <img title="octocat" alt="octocat" src="https://assets-cdn.github.com/images/icons/emoji/octocat.png" height="25" width="25" align="absmiddle"> Github Style

Github specifies a [whitelist of permitted HTML tags](https://github.com/github/markup/tree/master#html-sanitization) to take note of. Unfortunately you cannot use iframe tags, which would be convenient for inserting embed codes from sites like Youtube (accessible from the video page, Share, Embed). You can even enter "[entities](http://www.entitycode.com)" directly, such as &#182;. 

### <img title="white_check_mark" alt="white_check_mark" src="https://assets-cdn.github.com/images/icons/emoji/unicode/2705.png" height="25" width="25" align="absmiddle"> Syntax
 
```no-highlight
Sometimes entering an "entity" can be convenient: 
&copy;&sect;&ne;&hearts;&spades;&clubs;&diams;&#182;

Here's a definition list: 
<dl>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>
  <dt>XML</dt>
  <dd>Extensible Markup Language</dd>
</dl>

And an img tag inside an anchor tag, to display a clickable Youtube video:
<a href="http://www.youtube.com/watch?feature=player_embedded&v=YOUTUBE_VIDEO_ID_HERE
" target="_blank"><img src="http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>
```
 
### <img title="diamond_shape_with_a_dot_inside" alt="diamond_shape_with_a_dot_inside" src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f4a0.png" height="25" width="25" align="absmiddle"> Showcase

Sometimes entering an "entity" can be convenient:  
&copy;&sect;&ne;&hearts;&spades;&clubs;&diams;&#182;

Here's a definition list:  
<dl>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>
  <dt>XML</dt>
  <dd>Extensible Markup Language</dd>
</dl>

And a clickable Youtube video in nested Markdown:  
[![Bazaar at Shinbashi Tokyo, by Rick Cogley](http://img.youtube.com/vi/ibhHk0CCYXA/0.jpg)](http://www.youtube.com/watch?v=ibhHk0CCYXA)

Or, the same in HTML with the size set (not possible in pure Markdown):  
<a href="http://www.youtube.com/watch?feature=player_embedded&v=ibhHk0CCYXA
" target="_blank"><img src="http://img.youtube.com/vi/ibhHk0CCYXA/0.jpg" 
alt="Bazaar at Shimbashi Tokyo, by Rick Cogley" width="240" height="180" border="10" /></a>

* * *  

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Github Markdown Cheatsheet</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://rick.cogley.info" property="cc:attributionName" rel="cc:attributionURL">James R. Cogley</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/RickCogley/Github-Markdown-Reference" rel="dct:source">https://github.com/RickCogley/Github-Markdown-Reference</a>.
