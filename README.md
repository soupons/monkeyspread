# monkeyspread

monkeytype but for spreading drills. pulls random evidence from an imported verbatim file based on selected criteria, times reading time and gives analytics.

## run it

it's a static site. the built-in documents load with `fetch` so serve the folder over HTTP:

```
python3 -m http.server
```

then open http://localhost:8000. opening `index.html` straight from disk still works for uploaded `.docx` files, but not for the built-in docs.

## add documents

Put a `.docx` in `docs/` and add an entry to the `DOCS` list near the top of the script in `index.html`. cards are read the way Verbatim formats them and highlighting is what gets counted as a word.

you can also upload a file in the page itself. uploads are parsed in the browser and **are never sent anywhere**.
