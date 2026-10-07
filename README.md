# monkeyspread

A spreading drill trainer for debate, in the spirit of Monkeytype. It pulls a random card from a verbatimized Word file, times how long you take to read it, and reports words per minute counting only the highlighted words.

## Run it

It's a static site with no build step. The built-in documents load with `fetch`, so serve the folder over HTTP:

```
python3 -m http.server
```

Then open http://localhost:8000. Opening `index.html` straight from disk still works for uploaded `.docx` files, but not for the built-in documents.

## Add documents

Put a `.docx` in `docs/` and add an entry to the `DOCS` list near the top of the script in `index.html`. Cards are read the way Verbatim formats them: a Heading 4 tag, a cite line containing a year, then the body. Highlighting is what gets counted.

You can also upload a file in the page itself. Uploads are parsed in the browser and are never sent anywhere.

## Deploy

Any static host works: Netlify, Cloudflare Pages, or GitHub Pages (Settings, Pages, deploy from the `main` branch root).

## Notes

The cards in `docs/` are other debaters' work, and each one keeps its original cite.
