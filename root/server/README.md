# The server processes the request

- Optionally, a firewall/load balancers receive the request first ans dispatch it to the appropriate destination
- On the destination server, the HTTPD (HTTP Daemon) receives the request. The HTTPD server is the one handling the requests/responses on the server side. The most common HTTPD servers are Apache or Nginx for Linux and IIS for Windows.
- The HTTPD breaks down the request and run some checks and rewrites
- If needed, the HTTPD forward the request to an app
- The app generates a response (usually HTML)
- The HTTPD streams the output to the client
