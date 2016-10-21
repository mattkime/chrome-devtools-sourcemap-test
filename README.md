# chrome-devtools-sourcemap-test

This project exposes flaws with Chrome DevTools Node.js sourcemap support.

Verification of existing index.js sourcemap -

Open index.html in chrome and look at the console output and source list. The script will output '4' but more importantly you'll see `index.es6.js` in the source list.

Chrome DevTools sourcemap failure -

Run `npm start` in the console and open the resulting url. Hit Resume on the debugger. The script will run to completion. Take a look at the source file list - `index.es6.js` is not present.

---

You can rebuild index.js/index.js.map with `npm install && npm run build` although I've checked in the results.
