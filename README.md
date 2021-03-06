# Github hosted presentations in 6 easy steps

1. Create github repository

2. Clone your repository 

   > `git clone https://github.com/tdelev/presentations.git presentations`

3. Create `gh-pages` branch

   > `git checkout --orphan gh-pages`

4. Add [reveal.js](https://github.com/hakimel/reveal.js) dependency as a submodule in a folder
named `revealjs` in your repository 

   > `git submodule add https://github.com/hakimel/reveal.js.git revealjs`
   
5. Create you presentation in a new directory `presentation_name` and to include the reveal.js
dependencies use absolute paths i.e. `/{repo_name}/revealjs/{revealjs_file}`. View example
presentation [here](https://github.com/tdelev/presentations/blob/gh-pages/docker/index.html).

6. Commit and push the changes to publish your presentation at url 
`{github_username}.github.io/{repo_name}/{presentation_name}`

   > `git commit -am "Added revealjs submodule and published my presentation"`
   
   > `git push`
   

## Updating your submodule **revealjs**

   > `cd revealjs`
   
   > `git pull`
