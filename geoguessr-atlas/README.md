# GeoGuessr Atlas

Your personal GeoGuessr reference website.

## Folder structure

```
geoguessr-atlas/
├── index.html          ← The world map (main page)
├── style.css           ← Shared styles (don't edit unless you want to change design)
├── countries/
│   ├── _TEMPLATE.html  ← Copy this to create a new country page
│   ├── portugal.html   ← Example country page
│   ├── japan.html      ← Example country page
│   └── ...             ← Add more country pages here
└── images/
    └── ...             ← Put your screenshots/photos here
```

## How to add a new country

1. Copy `countries/_TEMPLATE.html`
2. Rename it, e.g. `countries/brazil.html`
3. Open it in Notepad or VS Code and fill in the info
4. In `index.html`, find the COUNTRIES object and add a line:
   ```js
   "BR": { name:"Brazil", flag:"🇧🇷", diff:"hard", page:"countries/brazil.html" },
   ```
5. Save and upload to GitHub

## How to add images

1. Save your screenshot/photo into the `images/` folder
2. In the country HTML file, find the `<img>` tag and change `src`:
   ```html
   <img src="../images/brazil-poles.jpg" alt="Poles in Brazil"/>
   ```

## How to publish on GitHub Pages

1. Go to github.com and create a repo called `geoguessr-atlas`
2. Upload ALL these files (keeping the folder structure)
3. Go to Settings → Pages → Source: Deploy from branch → main → / (root)
4. Your site will be live at: https://lukcifergh.github.io/geoguessr-atlas

## Difficulty levels

In index.html, each country has `diff:"easy"`, `diff:"medium"`, or `diff:"hard"`.
This controls the color on the world map.
