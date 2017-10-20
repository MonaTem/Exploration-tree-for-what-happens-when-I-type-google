# HTML parsing

-   The rendering engine starts getting the contents of the requested
document from the networking layer. This will usually be done in 8kB chunks.

-   The primary job of HTML parser to parse the HTML markup into a parse tree. The parse tree is a tree of DOM element and attribute nodes (Document Object Model). It is the object presentation of the HTML document and the interface of HTML elements to the outside world like JavaScript. The root of the tree is the "Document" object. Prior of any manipulation via scripting, the DOM has an almost one-to-one relation to
the markup.

-   When the parsing is finished, the browser begins fetching external resources linked to the page (CSS, images, JavaScript files, etc.) and parsing them.

-   At this stage the browser marks the document as interactive and starts
parsing scripts that are in "deferred" mode: those that should be
executed after the document is parsed. The document state is
set to "complete" and a "load" event is fired.
