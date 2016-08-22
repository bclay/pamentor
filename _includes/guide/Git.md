Git/Github
============

Version control for the rest of us
--------------------------

### What is Git

Git is the tool that handles your version control, Github is the online repository where you store all your files. Version control records specific changes to a file or a set of files over time so that you can access specific versions later. Github stores these versions on the cloud. Since you can add multiple people to a Github repository, it's also an excellent way to collaborate with others on projects. You should try this awesome simulation-version of this tutorial [here](try.github.io). Then you should make your Github [account](https://github.com/join) with your school email.

To install git on Mac:
- Use spotlight search to find and open terminal.
- Type git into terminal. If a bunch of text is printed you have git already.
- Otherwise go [here](http://git-scm.com/downloads) and download git.

To install on Windows:
- Go [here](http://git-scm.com/downloads) and download git.

### Unix
Unix is how your operating system is organized. Everything is organized into a hierarchy similar to a tree. Everything starts in the root and goes up to the leaves-files. Files are contained in folders called directories. You get to a file through a path of directories. `$` acts as a colon, and `-` denotes the root.

### Terminal  

Terminal is your text based access to the operating system. It carries out Unix commands. Here are some helpful and common Unix commands:

 - `ls`: graphically shows current directory
 - `cd`: change directory
 - `cd ..`: takes you one level up from current directory
 - `mkdir`: make directory (creates new folder)
 - `touch`: creates file
 - `rm`: remove files, use this command wisely
 - `mv`: moves/renames files
 - `pwd`: prints path to current directory

Feel free to try some of these commands, and look up others to see how they work.


### Set Up Git
Now that we have a basic understanding of Terminal and Unix commands we can set up git.Go [here](https://help.github.com/articles/set-up-git) to set up Git. You have already completed step 1. We highly recommend setting up an SSH keypair with your computer to allow more ease of use with Github. You can do that [here](https://help.github.com/articles/generating-ssh-keys). A few things to know about using Terminal: if you enter something and there is no message afterwards that usually means it has worked, and when typing in a password it will not appear that you are typing anything, but this is also working.

### Repositories

As said before, a repository is where your code is stored on Github. You can make a repsoitory following [instructions](https://help.github.com/articles/create-a-repo). You can also see instructions on how to commit a change from Github itself.

#### How to Add Changes Using Terminal
This assumes that you have setup a SSH keypair with your computer.

- Go to your repository on Github.
- Go to the bottom right of the repository screen where it says SSH clone URL and click on the clipboard icon.
- Go to terminal and change your directory using Unix commands (`cd`) to where you want to keep the repository.
- Now type git clone, then paste the SSH clone url, and press enter.
- Move any files that you have created that you would like to be a part of this repository to this folder.
- When all files are added, go back to terminal.
- Type `git add .`
- Type `git commit -m "a message about what you will be pushing"`
- Type `git push`

If you check your Github, you will see that the files have been updated and/or added.

#### Fork a Repository
Forking a repository is something you'll want to be able to do to collaborate with others on repositories. Github's instructions on forking a repository are [here](https://help.github.com/articles/fork-a-reop).

Their instructions also walk you through creating a branch. All files in a repository automatically end up in the master branch. However, if you would like to make some changes to the main code without damaging parts of the code that are working then you can create another branch and later merge it. When you're done making edits you can merge this other branch with the master branch again.

[Go to](http://try.github.com/levels/1/challenges/10) to do more interactive tutorials!

### Webpage Hosting

Webpage hosting is what actually puts your website on the internet. Many places offer hosting for a price but Github will host your webpage for free. You can see their instructions for hosting websites [here](http://pages.github.com)


### Resources
[Here](http://rogerdu...io/git-guide/) is another excellent guide to Git!
