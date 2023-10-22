## Non-persistent and Persistent HTTP

| Aspect                       | Non-Persistent HTTP (HTTP/1.0)        | Persistent HTTP (HTTP/1.1 and HTTP/2) |
|------------------------------|---------------------------------------|-------------------------------------|
| Connection Management        | New connection for each request/response pair | Retains open connection for multiple request/response pairs |
| Performance                  | Less efficient, higher latency due to connection setup and teardown | More efficient, lower latency with reduced connection overhead |
| Resource Retrieval           | Resources fetched sequentially, new connection for each resource | Multiple resources fetched sequentially or concurrently over the same connection |
| Head-of-Line Blocking        | Prone to head-of-line blocking; delay in one resource can block subsequent resources | Reduced head-of-line blocking; resources can be fetched independently |
| Client/Server Interaction    | Server unaware of subsequent requests from the same client | Server can recognize and optimize handling of multiple client requests on the same connection |
| Usage                        | Less common in modern web browsing | Default and widely adopted in contemporary web communication |

This table summarizes the key differences between non-persistent HTTP and persistent HTTP, highlighting the advantages of persistent connections in terms of performance and efficiency.
