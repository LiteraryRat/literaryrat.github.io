---
title: Documentation
author: Literary Rat
featuredImage: screenshot-home.png
---

{{< toc >}}

---

## Foreword

This section is meant to provide resources for interesting articles, websites, physical libraries, museums, etc. My vision of it was a sort of cultural library. I'm going to divide it up into sections. Might change in the future (this is obviously very much a work in progress). 

Happy exploring!

The Literary Rat\
January 2024

---

## Books

1. Local libraries: go to your local library!—if you have one. If you don't have a big library near you (that sucks) try seeing if there are any "mini-libraries" where people leave books for the public. I've found a couple in my neighborhood and in other cities and I know there are many initiatives to provide the public with free books in many cities.
2. Online libraries and archives. These are the ones I use, and they have some really good books! Unfortunately some got taken down due to copyright :( but there's still some great stuff in here!
    https://openlibrary.org/
    https://www.gutenberg.org/

3. Your local bookstore: now of course here in the US we have Barnes & Noble which is great and all (I'm happy they're finding success now after some dark years) but I think there's great value in supporting local bookstores. Not only do they have more soul I think they also allow you to support readership in a more meaningful way by helping a small business and the reading community in your town. In fact, I'm going to make it a goal this year to visit more local bookstores. 
4. Old book giveaways: Half Price Books is big in the US (not free but cheap) but also schools and libraries sometimes give out books for free they are trying to get rid of. I've gotten some real gems over the years. Also yard sales can be a bonanza (I'm guessing, idk I've never tried getting books that way).

---

## Literary magazines



---

## Hugo

Ed is a Hugo theme. That means you will need some familiarity with Hugo to take advantage of its full potential. While running a Hugo site is a bit more involved than Wordpress and other similar tools, the payoff in the long term is worth the effort to learn it. If you are new to Hugo, I recommend you take a look at {{< link src="https://strapi.io/blog/guide-to-using-hugo-site-generator" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}A Guide to Using Hugo{{< /link >}} at *Strapi*, {{< link src="https://gohugo.io/hosting-and-deployment/hosting-on-github/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}Host on GitHub{{< /link >}} on *Hugo Documentation Site* and {{< link src="https://gohugo.io/documentation/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}Hugo's own documentation{{< /link >}} to start getting a sense of how it works.

Once you have gone through these tutorials, you can get started using Ed. Remember to always and only edit content files for your site using {{< link src="https://en.wikipedia.org/wiki/Text_editor" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}a plain text editor{{< /link >}}, and *not* a word processor. I'm composing this file using a plain text editor called {{< link src="https://code.visualstudio.com/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}Visual Studio Code{{< /link >}}.

You should make sure that all your texts have the YAML {{< link src="https://gohugo.io/content-management/front-matter/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}Front Matter{{< /link >}} (the information at the top of the file). YAML stands for "YAML Ain't Markup Language" --- no disrespect to XML --- and it's the main way that Hugo handles named data. Here's an example of YAML Front Matter:

~~~ yaml
---
# Common-Defined params
title: "Cahier d'un retour au pays natal"
draft: true # Is this text a draft?
tags:
  - Tag
  - "Another tag"
date: 2022-02-01T14:56:58+02:00
lastmod: 2022-05-01T14:56:58+02:00

# Theme-Defined params
author: Aimé Césaire # Author of the text
editor: Alex Gil # Editor of the text
source: Project Guttenberg # The source of the text
rights: Public Domain # Rights for this text
pageTitle: Hello! # The title for the content w/o setting <title> tag
toc: true # Enable Table of Contents for specific page
private: true # Hide text from search engines
semanticType: about # Semantic type of the work (used for Schema.org)
featuredImage: screenshot-home.png # Featured image of the text
annotations: false # Disable annotation via hypothesis on this page
---
~~~

For more information about all available standard front matter variables, please read {{< link src="https://gohugo.io/content-management/front-matter/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}Hugo Front Matter{{< /link >}}.

---

## Markdown and CommonMark

Ed is designed for scholars and amateur editors who want to produce either a clean reading edition or a scholarly annotated edition of a text. The main language we use to write in the Hugo environment is called Markdown. To learn more about the Markdown family, see Dennis Tenen and Grant Wythoff's "{{< link src="http://programminghistorian.org/en/lessons/sustainable-authorship-in-plain-text-using-pandoc-and-markdown" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}Sustainable Authorship in Plain Text using Pandoc and Markdown{{< /link >}}".

By default Hugo uses a special Markdown processor called Goldmark. The processor can be said to use it's own 'flavor' of Markdown called CommonMark, and sometimes the Markdown syntax will be different than other flavors of Markdown. CommonMark is a rationalized version of Markdown syntax with a spec whose goal is to remove the ambiguities and inconsistency surrounding the original Markdown specification. It offers a standardized specification that defines the common syntax of the language along with a suite of comprehensive tests to validate Markdown implementations against this specification. You can become familiar with the CommonMark syntax in the {{< link src="https://spec.commonmark.org/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}CommonMark documentation{{< /link >}}. Another way to become familiar is to examine the sample text source files we provided.

---

## Genres

Ed offers four different layouts: poem, narrative, drama and simple post. To create content of a certain genre, create a file in the appropriate folder. For example, if you want to create a poem, create a file in the `content/poems` folder. Another way is to indicated genre in the YAML front matter on your texts. The templates that govern how these genres are displayed can be found in the Ed's `layouts` folder. Redefining these layouts in project wide level will allow you to tweak the stylesheets according to your different needs. Out of the box, Ed contains some special instructions for poetry in its stylesheets that allow you to deal with some of the peculiarities of poetry layouts.

To indicate lines in poetry we use the line syntax from Markdown:

~~~ markdown
- Hold fast to dreams
- For if dreams die
- Life is a broken-winged bird
- That cannot fly.
- Hold fast to dreams
- For when dreams go
- Life is a barren field
- Frozen with snow.
~~~

The `-` at the beginning of each line indicates that these are lines. Another way to achieve the same effect is to use the following syntax:

~~~ markdown
Hold fast to dreams\
For if dreams die\
Life is a broken-winged bird\
That cannot fly.\
Hold fast to dreams\
For when dreams go\
Life is a barren field\
Frozen with snow.
~~~

To indent specific lines we take advantage of Hugo shortcuts that allows us to create empty indentation for a line. This approach still allows the line to be readable while editing.

~~~ markdown
- {{</* indent 3 */>}} But O heart! heart! heart!
- {{</* indent 4 */>}} O the bleeding drops of red,
- {{</* indent 5 */>}} Where on the deck my Captain lies,
- {{</* indent 6 */>}} Fallen cold and dead.
~~~

or:

~~~ markdown
{{</* indent 3 */>}} But O heart! heart! heart!\
{{</* indent 4 */>}} O the bleeding drops of red,\
{{</* indent 5 */>}} Where on the deck my Captain lies,\
{{</* indent 6 */>}} Fallen cold and dead.
~~~

The `{{</* indent 3 */>}}` is what we need to in order to indicate the indent value for that line. Values can range from 1-10. You can expand the range or adjust the values in the custom stylesheet file. Ed is customized by creating stylesheet files in `assets/css/extended/*.css` at project wide level.

The example from Raisin in the Sun shows us that we don't need much special markup for theater as long as we use CAPITAL LETTERS for speakers. Italics for directions are easy enough. Just use `*` around the words you want to italicize.

*Narrative of the Life of Frederick Douglass* shows us an example of narrative that includes footnotes and quoted poetry. See the sections below for how to accomplish these different effects.

---

## Footnotes

Footnotes are the bread and butter of scholarship. Hugo makes footnotes a fairly simple affair:

~~~ markdown
- O Captain! my Captain! rise up and hear the bells;
- Rise up—for you the flag is flung—for you the bugle[^1] trills,

...

[^1]: The bugle is a small trumpet implicated in the military industrial complex.
~~~

These footnotes can be placed anywhere, but they will always be generated at the bottom of the document. To have a multi-paragraph footnote you need to start the footnote text on the next line after the footnote anchor and indent it:

~~~ markdown
[^1]: Ugh pinterest fixie cronut pitchfork beard. Literally deep
      cold-pressed distillery pabst austin.

      Typewriter 90's roof party poutine, kickstarter raw
      denim pabst readymade biodiesel umami chicharrones XOXO.
~~~

Please note, you need to indent all lines at the same level to make them stay inside the footnote.

At the moment (May 2022) time the footnotes system provided by Hugo does have one limitation: It does not support non-numbered footnotes, and it only allows you to have one set of footnotes for a text. In some cases we have to separate the author's footnotes from our own, in others we want to represent the author's own footnote style. In these cases we have to use custom Ed's shortcode for footnotes. Here's the example from *Narrative of the Life*:

~~~ markdown
... At this time, Anna,{{</* footnote "fn2" */>}} my intended wife, came on;

...

{{</* footnotesList */>}}
...
{{</* citation "fn2" "She was free." */>}}
...
{{</* /footnotesList */>}}
~~~

---

## Blockquote

*Narrative of the Life* also includes several blockquote elements. You can also find another example of blockquote use in the footnote of "O Captain! My Captain!" Simple blockquote are simple enough in Markdown:

~~~
> This is to certify that I, the undersigned, have given the bearer, my servant, full liberty to go to Baltimore, and spend the Easter holidays.
>
> Written with mine own hand, &c., 1835.
> WILLIAM HAMILTON,
~~~

To use a line break in block elements add two spaces after the end of the line where you want the break. You can't see them after `&c., 1835.` but they are there.

Things get a bit complicated when we want to use poetry inside the block or when the block is included in another block element, like a footnote. Here's the last two stanzas from "A Parody" in *Narrative of the Life*, which shows an example of a blockquote of poetry:

~~~
...
> - Two others oped their iron jaws,
> - And waved their children-stealing paws;
> - There sat their children in gewgaws;
> - By stinting negroes' backs and maws,
> - They kept up heavenly union.
{.poetry}
> - All good from Jack another takes,
> - And entertains their flirts and rakes,
> - Who dress as sleek as glossy snakes,
> - And cram their mouths with sweetened cakes;
> - And this goes down for union.
{.poetry}
~~~

The `{.poetry}` tag at the end tells the processor to think of the lines above it as poetry. The `{.poetry}` tag is an example of Goldmark class assignments for block-elements. Because this segment of poetry exists in the 'narrative' layout, and because it is part of a blockquote, we need to signal to the processor to process poetry this way, so that the right class is invoked in the stylesheet. The good news is this is the most complex Goldmark syntax layout you will encounter in Ed.


## Pages

Your editions are treated as {{< link src="https://gohugo.io/content-management/sections/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}sections{{< /link >}} or {{< link src="https://gohugo.io/content-management/page-bundles/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}page bundles{{< /link >}} in Ed. Other web pages in your site exist outside the `content` folder. Default homepage, for example, is constructed from the `index.html` file found on the `layouts` folder of Ed theme.

You will notice that the homepage in particular has a `.html` file ending instead of a `.md` ending. All template files in Hugo are HTML, and the index behaves as a template file. Although these files are mostly written in HTML, notice that they may contain {{< link src="https://gohugo.io/templates/introduction/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}template tags{{< /link >}}. To create your own homepage create `index.html` file in project `layouts` folder, making sure that your changes to `index.html` are written in valid HTML. The same goes for all Ed's template files in the `layouts` folder.

---

## Tables of Content

You will find three kinds of Tables of Content in Ed. The first example is in the list of Latest Publications in the Homepage. This list is generated using the {{< link src="https://gohugo.io/templates/introduction/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}templating language{{< /link >}}. This is one of the major components of Hugo, and I recommend you deepen your knowledge of it if you want to modify the logic that automates much of Ed. Here is the code that generates the Latest Publications list on the homepage:

~~~ html
<div class="toc">
  <h2>Latest Publications</h2>
  <ul class="texts">
      {{ range first 10 (where site.RegularPages.ByDate.Reverse "Type" "in" site.Params.mainSections) }}
          <li class="text-title">
              <a href="{{ .Permalink }}">{{ .Title }}</a>
          </li>
      {{ end }}
  </ul>
</div>
~~~

To override this list, create file `mini-toc.html` inside `layouts/partials` folder.

As you can see, the templating tags `{{ }}` are embedded into the HTML. These tags often use programmatic logic, as is the case here. However, another use of these tags is pull data from your project. In the example above it pulls the `Title` from each allowed post type.

As you may have noticed already, we are basically adapting the blogging features of Hugo to our own ends, what Cuban designer and theorist Ernesto Oroza would call "{{< link src="https://www.ernestooroza.com/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}technological dissobedience{{< /link >}}".

The second kind of table of content is exemplified in this documentation. If you open the source file for the documentation, you will notice at the top this snippet:

~~~ markdown
{{</* toc */>}}
~~~

This is the Hugo way. The shortcode, `{{</* toc */>}}` tells the processor to create a table of contents based on headers in the document. You can use this syntax in any page on the site that uses headers.

The third way is simple as the previous one, but very useful for long texts. If we enable the table of contents in the YAML front matter of a page:

~~~ yaml
toc: true
~~~

Ed will activate the optional table of content sidebar (`layouts/partials/sidebar-toc.html` in Ed) and move the table of contents to a special sidebar for that page. *Narrative of the Life* uses this method for its table of content.

The internal links pointing to the right sections in your document are generated from the title names automatically. If you can figure out how Ed accomplishes this trick, you have graduated from the Ed school of minimal editions.

---

## Comments

Ed theme now supports adding a comments system to your site, enhancing interactive engagement. Currently, the theme supports integration with {{< link src="https://giscus.app/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}giscus{{< /link >}}.

{{< link src="https://giscus.app/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}giscus{{< /link >}} is a comments system powered by {{< link src="https://docs.github.com/en/discussions/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}GitHub Discussions{{< /link >}}. It leverages GitHub's infrastructure to provide a free, open source platform for comments.

giscus operates by linking your website's comment section directly to GitHub Discussions. Here’s an overview of the process:
- When a page with giscus integration loads, it uses the {{< link src="https://docs.github.com/en/graphql/guides/using-the-graphql-api-for-discussions#search" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}GitHub Discussions search API{{< /link >}} to locate a discussion that matches the page. The association is determined based on a chosen mapping strategy such as URL, pathname, or the page's `<title>`.
- If no existing discussion matches the page, giscus is configured to automatically create a new discussion when a visitor posts the first comment or reaction. This ensures that each page can have its own dedicated discussion thread, even if one was not previously set up manually.
- To post a comment, visitors must authorize the giscus application via the GitHub OAuth flow, which grants the app permission to {{< link src="https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/authenticating-with-a-github-app-on-behalf-of-a-user" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}post comments on their behalf{{< /link >}}. This authorization is a straightforward process, typically requiring just a few clicks to connect a GitHub account.
- Alternatively, visitors can choose to comment directly within the GitHub Discussions platform. This flexibility allows users familiar with GitHub to engage in the discussion using an interface they are comfortable with.
- All comments posted through giscus are hosted and moderated on GitHub, leveraging GitHub's native tools for managing discussions. This integration allows site owners to manage comments using the same workflows they use for other GitHub activities, providing a seamless moderation experience.

Integrating giscus not only activates the dynamic interaction capabilities of GitHub Discussions on your Hugo site but also simplifies the management of user comments and engagements.

To enable giscus in your Hugo site, you must first add configuration settings in the site's YAML configuration file (`config/_default/params.yaml`). Below is a template for setting up giscus, which includes enabling the system and specifying necessary identifiers that link your site with the giscus service:

To enable giscus, you need to add the following to the site configuration file:

~~~ yaml
comments:
  enable: false  # Set to true to enable comments globally
  type: giscus

  giscus:
    # Required parameters:
    # Replace with your repository
    repo: 'your-github-username/repository-name'
    # Repository ID from giscus setup
    repoId: 'repository-ID'
    # Discussion category
    category: 'Announcements'
    # Category ID from giscus setup
    categoryId: 'category-ID'

    # Optional parameters:
    #
    # ...
~~~

You can obtain the `repoId` and `categoryId` by configuring your repository on the {{< link src="https://giscus.app/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}giscus setup page{{< /link >}}. More details can also be found there.

### Comment Configuration for Content Types

In the Ed theme, comments are disabled by default for all content types to maintain simplicity and focus for users. This includes all posts (poems, narratives, dramas, and blog posts) and pages. This setting helps ensure that comments are only enabled where they are explicitly needed, allowing for more granular control over site interactions.

~~~ yaml
# Default configuration in params.yaml to disable comments globally
comments:
  enable: false
  # ...
~~~

If you wish to enable comments on specific posts to encourage community interaction, you can override the default setting in the front matter of each post:

~~~ yaml
# Example of enabling comments in the front matter of a post
---
title: Exploring Narratives
comments: true
---
~~~

This allows you to selectively activate comments on content that benefits from user engagement, such as articles, stories, and discussions.

For sites where community feedback is integral across all posts, comments can be enabled globally through the site's configuration file:

~~~ yaml
# Enable comments globally in params.yaml
comments:
  enable: true
  # ...
~~~

This setting will activate comments for all posts but will not affect pages, as comments on pages are not supported. This approach is consistent with the theme’s design to keep static pages like "About" and "Contact" free from comments, ensuring these pages remain streamlined and professional.

### Styling Comments

By default, giscus will inherit the styling from your GitHub discussion forum. However, you can customize the appearance to better fit your site's design by specifying a `theme` parameter in the giscus configuration block:

~~~ yaml
comments:
  # ...

  giscus:
    # Required parameters:
    #
    # ...

    # Optional parameters:
    # Available themes: cobalt, dark, light, dark, purge, etc.
    theme: dark_dimmed
~~~

Refer to the {{< link src="https://github.com/giscus/giscus/blob/main/ADVANCED-USAGE.md#data-theme" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}giscus theme documentation{{< /link >}} for more details on available themes.

### Localization

giscus supports multiple languages, and you can set the desired language for your comments section through the `lang` parameter:


~~~ yaml
comments:
  # ...

  giscus:
    # Required parameters:
    #
    # ...

    # Optional parameters:
    # Use language codes like 'en' for English, 'es' for Spanish, etc.
    lang: fr
~~~

---

This enhancement to the Ed theme allows you to leverage the power of community discussions directly on your site, making it more dynamic and engaging for visitors.

For more information on giscus, visit the {{< link src="https://giscus.app/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}giscus website{{< /link >}}.

---

## Getting help

That should do it. If you have suggestions on how to improve Ed, make sure to leave us a line on {{< link src="https://github.com/sergeyklay/gohugo-theme-ed/issues" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}our issues page{{< /link >}}, or send us a pull request. If you run into an issue that isn't answered by this documentation or the `{{< link src="https://github.com/sergeyklay/gohugo-theme-ed/tree/main/exampleSite" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}exampleSite{{< /link >}}`, then visit the {{< link src="https://discourse.gohugo.io/" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}Hugo forum{{< /link >}}. The folks there are helpful and friendly. **Before** asking your question, be sure to read the {{< link src="https://discourse.gohugo.io/t/requesting-help/9132" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}requesting help guidelines{{< /link >}}. Feel free to tag me in your question, my forum username is {{< link src="https://discourse.gohugo.io/u/egrep/summary" class="external" target="_blank" hreflang="en" rel="noopener noreferrer" >}}@egrep{{< /link >}}.



