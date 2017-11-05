# The browser displays the page

The browser's functionality is to present the web resource you ask for (usually an HTML document, but may also be a PDF, image, or some other type of content).

The way the browser interprets and displays HTML files is specified in the HTML and CSS specifications. These specifications are maintained by the W3C (World Wide Web Consortium) organization, which is the standards organization for the web.

Once the server supplies the resources (HTML, CSS, JS, images, etc.) to the browser it undergoes the below process:

- browser checks the status code of the response. Redirects (3xx), authorization requests (401), errors (4xx and 5xx) are handled differently from normal responses (2xx)
- if cacheable, response is stored in cache
- browser decodes response (e.g. if it's gzipped, and/or encrypted)
- Parsing - HTML, CSS, JS [(explore)](./parsing/)
- Rendering [(explore)](./rendering/)

It's important to understand that this is a gradual process. For better user experience, the rendering engine will try to display contents on the screen as soon as possible. **It will not wait until all HTML is parsed before starting to build and layout the render tree**. Parts of the content will be parsed and displayed, while the process continues with the rest of the contents that keeps coming from the network.
