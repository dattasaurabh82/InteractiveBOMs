# InteractiveBOMs

![build and publish](https://github.com/dattasaurabh82/InteractiveBOMs/actions/workflows/create_ibom.yml/badge.svg)

## Context

The purpose of this repository is to host the board's JSON file exported (using [brd2json](https://github.com/Funkenjaeger/brd2json) from my Fusion360 Electronics).

Every time a commit is made to this repository a Github Actions CI+CD pipeline (which uses [iBOM](https://github.com/openscopeproject/InteractiveHtmlBom) and __github-pages__ to generate an html page of the interactive BOM and deploy it to the github pages. 

So ultimately I can see the iBOM from another computer/mobile device/tablet near my soldering station during assembly.

> Mine's at: [dattasaurabh82.github.io/InteractiveBOMs/](https://dattasaurabh82.github.io/InteractiveBOMs/)

And I have a dedicated old phone for it near my soldering station, where if anything changes, I can refresh and get the new design. 

TODO: Update image of setup

---

## If you wanna clone and push to github to host yours ...

### Setup your github for gh-pages

In your GitHub repository `settings`, you need to configure GitHub Pages:

1. Go to your repository's `Settings`
2. In the left sidebar, click `Pages`
3. Under `Build and deployment`:
   - For `Source`, select `GitHub Actions`
   - > Do not select `Deploy from a branch` since we're using the Actions workflow

That's it! You don't need to configure anything else in the Pages settings. 

The workflow we set up will handle everything:

- Building the site (generating the iBOM HTML)
- Creating the necessary artifacts
- Deploying to GitHub Pages

The first time you run the workflow, GitHub Pages will be automatically set up. 

The URL where your site will be published will be shown in:
- The workflow run output
- Your repository's Pages settings
- Usually in the format: `https://<username>.github.io/<repository>/`

### Generate board json

_The Board's name and the JSON file's prefix name, doesn't matter._

### Push

---

## Bonus tip

My local repo of this, uses [gitomatic](https://github.com/muesli/gitomatic) to watch the folder and everytime I replace the .brd and .json files in there, it commits them to this remote repo and the generation of iBOM, followed by hosting of the html page, begins. 

