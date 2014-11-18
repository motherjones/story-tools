# Mother Jones's Storytelling Tools
A how-to guide for folks in the Mother Jones newsroom. **Note:** This walkthrough pretty much only applies to folks at Mother Jones. All of our spreadsheet templates are publicly viewable and copy-able, however.

## Index

* [List of tools](#list-of-tools)
* [How we work](how-we-work)
* [Setting up your machine](#setting-up-your-machine)
* [Starting a new project](#starting-a-new-project)
* [Coordinating with the newsroom](#coordinating-with-the-newsroom)

## List of tools

[Full list](https://github.com/motherjones/story-tools/blob/master/list.md)

##How we work

Here's an overview of how we use these tools at Mother Jones. Step-by-step instructions are [below](#starting-a-new-project).

Most of our tools are powered by Google Spreadsheets. We have sample spreadsheet templates that you can copy and modify for your story.

Next, you'll use the command line to make a copy of the tool you want from our Github library. This copy will live on your machine, or "locally." Then, you'll use a text editor to make it match the data in your spreadsheet.

Once your "local" version of the tool is working properly, you'll upload your version to the cloud using Amazon Web Services S3, a cloud-based file-storage service, so that you can make it publicly viewable.

Finally, you'll link to this public version of your project from our CMS.

## Setting up your machine

To use these tools, there are a few things you'll need to download or set up on your machine.

* Admin access on your machine. Talk to Ross.

* A good text editor. We prefer [SublimeText](http://www.sublimetext.com/).

* You'll be using the command line to access our GitHub account. All Macs have a built-in command line program called Terminal. You can use that, but we prefer [iTerm2](http://www.iterm2.com/#/section/home).

* We use GitHub for "version control," or keeping files neatly organized and easy to ctrl+Z if anything breaks. [Download Git](http://git-scm.com/downloads). Then, set up a new GitHub account for yourself and follow [this guide](https://help.github.com/articles/set-up-git/) to connect your GitHub account to your computer.

* Finally, you need to link your account to the Mother Jones [GitHub account](https://github.com/motherjones). Talk to Tasneem.

* [S3 Organizer](#), the Firefox plugin for uploading to [Amazon S3](#), a cloud-based file storing service, as well as access to our files on s3. Talk to Robert.

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

On the tool's README section, open the Spreadsheet Template link. When it opens in Google Docs, go to ``File > Make a Copy``. Give your project a working title.

``File > Move to Folder > Mother Jones Drive > folder for your beat``. Make Mother Jones the owner of the spreadsheet under ``Sharing > Owner``.

Replace the data in the spreadsheet with the data for your project. Check the README for specifics.

``File > Publish to the Web`` Publish just the sheet with your data. Make sure that automatic republishing is turned on. Notice the URL that's created after you hit Publish; you'll need that later.

#### 2. Make a copy of the tool

Create a new private repo under the Mother Jones account ([how-to](https://help.github.com/articles/create-a-repo/))

Duplicate the tool and push to the new repo ([how to](https://help.github.com/articles/duplicating-a-repository/))

In SublimeText, open the main folder of your repo. Replace the spreadsheet key in ``script.js`` with the URL to your new spreadsheet. It usually looks something like this:

      Tabletop.init( { 
        key: 'https://docs.google.com/spreadsheet/pub?key=0AuHOPshyxQGGdDFnemtSV2tCXzJDOFNfeDNQY2lvb2c&output=html',
        callback: makeTable, 
        simpleSheet: true,
    } )

Change any other variables or copy that you need. Hopefully, the tool's README page will help. Open the ``index.html`` file in a browser like Chrome or Firefox to check your progress.

Add, commit, and push your changes as you go.

#### 3. Upload to s3

Open S3 Organizer in Firefox. The left-hand pane shows files on your machine (aka "local"). The right-hand pane shows files in the cloud. Upload your local files to the right place in the cloud. Notice the icons in the top-right corner of the screen; you use these to move around, make new directories, and so on.

After your files have been uploaded, right-click on the main project folder. ``Edit ACL`` and change the permissions as needed. Click "Apply to subfolders" to change all your files at once.

Finally, right-click on your ``index.html`` file to copy the distribution URL (you want the one on the bottom). You'll need this in the next step.

#### 4. Embed in the shell

We use [Pym.js](http://blog.apps.npr.org/pym.js/) to embed projects into stories via our CMS. Here's what you need to put in the Source view:

      <div id="graphic"></div>
      <script type="text/javascript" src="http://assets.motherjones.com/interactives/plugins/pym.js/src/pym.js"></script>
      <script>
            var pymParent = new pym.Parent('graphic', 'replaceme.html', {});
      </script>

Your distribution URL goes in the place of ``replaceme.html``. Check that things are working in the latest versions of Firefox, Chrome, and Safari, and test on an iPhone 4 or later as well.

#### 5. After publishing:

* Replace the working title of your spreadsheet with the headline on your published article
* Convert private repo to public
* If you made useful design improvements to the tool, go back to the tool's original repo and make these changes there

## Coordinating with the newsroom

Of course, stories involve a lot more than spreadsheets and html files. Here is a list of non-technical but very important editorial concerns when it comes to publishing your story: 
[Editorial needs](https://github.com/motherjones/story-tools/blob/master/newsroom.md)
