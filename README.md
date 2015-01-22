learn-git
=========

This repo is associated with a set of tasks for Google Code In 2014.

Contents of each task was as following.

```text
Important: For this task you need to have a basic familiarity of git.

In this task you have to follow a set of steps and Document what you learn out of it.

Check out this project at Github https://github.com/RoonyH/learn-git

Clone it.

git clone https://github.com/RoonyH/learn-git.git

cd learn-git
git log

You should see 6 commits.

 

_________________________________________________________________

Here's the story behind those commits.

* Forget the first commit (Initial Commit) for now.

* The next commit adds a new file to the repo.

* The third adds another file to the repo. But the commit message has gone wrong. The committer has mistakenly put "bbbad message" when what he actually meant to put was "Added the second file". Such a common mistake; Could have happened to anyone :)

* The forth adds a line to the second.txt file. It contains a typo. But not noticing this the work has been commited. "I am so mad to be here" really should have bee "I am so glad to be here"

* So the fifth commit corrects it.

* Sixth adds another file.

Install gitk and go through the commit list to understand the story.

sudo apt-get install gitk

gitk

Or you can look at commits list on Github.

Take screen shots. _________________________________________________________________

Your task is to follow the simple steps that follow to get this repo into a cleaner state.

first of all do a git log and take a screen shot.

We are using git interactive rebase to do this. Don't worry if you don't know what that is you can learn while using it.

run,

git rebase -i 8d9cbc6a337

8d9cbc6a337 is (a prefix to) the commit hash of the first commit. We are telling git to make an interactive rebase upto that commit from the current one. Now take a screenshot of what you see. You should see following info on an editor.

pick a5761b2 Added the first file
pick 547165e bbbad messege
pick e84e89f Added a line to the second file
pick de19645 Oops! typo fixed
pick 95a88fd Added one final task

# Rebase 8d9cbc6..95a88fd onto 8d9cbc6
#
# Commands:
# p, pick = use commit
# r, reword = use commit, but edit the commit message
# e, edit = use commit, but stop for amending
# s, squash = use commit, but meld into previous commit
# f, fixup = like "squash", but discard this commit's log message
# x, exec = run command (the rest of the line) using shell
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.
#
# Note that empty commits are commented out

Read it. Try and understand it. Lines that begin with # are comments. They help you to decide what to put at the top lines without a # at the beginning. They are the commands.

Now we want to fix the second commit. We just need to "use commit, but edit the commit message". Can you figure out what change you should do to the text file.

YES. we need to reword the second commit, so change this file to following

pick a5761b2 Added the first file
reword 547165e bbbad messege
pick e84e89f Added a line to the second file
pick de19645 Oops! typo fixed
pick 95a88fd Added one final task

# Rebase 8d9cbc6..95a88fd onto 8d9cbc6
#
# Commands:
# p, pick = use commit
# r, reword = use commit, but edit the commit message
# e, edit = use commit, but stop for amending
# s, squash = use commit, but meld into previous commit
# f, fixup = like "squash", but discard this commit's log message
# x, exec = run command (the rest of the line) using shell
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.
#
# Note that empty commits are commented out

Save and exit the editor. Now your text editor should be open again with this.

take a screen shot.

bbbad messege

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# Author: Aruna Herath <arunabherath@gmail.com>
#
# rebase in progress; onto 8d9cbc6
# You are currently editing a commit while rebasing branch 'master' on '8d9cbc6'.
#
# Changes to be committed:
# new file: second.txt
#

You know what to do.

Add the correct commit message and save and exit editor.

Do a git log.
You are probably getting tired of this but take the screenshot.

Figure out on your own what we need to do to fix the fifth commit (de19645). Hint: its squash :)

Fix it and don't forget the screen shot.

Now comes the most important part,

Put all those screenshots and write a blog post on what you just learned!
It should help someone else to learn basics of git interactive rebasing.
```

And students came up with some great work!

# Students' work

* http://sharpcoderock.blogspot.in/2014/12/git-interactive-rebasing.html
* https://github.com/amroto/Git-Rebasing-Tutorial
* http://iamikram.wordpress.com/2015/01/02/lets-flash-out-our-faults-d-using-github-p/
* http://awblog.blog.com/2015/01/01/learn-git/
* http://gcicodingarticles.blogspot.in/2015/01/learn-git-interactive-rebasing.html
