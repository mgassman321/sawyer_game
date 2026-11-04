# xgassman.com

A small gallery of browser games and tools I've made, live at **[xgassman.com](https://xgassman.com)**.

## Projects

| Project | File | What it is |
|---|---|---|
| Sawyer's Skateboarding Superpets | `soy_game_4.html` | Pixel-art skateboarding game: pick one of eight pets and jump down the school hallway. |
| Dice | `dice_simulator_2.html` | Dice roller with Classic, Vegas and Disco themes, locking dice and running totals. |
| Spectrum Studio | `spectrum-studio_1.html` | Live audio visualizer for your mic, a browser tab or a demo track. |
| Idea Board | `stickies.html` | Corkboard of sticky-note checklists, photos and links. Saves in your browser. |
| Da Chicago Pope Hot Dog Dropper Game | `hotdog_drop.html` | Chicago street-food drop game. Inspired by the 1995 freeware Mac game [Slick Willie 2.0](https://www.macintoshrepository.org/6705-slick-willie-2-0) by Jim Byer. |

Everything is plain HTML, CSS and JavaScript: no build step, no dependencies.

## Folder layout

```
index.html      the gallery page
*.html          one file per project
images/         artwork for Superpets
icons/          gallery tile icons (source copies; index.html has them built in)
favicons/       browser-tab and home-screen icons for each page
CNAME           custom domain for GitHub Pages (managed by GitHub)
```

## Hosting

Served by **GitHub Pages** from the `main` branch, root folder. The domain is registered at Squarespace, with DNS pointing to GitHub:

- `A @` → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
- `CNAME www` → mgassman321.github.io

## Updating the site

```
cd ~/Documents/sawyer_game
git pull                     # always first: picks up changes made on github.com
git add -A
git commit -m "Describe the change"
git push
```

Changes appear on xgassman.com about a minute after pushing.

## Adding a project

1. Put the new `.html` file in this folder.
2. In `index.html`, copy one of the `<li>` tiles in the grid, then change the link, name and class.
3. Add a matching color line in the "Tile colors" CSS block.
4. Add a favicon by copying the two `<link rel="icon">` lines from another project page.

To preview locally, open `index.html` in a browser, or run `python3 -m http.server` here and visit http://localhost:8000.
