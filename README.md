# R16 animator portfolio

A single-page portfolio for Roblox R16 animation commissions, built as a static site so it can be hosted for free on GitHub Pages.

## What's in here

```
index.html        the whole site (HTML + CSS + JS, no build step)
media/             the four reference clips, converted to small mp4/webm loops + poster images
```

The four reference gifs you uploaded (Walking, Running, Crouching, Crouch-walking) were converted from ~30MB of gif to about 600KB total of mp4/webm — same loops, but they'll actually run smoothly on a low-end PC instead of eating CPU the way autoplaying gifs do.

## Before you publish

Open `index.html` and search for these placeholders, then replace them with your real info:

- `yourname.anim` — the name in the top-left corner
- `yourname#0000` — your Discord handle
- `roblox.com/users/000000` — your Roblox profile link
- `you@example.com` — your email
- `github.com/yourusername` — your GitHub profile

Also double check the **pricing** section (`$5` / `$5` / `$7` / `$8` for walk / crouch / crouch-walk / run) — these are placeholders inside your stated $5–10 range. Change the numbers to whatever you actually want to charge per animation.

## Putting it on GitHub Pages

1. Create a new repository on GitHub — name it `your-username.github.io` if you want it at the root of your GitHub domain, or anything else if you're fine with a `/repo-name/` subpath.
2. Upload `index.html` and the `media` folder to the repository (drag-and-drop on github.com works, or `git add` / `commit` / `push` if you're using git locally).
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to "Deploy from a branch," pick the `main` branch and the `/ (root)` folder, then save.
5. GitHub gives you a live URL a minute or two later — usually `https://your-username.github.io` or `https://your-username.github.io/repo-name`.

## Adding more reference clips later

Each work-sample card in `index.html` is a self-contained block inside `<section id="work">`. Copy one of the existing `.clip-card` blocks, point its `<source>` tags at a new file in `media/`, and update the filename/frame-count/description text. Keep new clips small (under ~200KB) so the page stays fast — if you're starting from a gif, the same mp4/webm conversion used here will get you there.
