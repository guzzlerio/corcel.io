# docs.corcel.io

For info these commands helped me reset and retry getting the subtree stuff to work

```shell

# removing the subtree from existence
git filter-branch --index-filter 'git rm --cached --ignore-unmatch -rf public' --prune-empty -f HEAD

# removing the gh-pages from the remote
git push origin --delete gh-pages

```

When you setup a new gh-pages branch following the hugo documentation everything is as it should be and works.  You create the deploy script and it works.  Then you go into github and set a new url for the github pages site.  Github does this by adding a file called `CNAME` into the gh-pages branch root.  This commit then prevents a subtree from working in all the attempts I have made.  

Every time I came to do a `git subtree push` it failed stating there were changes on the remote which were not in the local and it would be correct.  Doing a `git subtree pull` did not fix it though and so the only solution I could think of doing was handling the creation of the `CNAME` file manually.  Now the deploy script works without a hitch!
