# Before
The server received the request [⏮](../request/index.md)

# The server processes the request

- The HTTPD (HTTP Daemon) receives the request. The HTTPD (HTTP Daemon) server is the one handling the requests/responses on the server side. The most common HTTPD servers are Apache or nginx for Linux and IIS for Windows.
- The HTTPD breaks down the request and run some checks and rewrites
- If needed, the HTTPD forward the request to an app
- the app generates a response (usually HTML)
- the HTTPD streams the output to the client


# Next
Page is going to be displayed. [⏭](../display/index.md)
