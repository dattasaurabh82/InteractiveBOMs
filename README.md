# InteractiveBOMs

![build and publish](https://github.com/dattasaurabh82/InteractiveBOMs/actions/workflows/create_ibom.yml/badge.svg)

## Context

The purpose of this repository is to host the board's JSON file exported (using [brd2json](https://github.com/Funkenjaeger/brd2json) from my Fusion360 Electronics).

Every time a commit is made to this repository a Github Actions CI+CD pipeline (which uses [iBOM](https://github.com/openscopeproject/InteractiveHtmlBom) and __github-pages__ to generate an html page of the interactive BOM and deploy it to the github pages. 

> Mine's at: [dattasaurabh82.github.io/InteractiveBOMs/](https://dattasaurabh82.github.io/InteractiveBOMs/)


_The Board's name and the JSON file's prefix name, doesn't matter._


So ultimately I can see the iBOM from another computer/mobile device/tablet near my soldering station during assembly.

It can be accessed here: http://current_ibom.dattasaurabh.com/output/ibom.html

And I have a dedicated old phone for it near my soldering station, where if anything changes, I can refresh and get the new design. 
![PXL_20220119_105101144 PORTRAIT](https://user-images.githubusercontent.com/4619862/150786882-3e561709-9d1d-4950-b78c-a6ce47b46438.jpg)

__Bonus tip__: My local repo of this, uses [gitomatic](https://github.com/muesli/gitomatic) to watch the folder and everytime I replace the .brd and .json files in there, it commits them to this remote repo and the generation of iBOM, followed by hosting of the html page, begins. 

