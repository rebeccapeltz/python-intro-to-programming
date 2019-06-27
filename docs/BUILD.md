# Instructions to CREATE, BUILD, PUBLISH #

## Create ##  

You can write markdown in VS Code and use CMD-SHFT-V to view. 
You can download and use the legacy Gitbook Editor  
[download legacy Gitbook Editor Mac](https://legacy.gitbook.com/editor/osx)  
[download legacy Gitbook Editor Windows](https://legacy.gitbook.com/editor/windows)  
[download legacy Gitbook Editor Linus](https://legacy.gitbook.com/editor/linux)  


## Build and Publish ##
Install node from [nodejs.org](https://nodejs.org/en/download/)  

Install yarn globally    
`npm install -g yarn`

Install gulp globally  
`npm install -g gulp`

Build HTML from Markdown    
You should see a _books folder with the html files    
`gitbook build`  or `gitbook serve`  

Build, Copy to Docs and Publish the html to gh-pages  
Book is hosted on Github.io via Docs directory.        
`gulp`  




