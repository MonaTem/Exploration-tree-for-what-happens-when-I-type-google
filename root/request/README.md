Previously, we "resolved" the address "google.com" to an IP address understandable by the machines of the network. We can now send messages to this machine.

# The browser sends a request to google.com

- the browser determines the appropriate "scheme" to communicate with the destination. (in our case of entering and address in the URL bar of a browser, it boils down to : http or https). For "google.com", it will be https [see why](./scheme/)
- the browser determines the appropriate port : 443 in our case. [see why](./port/)
- the browser initiate the process to agree on the encryption of the communication [explore](../../common/networking/L6/TLS/)
- the browser sends encrypted data to the server using HTTP protocol [explore](./http_request/)
