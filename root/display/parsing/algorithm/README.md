# The parsing algorithm

HTML cannot be parsed using the regular top-down or bottom-up parsers.

The reasons are:

-   The forgiving nature of the language.
-   The fact that browsers have traditional error tolerance to support well
  known cases of invalid HTML.
-   The parsing process is reentrant. For other languages, the source doesn't
  change during parsing, but in HTML, dynamic code (such as script elements
  containing `document.write()` calls) can add extra tokens, so the parsing
  process actually modifies the input.

Unable to use the regular parsing techniques, the browser utilizes a custom
parser for parsing HTML. The parsing algorithm is described in
detail by the HTML5 specification. Note there is never an "Invalid Syntax" error on an HTML page. Browsers fix any invalid content and go on.

The algorithm consists of two stages: tokenization and tree construction.
