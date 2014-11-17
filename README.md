# Mother Jones's Storytelling Tools

Each tool has a README page, which is like a user's manual. The README will have a link to a spreadsheet template that shows you how your project's data needs to look to work with the tool. Open that link, then go to File > Make a Copy. Name your project, then go to File > Move to Folder > Mother Jones Drive, and then whatever beat folder your project should go in.

Replace the data in the spreadsheet with the data for your project. Different tools have different rules around changing column names, order, and so on. Check the README for these rules. 

When you've replaced the demo data with your project data, go to File > Publish to the Web and publish just the sheet with your data. Make sure that automatic republishing is turned on. Notice the URL that's created after you hit Publish; you'll need that later.

Grab a copy of the tool you want from Mother Jones's GitHub page.
Open up the copy's files in a text editor (a program for editing HTML, CSS, and javascript files).
Open up the spreadsheet template 

## Setting Up Your Machine

To use these tools, there are a few things you'll need to download or set up on your machine.

* Admin access on your machine. Talk to Ross.
* A good text editor. We prefer [SublimeText](http://www.sublimetext.com/). After downloading, check out this [walkthrough](http://scotch.io/bar-talk/the-complete-visual-guide-to-sublime-text-3-getting-started-and-keyboard-shortcuts) for some extremely useful keyboard shortcuts and other tips.
* You'll be using the command line to access our GitHub account. There's a built-in application on all Macs called Terminal, which is a command line program. You can use that, but we prefer [iTerm2](http://www.iterm2.com/#/section/home). Download it.
* We use GitHub for "version control," which means keeping all of our files neatly organized and easy to ctr+Z if anything breaks. First, you'll need to [download Git](http://git-scm.com/downloads). Then, set up a new GitHub account for yourself and follow [this guide](https://help.github.com/articles/set-up-git/) to use Terminal or iTerm2 to connect your GitHub account to your computer.
* Finally, you need to be added to the Mother Jones [GitHub account](https://github.com/motherjones). Talk to Tasneem.
* [S3 Organizer](#), the Firefox plugin for uploading to [Amazon S3](#), a cloud-based file storing service, as well as access to our files on s3. Talk to Robert.
* The shared Mother Jones Google Drive folder. Talk to Tasneem.

## Using GitHub

We use Github 

## Life Cycle of a MoJo interactive

* Start a Slack chat with the necessary reporters, editors, and producers
* Decide who's in charge of keeping this item updated on the slider doc
* Create a Google doc in the shared MoJo Drive folder, under the relevant beat. Make sure Mother Jones in the owner of the spreadsheet under Sharing > Owner. Share the doc URL in the Slack chat
* If you're using one of the existing tools, [duplicate](#) the tool's repo locally, then [push up](#) to a new private repo under the Mother Jones account
* Create a new directory on s3 for the project

* If full-width, confirm sign-off from Business folks
* Coordinate with fact-check and copyedit
* Talk to story editor about intro copy
* Talk to story editor about byline and any additional credits
* Headline chat for both regular and social heds/decks, for each package item
* Cross-link between interactive and mainbar as needed

* Test all URLs
* Mobile and browser test on latest Chrome, Safari, Firefox, iPhone, and one popular Android
* Does any data need to be proxied?

* Keep Public Affairs in the loop for any updates on story publication
* Give Public Affairs all URLs for promo
* Talk to story editor about tweet memo

After publishing:
* Convert private repo to public
* If you made useful design improvements to the tool, go back to the tool's original repo and make these changes there

## List of tools

* [US map with tooltips](https://github.com/motherjones/spreadsheet-to-svg) For color-coded maps with state-by-state US data. Polygons only.

* [Prettylist](https://github.com/motherjones/prettylist) Generate a nicely formatted list from a spreadsheet.

* [Simple slider](https://github.com/motherjones/simple-slider/) A horizontal inline slider that works with images, videos, and any html elements.

* [Image sidebar](https://github.com/motherjones/image-sidebar) Useful for inline navs, images with captions, and so on. Can be horizontal or vertical.

* [Newsquiz](https://github.com/motherjones/newsquiz) A simple quiz app with lots of options for using images. 

* [Choose Your Own Adventure](https://github.com/motherjones/cyoa) Good for walkthrough explainers.

* [Map Table](https://github.com/motherjones/map-table) Combo map and table graphic for data about the 50 states.

* [Full-width template](https://github.com/motherjones/full-width-template) For "big" features and interactives.

* [Random sentence generator](https://github.com/motherjones/random-sentence-maker) A simple tool for randomizing phrases.

* [Madlibs](https://github.com/motherjones/madlibs) Our version of the silly phrase generator.

* [Brackets](https://github.com/motherjones/brackets) Interactive brackets for March Madness-style contests.

* [World Map](https://github.com/motherjones/world-map) World map svg with tooltips.

* [US map with d3 markers](https://github.com/motherjones/us-map-d3-markers) For putting dynamically sized markers on a US map.

* Datawrapper: Our version of the excellent [charting tool](datawrapper.de).
