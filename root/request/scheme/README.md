# The browser determines the appropriate "scheme" to communicate with the destination.

- The browser checks its preloaded HSTS (HTTP Strict Transport Security) list. This is a list of websites that have requested to be contacted via HTTPS only.
- If the website is in the list, the browser sends its request via HTTPS instead of HTTP.
- Otherwise, the initial request is sent via HTTP. (Note that a website can still use the HSTS policy *without* being in the HSTS list.  The first HTTP request to the website by a user will receive a response requesting that the user only send HTTPS requests.  However, this single HTTP request could potentially leave the user vulnerable to a `downgrade attack`, which is why the HSTS list is included in modern web browsers.)
