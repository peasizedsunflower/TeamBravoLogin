# TeamBravoLogin

## Fork the repository
## go to your copy on your github profile and clone it.
## Create a new branch, work on it and then push it to your repository
## Open a pull request then i will merge it

# Keep forked repository in sync

*The images used are not from this repository, it is there to make you understand how to go about updating*

_After Forking and cloning your repository, you start contributing to the main repository and after a while, you notice that your forked repository and the upstream repository are not in sync anymore, usually noticed when your branch have conflicts with the main branch. This guide will make you get the current version of the upstream repository._

## Add the Upstream

The original repository is mostly called `upstream` . In our case, that would be `https://github.com/giftapad/main_files.git` , `cd` into your forked repository, you should preferably be on the `master` branch. To add `upstream` you use the command;

`git remote add upstream git://github.com/RaphaelNagato/TeamBravoLogin.git`

Using the `git remote -v` command after, you should see the following;

![ScreenShot](https://res.cloudinary.com/raphaelnagato/image/upload/v1567518500/clodinary_upstream.png)

if you made any mistakes in the URL when adding the upstream, you could always use `git remote remove upstream` , and repeat the process again .

## Fetch and Merge upstream with forked repository

Now that we have both URLs, we can now use the command `git fetch upstream` to fetch all the changes from the upstream and then we merge the changes using:

`git merge upstream/master master`.

you can do all this with just `git pull` i.e `git pull upstream master`

## Keeping remote origin up to date

After the previous step, if you type the command `git status` , you should get a message like;

![ScreenShot](https://res.cloudinary.com/raphaelnagato/image/upload/v1567519673/behind_giftapad.png)

This is because, you have only updated your local repository, to update your remote repository, that is the one on GitHub,you will have to use `git push` command i.e `git push -u origin master`.

refreshing your remote repository on GitHub should show that your `branch` is even with `RaphaelNagato:master`.

