# Github hosted presentations

1. Create github repository

2. Clone your repository 

   > `git clone https://github.com/tdelev/presentations.git presentations`

3. Create `gh-pages` branch

   > `git checkout --orphan gh-pages`

3. Add reveal.js dependency in your repository 

   > `git remote add reveal.js https://github.com/hakimel/reveal.js.git`

4. Fetch the contents

   > `git fetch reveal.js`

5. Checkout `reveal.js/master` branch in your own branch `reveal_branch`

   > `git checkout -b reveal_branch reveal.js/master`
   > 'git push origin reveal_branch' optionally push the branch to github 

6. Return back to your branch

   > `git checkout gh-pages`

7. Add subfolder **revealjs** from `reveal_branch/master` in your current repository

   > `git read-tree --prefix=revealjs/ -u reveal_branch`

8. Commit and push the changes

   > `git commit -am "Added revealj subdirectory"
   > `git push`

## Updating your subfolder **revealjs**

1. Switch to `reveal_branch` and pull changes

   > `git checkout reveal_branch`
   > `git pull`

2. Switch back to `gh-pages` branch and merge changes

   > `git checkout gh-pages`
   > `git merge --squash -s subtree --no-commit reveal_branch`

   To view the diff in you subtree
   > `git diff-tree -p rack_branch`




[http://git-scm.com/book/en/Git-Tools-Subtree-Merging](http://git-scm.com/book/en/Git-Tools-Subtree-Merging "Subtree merging")