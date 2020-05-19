# Templates for Project 1 in 432

## Portfolio Templates

I'm providing three templates for the portfolio, all of which work well for the project, in my view, and it's easy to switch from one to another by changing the YAML at the top of the document. You are welcome to use these templates or not in preparing your work, but an argument for doing so is that you'll more or less automatically deal with [several of the specific requirements for your work](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1#new-some-additional-thoughts-after-reviewing-the-proposal-drafts) that I've laid out in the instructions for Project 1.

1. A template built using readthedown from the rmdformats package.
    - [R Markdown Code](https://github.com/THOMASELOVE/2020-432/blob/master/projects/project1/templates/proj1_template_readthedown.Rmd) 
    - [View the HTML result (on RPubs)](https://rpubs.com/TELOVE/project1_template_432-2020_readthedown)

2. A template built using html_clean from the rmdformats package.
    - [R Markdown Code](https://github.com/THOMASELOVE/2020-432/blob/master/projects/project1/templates/proj1_template_htmlclean.Rmd)
    - [View the HTML result (on RPubs)](https://rpubs.com/TELOVE/proj1_template_432-2020_clean)
    
3. A template with a floating table of contents built from plain vanilla HTML in R Markdown
    - [R Markdown Code](https://github.com/THOMASELOVE/2020-432/blob/master/projects/project1/templates/proj1_template_floatingTOC.Rmd)
    - [View the HTML result (on RPubs)](https://rpubs.com/TELOVE/pr1_template_432-2020_float)

## Highlight: How R code is presented

In each of the templates, there's an option to change the highlight style, which just changes how the R code is presented.

- Supported highlight styles include default, tango, pygments, kate, monochrome, espresso, zenburn, haddock, breezedark, and textmate. If you like, try making a change and see if you prefer the results.

## Themes (for the Floating TOC template)

- The theme command in the YAML specifies the Bootstrap theme to use for the page (themes are drawn from the [Bootswatch theme library](https://bootswatch.com/3/)). Valid themes include default, cerulean, journal, flatly, darkly, readable, spacelab, united, cosmo, lumen, paper, sandstone, simplex, and yeti. Again, feel free to try alternatives to see if you like them.

Just make sure I can read the result easily.

Check out https://bookdown.org/yihui/rmarkdown/html-document.html for more on customizing your HTML output.

## NEW! Poster Template

I have now provided a posterdown template for your use in developing your Poster for Project 1. To use the template, you'll need to have the posterdown package installed in R.

- [R Markdown Code for Poster](https://github.com/THOMASELOVE/2020-432/blob/master/projects/project1/templates/proj1_template_posterdown.Rmd)
- [View the HTML result of the Poster (on RPubs)](https://rpubs.com/TELOVE/poster_template_2020-432)
    
If you want to customize the poster further, the [most useful page I found is here](https://github.com/brentthorne/posterdown/wiki/posterdown_html).

My best piece of advice is to build the poster and then knit it, and then open the knitted version in the browser, so you can scroll around more easily and shrink the poster to view it as I will.

- Your audience for the poster consists of Dr. Love, the TAs and your fellow students. Write it to interest them in what you've done.
