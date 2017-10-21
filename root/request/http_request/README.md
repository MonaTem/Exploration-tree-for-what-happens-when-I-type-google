# The browser sends data to the server using HTTP protocol

If the web browser used was written by Google, instead of sending an HTTP request to retrieve the page, it will send a request to try and negotiate with the server an "upgrade" from HTTP to the SPDY protocol.

If the client is using the HTTP protocol and does not support SPDY, it sends a request to the server of the form::

    GET / HTTP/1.1
    Host: google.com
    Connection: close
    [other headers]

where ``[other headers]`` refers to a series of colon-separated key-value pairs formatted as per the HTTP specification and separated by single new lines. (This assumes the web browser being used doesn't have any bugs violating the HTTP spec. This also assumes that the web browser is using ``HTTP/1.1``, otherwise it may not include the ``Host`` header in the request and the version specified in the ``GET`` request will either be ``HTTP/1.0`` or ``HTTP/0.9``.)
HTTP/1.1 defines the "close" connection option for the sender to signal that the connection will be closed after completion of the response. For example,

    Connection: close

HTTP/1.1 applications that do not support persistent connections MUST include the "close" connection option in every message.

After sending the request and headers, the web browser sends a single blank newline to the server indicating that the content of the request is done.
