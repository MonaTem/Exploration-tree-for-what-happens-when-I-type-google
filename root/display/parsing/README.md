# HTML parsing

The job of HTML parser to parse the HTML markup into a `parse tree`. The `parse tree` is the object presentation of the HTML document and the interface of HTML elements to the outside world like JavaScript. The root of the tree is the `document` object. Prior of any manipulation via scripting, the DOM has an almost one-to-one relation to the markup.

Elements are parsed in this order :

- First, the html of the page
- Then, external resources linked to the page (CSS, images, JavaScript files, etc.). At this stage the document state is set to `interactive`.
- Finally, scripts that are in "deferred" mode: those that should be executed after the document is parsed. The document state is set to `complete` and a `load` event is fired.
