# Lio Min

### general yaml tips
in .yml files, try to use consistent indentation and wrap values in quotation marks (i.e. `title: "cool title"`). 

**Edge Cases:**

Sometimes you may have quotations as part of the text itself. For example, hypothetically if a link's text was to be _She said "maybe"_ wrapping this value in quotes like below would cause an error:

```
link: "https://somewhere.com"
text: "She said "maybe""
```

So instead you could use single quotes like so...

```
link: "https://somewhere.com"
text: 'She said "maybe"'
```
this will help distinguish the quotes that are part of the text to show and the formatting of the yaml code.

**Also I was wrong about multiple lines!** As long as they are inside quotes it should be fine. I.e. this is ok:

```
text: '<a href="https://hello.com">hello world</a>
<a href="https://doom.com">are we doomed?</a>
<a href="https://somethingelse.com">somewhere else</a>'
```
Notice I also am using single quotes in that example because the `href` uses double quotes already and we want to be able to distinguish between which quotes are wrapping the entire text value vs which ones are part of the text value itself.

### general markdown tips

_You'll only be using markdown when you are creating one-off pages like `/beatingheartbeats`_

When you create a new .md file, you should make sure that you are creating it in the root folder and not inside a subfolder like _data or _layouts. 

For writing in markdown, I like this [guide]("https://www.markdownguide.org/cheat-sheet/]").
You can also just write plain old html in your markdown file and that will work too. 

Jekyll uses what's called "frontmatter" at the top of every markdown file to store metadata like the page title, url, etc (that's a term from publishing no?). So the top of your markdown file should look like this:
```
---
layout: default
title: ADD TITLE OF YOUR PAGE HERE
permalink: /add_link_you_want_here/
---
```

and then after that you can start writing your markdown. Take a look at `/beatingheartbeats.md` as an example. 



----------------------------------------------------------------------
## Updating work

1. go to _data/work.yml
2. type your yaml to add a work. Follow this pattern:

```
- title: "Title of your project"
  category: "Category name (be wary of capitals, try to be consistent (i.e. Books vs books))"
  body: (you can add as many description/link pairs as you need per project)
  - description:  "text to show" 
    link: "https://link_to_go_to.com"
  - description:  "text to show" 
    link: "https://link_to_go_to.com"
  - description:  "text to show" 
    link: "https://link_to_go_to.com"

```
indentation matters with yaml. For example, in the above code, the fact that `- description` is indented further than `body` indicates that `- description` is nested within `body`. (Members of a list in yaml start with the `-` symbol).

## Updating Upcoming

1. go to _data/upcoming.yml
2. Add/remove/edit the text/link pairs following the pattern...
```
- text: "→ Comic Practice (archive)"
  link: "https://comicpractice.tumblr.com/"

- text: "→ Comic Practice (archive)"
  link: "https://comicpractice.tumblr.com/"
  
- text: "→ Unnatural World (The Nib)"
  link: "https://thenib.com/exhibiting-extinction/"
...
```

## Updating Collaborations

1. go to _data/collaborations.yml
2. Fairly straightforward. Edit between the quotation marks i.e.
```
text: "edit this"
```

## Updating radio lio

1. go to _data/radio_lio.yml
2. Fairly straightforward. Edit between the quotation marks i.e. But be mindful of which quotation marks are being used inside the text vs wrapping around it.

```
text: '#RADIOLIO <br> <iframe scrolling="no" style="width:100%!important;border:1px #ccc solid !important;" src="https://buttondown.email/RADIOLIO?as_embed=true"></iframe>'
```

## Updating colophon

1. go to _data/colophon.yml
2. Fairly straightforward. Edit between the quotation marks i.e. But be mindful of which quotation marks are being used inside the text vs wrapping around it.

```
text: "⬆️<br>Sign up for the RADIOLIO newsletter.<br><br>LIOMIN.com is the work of Aarati Akkapeddi.<br><br>Thanks for reading :^) Safe travels & good hunting on the digital tides..."
```

## Updating contact info

1. go to _data/contact.yml
2. Fairly straightforward. Edit between the quotation marks i.e. But be mindful of which quotation marks are being used inside the text vs wrapping around it.

```
text: '<a target="_blank" href="mailto:liomin@protonmail.com">Email</a> / 
<a target="_blank" href="http://instagram.com/emo__ocean">Instagram</a> / <a target="_blank" href="https://emo--ocean.tumblr.com/">Tumblr</a>'
```

## Adding a playlist page

1. create a new .md file in the root folder. See beatingheartbeats.md as an example.
2. in this file add this frontmatter to the top:
```
---
layout: default
title: ADD TITLE OF YOUR PAGE HERE
permalink: /add_link_you_want_here/
---
```
3. After this frontmatter you can start writing your own [markdown]("https://www.markdownguide.org/cheat-sheet/") for the content of the page.


