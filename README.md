# PaaC - Presentation as a Code 
Presentation Using Markdown, Hosted on GitHub Pages :) 

### Creating presenations for your application and PaaC it like a geek, how codiful is that! 

Idea is to have the presentation built with simple mardown files and embed it within your repo, and demo it from same repo (github pages)!

### Getting Started
- Clone this Repo Template
- Write your slide deck using [Marp](https://marpit.marp.app/) Markdown
- Manage the content of slides in your own Git repo
- Convert markdown to presentable html format using node/npx command
- Commit html to git repo and enable github pages via settings tab
- Blazingly fast delivery on your presentation via Github Pages
- Sample: https://deanjain.github.io/Presentations/PATTERNS.html



### PreReq
- Install [Node.js 12+](https://nodejs.org/) 
- Clone this Repo (Template)

### Preview deck

[**Marp for VS Code**](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode) extension is the best partner for writing Marp slide deck with live preview.

<p align="center">
  <a href="https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode">
    <img src="https://raw.githubusercontent.com/marp-team/marp-vscode/master/docs/screenshot.png" width="500" />
  </a>
</p>

### Edit deck

Just edit **Your Markdown File**!

### CodeGen CLI

```yaml
npx @marp-team/marp-cli -w YourMarkdown.md                            
npx: installed 266 in 30.6s
[  INFO ] Converting 1 markdown...
[  INFO ] YourMarkdown.md => YourMarkdown.html
```

### Deploy on Github Pages
- Just go to github repo settings and enable the github pages from your root where you have hosted html file, you are now rocking!
  
### Assets and themes

- `assets` directory can put your assets for using in the deck. (e.g. Image resources)
- `themes` directory can put [custom theme CSS](https://marpit.marp.app/theme-css). To use in the deck, please change `theme` global directive.

### Other Features
- export presenation in PDF/PPT/Image format via CLI
