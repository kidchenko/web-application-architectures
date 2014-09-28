# HTTP - Response

### HTTP - Server Side

Let us now consider the server side of this protocol. An HTTP/1.1 response message is similar to a request message. I.e., it also consists of three parts:
1. Response line
2. Header
3. Message body

After delivering the response, the server closes the connection (the default behavior with HTTP 0.9 and 1.0). With HTTP 1.1, a persistent connection is assumed by default.

### HTTP - Server Side: Response Line
- The response line is the first line of of the response provided by the server – it is called the status line.
- The status line consists of three parts:
  1. The HTTP version, in the same format as in the message request, e.g., HTTP/1.1.
  2. A response status code that provides the result of the request.
  3. An English reason phrase describing the status code.

Ex.
HTTP/1.1 200 OK
HTTP/1.1 404 Not Found

### HTTP - Server Side: Response Line
The status codes associated with the status line belong to done of five categories:
1. 1xx (Provisional Response) - A provisional response that requires the requestor to take additional action in order to continue. e.g., 100, the Continue status code, indicates that the requester should continue with the request. 101, the Switching Protocols status code, the requestor has asked the server to switch protocols (e.g., HTTPS) and the server is acknowledging that it will do so.
2. 2xx (Successful) - The server successfully processed the request.
3. 3xx (Redirected) - Further action is needed to fulfill the request. Often, these status codes are used for redirection.
4. 4xx (Request Error) - There was likely an error in the request which prevented the server from being able to process it.
5. 5xx (Server Error) - The server had an internal error when trying to process the request.

A complete list of response codes can be found in RFC 2616, the official HTTP 1.1 specification

### HTTP - Server Side: Header
- The header fields in the response allow the server to pass additional information about the response which cannot be placed in the status line.
- These header fields have the same format as in the request, and give information about the server and about further access to the resource identified by the request URI.
- Example response fields in the header include:
  - Accept-Ranges – Allows the server to indicate its acceptance of range requests for a resource.
  - Age – Sender’s estimate of the amount of time since the response was generated at the origin server.
  - Location – Used to redirect the recipient to a location other than the request URI for completion of the request or identification of a new resource.
  - Proxy-Authenticate – Allows the client to identify itself (or its user) to a proxy which requires authentication.

### HTTP - Server Side: Message Body
- The message body in the response must also be preceded by a blank line.
- The response to a HEAD request does not include a message body. All other responses do include a message body, although it may be of zero length.
- The requested resource, e.g., the actual HTML, is included in the message body of the response.

### HTTP Secure
- The HTTP Secure protocol (HTTPS) is a combination of the HTTP and SSL/TLS protocols. Thus, it makes use of the public key infrastructure.
- HTTPS enhances the HTTP protocol by providing encrypted communication and secure web server identification.
- The HTTPS protocol is often used for processing payments in web applications, or for handling other sensitive transactions.
- The trust associated with HTTPS is based on the major certificate authorities, whose software comes pre-installed in the browser. I.e., what is really happening is that your browser must trust some certificate authority (e.g. VeriSign/Microsoft/etc.) so that it can tell your browser whom it should trust.
- HTTPS URLs begin with “https://..." and uses port 443 by default.
