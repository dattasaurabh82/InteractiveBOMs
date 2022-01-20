# InteractiveBOMs
The purpose of this repository is to host the board's JSON file exported (using [brd2json](https://github.com/Funkenjaeger/brd2json) from my Fusion360 Electronics).

_The Board's name and the JSON file's prefix name, doesn't matter._

Every time a commit is made to this repository a Github Actions CI+CD pipeline (which uses [iBOM](https://github.com/openscopeproject/InteractiveHtmlBom) and [github-pages](https://github.com/JamesIves/github-pages-deploy-action)) to generate an html page of the interactive BOM and deploy it to the github pages. 

So ultimately I can see the iBOM from another computer/mobile device/tablet near my soldering station during assembly.

__Bonus tip__: My local repo of this, uses [gitomatic](https://github.com/muesli/gitomatic) to watch the folder and everytime I replace the .brd and .json files in there, it commits them to this remote repo and the generation of iBOM, followed by hosting of the html page, begins.  
