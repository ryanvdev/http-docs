# Cross-Origin Resource Sharing

 Cors error is a security error that occurs when a web browser tries to access a resource from a different domain than the one that served the page. This is done to prevent malicious websites from accessing sensitive data on other websites.

`CORS` errors can be caused by a number of things, including:

- The server does not have the necessary CORS headers configured.
The client is trying to access a resource from a domain that is not allowed by the server's CORS configuration.
- The client is trying to send credentials (such as cookies or HTTP authentication headers) with a cross-origin request, but the server is not configured to allow this.

## Resolve cors error

To resolve cors error you must response some headers to browser for each request.

### `Access-Control-Allow-Credentials`

Browsers will only expose the response to the frontend JavaScript code if the Access-Control-Allow-Credentials value is true

__Syntax__:

```http
Access-Control-Allow-Credentials: true
```

### `Access-Control-Allow-Origin`

__Syntax__:

```http
 <!-- For requests without credentials -->
Access-Control-Allow-Origin: *

# Specifies an origin
Access-Control-Allow-Origin: <origin>
```

__Example__:

```http
Access-Control-Allow-Origin: abc.net
<!-- or  -->
Access-Control-Allow-Origin: *
```

### `Access-Control-Allow-Methods`

__Syntax__:

```http
Access-Control-Allow-Methods: <method>, <method>, …
Access-Control-Allow-Methods: *
```

__Example__:

```http
Access-Control-Allow-Methods: GET, POST, OPTIONS, PUT, PATCH, DELETE
```

### `Access-Control-Allow-Headers`

The Access-Control-Request-Headers used to indicate which HTTP headers can be used during the actual request.

__Syntax__:

```http
Access-Control-Allow-Headers: X-Custom-Header
```

__Example__:

```http
Access-Control-Allow-Headers: X-Requested-With, Content-Type
```

### `Access-Control-Expose-Headers`

For clients to be able to access other headers, the server must list them using the `Access-Control-Expose-Headers` header.

__Syntax__:

```http
Access-Control-Expose-Headers: [<header-name>[, <header-name>]*]
Access-Control-Expose-Headers: *
```

__Example__:

```http
Access-Control-Expose-Headers: Content-Encoding, Kuma-Revision
```
