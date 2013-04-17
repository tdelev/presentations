# Github hosted presentations

1. Create github repository

2. Clone your repository 

`git clone https://github.com/tdelev/presentations.git presentations`

3. Add reveal.js dependency in your repository 

`git remote add reveal.js https://github.com/tdelev/reveal.js.git`

4. Fetch the contents

`git fetch reveal.js`

5. Subtree merging

`git checkout -b reveal_branch reveal.js/master` 


[http://git-scm.com/book/en/Git-Tools-Subtree-Merging](http://git-scm.com/book/en/Git-Tools-Subtree-Merging "Subtree merging")