First rules about git:
1. Always do *git pull* first,
2. then look and plan what small increment you will do, decide first.
3. then do *git pull* again (really important!!!)
4. only then immediately create the branch with *git checkout -b category-add-fix-juhani* where the branch name tells which feature is worked on, how and by whom,
5. then immediately work on it, and,
6. as soon as possible, (when no errors or problems of any kind exist) , *commit -m "Fix Add Category"*
7. *git push --set-upstream origin category-add-fix-juhani* to remote (same branch, not master!)
8. and make a pull request in GitHub.com web site from that branch
9. somebody else must review it (Remember that git merge understands nothing of a) our project b) the programming languages we use. It just tries to guess and merge text lines! You must know the big picture and details of the changes)
10. after accepted review look at the possible merge conflicts? Resolve if possible.
11. merge only after seeing no catastrophy coming
12. close pull request
13. delete the branch so people know that's not worked on! Either click button in GitHub.com, or change back to master branch with *git checkout master* AND delete unnecessary branch with *git branch -d category-add-fix-juhani* from command line

It's important to go from 3 to 13 as soon as possible! Don't leave branches open for any longer than absolutely necessary!

If decide to scrap all your work so far, you can jump over 6. - 12. by command *git stash* which will clear all your working folder changes going back to latest commit.

Then you can either 13. delete that branch, or start fresh from 4. But then again, you'll need to do pull from master. E.g. *git pull origin master* will make your own branch to start from current master version.

We will tweak this process later, but then it gets slightly complicated (pulling from master to your branch and merging + testing there first). Smoother, but more complicatated to understand. Then third level is to create a third branch, e.g. development and make pull requests from your branch to that first.
