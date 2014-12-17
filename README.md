# Mother Jones's Storytelling Tools

## Index

* [List of tools](#list-of-tools)
* [How we work](#how-we-work)
* [Setting up your machine](#setting-up-your-machine)
* [Starting a new project](#starting-a-new-project)
* [Coordinating with the rest of the newsroom](#coordinating-with-the-newsroom)

## List of tools

* [US color-coded map](https://github.com/motherjones/spreadsheet-to-svg) For color-coded maps with state-by-state US data. Polygons only.

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

##How we work
*Important caveat: This walkthrough isn't going to be very useful to non-MoJo folks. All of our spreadsheet templates are publicly viewable and copy-able, however.*

Here's an overview of how we use these tools at Mother Jones. Step-by-step instructions are [below](#starting-a-new-project).

Most of our tools are powered by Google Spreadsheets. We have sample spreadsheet templates that you'll copy and modify for your story.

Next, you'll use the command line to make a copy of the tool you want from our Github library. This copy will live on your machine, or "locally." Then, you'll use a text editor to match it up with your spreadsheet.

Once your "local" version of the tool is working properly, you'll upload it to the cloud using Amazon Web Services S3, a cloud-based file-storage service, where it becomes publicly viewable.

Finally, you'll embed this public version of your project in an article via our CMS.

<p align="center">
  <img width="75%" src="https://raw.githubusercontent.com/motherjones/story-tools/master/flowchart.png" alt="screenshot"/>
</p>

## Setting up your machine

To use these tools, there are a few things you'll need to download or set up on your machine.

* Admin access on your machine. Talk to Ross.

* A good text editor. We prefer [SublimeText](http://www.sublimetext.com/).

* You'll be using the command line to access our GitHub account. All Macs have a built-in command line program called Terminal. You can use that, but we prefer [iTerm2](http://www.iterm2.com/#/section/home).

* We use GitHub for "version control," or keeping files neatly organized and easy to ctrl+Z if anything breaks. [Download Git](http://git-scm.com/downloads). Then, set up a new GitHub account for yourself and follow [this guide](https://help.github.com/articles/set-up-git/) to connect your GitHub account to your computer.

* Finally, you need to link your account to the Mother Jones [GitHub account](https://github.com/motherjones). Talk to Tasneem.

* [S3 Organizer](http://www.s3fox.net/), the Firefox plugin for uploading to [Amazon S3](http://www.hongkiat.com/blog/amazon-s3-the-beginners-guide/), a cloud-based file storing service, as well as access to our files on s3. Talk to Robert.

* The shared Mother Jones Google Drive folder. Talk to Tasneem.

#### Some good background

The tools, languages, and concepts you'll encounter when working with these tools might be totally new to you. Here are some good backgrounds:

* [HTML and CSS](http://css-tricks.com/video-screencasts/58-html-css-the-very-basics/)
* Github: [1](https://try.github.io/levels/1/challenges/1) and [2](http://rogerdudler.github.io/git-guide/)
* [Command line](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line)
* [Text editors](http://scotch.io/bar-talk/the-complete-visual-guide-to-sublime-text-3-getting-started-and-keyboard-shortcuts)
* [Amazon S3](http://www.hongkiat.com/blog/amazon-s3-the-beginners-guide/)

## Starting a new project

#### 1. Upload your data

Go to the Github page of the tool you want to use. Read through the README, then open the Spreadsheet Template link. When it opens in Google Docs, go to ``File > Make a Copy``. Give your project a working title.

``File > Move to Folder > Mother Jones Drive > folder for your beat``. Make Mother Jones the owner of the spreadsheet under ``Sharing > Owner``.

Replace the data in the spreadsheet with the data for your project. Check the README for specifics.

``File > Publish to the Web`` Publish just the sheet with your data. Make sure that automatic republishing is turned on. Notice the URL that's created after you hit Publish; you'll need that later.

#### 2. Make a copy of the tool

Create a new private repo under the Mother Jones account ([how-to](https://help.github.com/articles/create-a-repo/)).

<p align="center">
  <img width="75%" src="https://raw.githubusercontent.com/motherjones/story-tools/master/new-repo.png" alt="screenshot"/>
</p>

Name it with the slug of your story + the name of the tool, i.e.: [rape-statutes-map-table](https://github.com/motherjones/rape-statutes-map-table). 

Now you're going to make a copy of the tool you want to use and stick it in the new repo. Here's a screenshot of all the commands you'll need (replacing your repo names as needed). The portions that are blacked out are messages back from the terminal. 

You can also find the same commands here: ([how to](https://help.github.com/articles/duplicating-a-repository/)). 

<p align="center">
  <img src="https://raw.githubusercontent.com/motherjones/story-tools/master/terminal.jpg" alt="screenshot"/>
</p>


In SublimeText, open the main folder of your repo. At this point, go check out the tool's own README page for further instructions. 

As you make changes these changes, you need to update your project file's on GitHub to match what you're doing on your own machine (essentially saving as you go). Check out these tutorials for a basic intro to GitHub commands:

* Github: [1](https://try.github.io/levels/1/challenges/1) and [2](http://rogerdudler.github.io/git-guide/)
* [Command line](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line)

Here are the commands you'll use over and over:

* ``cd`` open and go into a folder on your machine

* ``git status`` check to see if you have unsaved changes

* ``git add --all`` add all your changes to be saved

* ``git commit -m "Message here"`` decribe your changes

* ``git pull`` check that no one else has uploaded any new changes

* ``git push`` finally, upload your changes to GitHub

This screenshot shows the process of making a couple sets of changes and uploading them to GitHub:

<p align="center">
  <img src="https://raw.githubusercontent.com/motherjones/story-tools/master/more-git-commands.jpg" alt="screenshot"/>
</p>

#### 3. Upload to s3

Open S3 Organizer in Firefox. The left-hand pane shows files on your machine (aka "local"). The right-hand pane shows files in the cloud. Upload your local files to the right place in the cloud. Notice the icons in the top-right corner of the screen; you use these to move around, make new directories, and so on.

After your files have been uploaded, right-click on the main project folder. ``Edit ACL`` and change the permissions as needed. Click "Apply to subfolders" to change all your files at once.

Finally, right-click on your ``index.html`` file to copy the distribution URL (you want the one on the bottom). You'll need this in the next step.

#### 4. Embed in the shell

We use [Pym.js](http://blog.apps.npr.org/pym.js/) to embed projects into stories via our CMS. Here's what you need to put in the Source view:

      <div id="graphic"></div>
      <script type="text/javascript" src="http://assets.motherjones.com/interactives/plugins/pym.js/src/pym.js"></script>
      <script>
            var pymParent = new pym.Parent('graphic', 'replace.html', {});
      </script>

Your distribution URL goes in the place of ``replace.html``. Check that things are working in the latest versions of Firefox, Chrome, and Safari, and test on an iPhone 4 or later as well.

#### 5. After publishing:

* Replace the working title of your spreadsheet with the headline on your published article
* Convert private repo to public
* If you made happened to make useful design improvements to the tool, talk to Tasneem about potentially making these changes to the master version as well.

## Coordinating with the newsroom

Of course, stories involve a lot more than spreadsheets and html files. Here is a list of non-technical but very important editorial concerns when it comes to publishing your story: 

[Editorial needs](https://github.com/motherjones/story-tools/blob/master/newsroom.md)
