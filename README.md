# Open When… 💌

A little website of "Open When…" letters for a long-distance partner. Each letter is a sealed envelope. Tap one to read it, and the page remembers which ones have been opened and when.

It's a single static file (`index.html`) with no build step and no dependencies.

## Edit the letters

Open `index.html` and find the section marked `EDIT THIS SECTION`:

- `CONFIG` holds his name, your name and both cities.
- `LETTERS` is the list of letters. Each one looks like this:

```js
{icon:"💭",when:"you miss me",body:"First paragraph.\n\nSecond paragraph."}
```

Use `\n\n` for a paragraph break. Add, remove or reorder letters freely.

## Run it locally

Just double-click `index.html`, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Publish with GitHub Pages

```bash
git init
git add .
git commit -m "Open When letters"
git branch -M main
git remote add origin https://github.com/<your-username>/open-when.git
git push -u origin main
```

Then on GitHub go to **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save. Your site will be live at `https://<your-username>.github.io/open-when/` after a minute or two.

Tip: if the repo is public, anyone with the link can read the letters. Use a private repo plus a Pages plan that supports private sites, or host it somewhere that needs a password, if that matters.

## Notes

- "Opened" dates are saved in the browser's local storage, so they're per device and per browser.
- Fonts (Caveat and Fraunces) load from Google Fonts, so the page needs an internet connection to look its best.
