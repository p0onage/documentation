---
outputFileName: index.html
---

<!-- TODO: Combine with CC pages? -->

# Description Document

With the addition of Competing Consumers, which is another way of reading streams, the need arose to expose these different methods to consumers.

The introduction of the description document has some benefits:

-   Clients can rely on the keys (streams, streamSubscription) in the description document to remain unchanged across versions of Event Store and you can rely on it as a lookup for the particular method of reading a stream.
-   Allows the restructuring of URIs underneath without breaking clients. e.g., `/streams/newstream` -> `/streams/newstream/atom`.

## Fetching the description document

There are 3 ways in which Event Store returns the description document.

-   Attempting to read a stream with an unsupported media type.
-   Attempting to read a stream with no accept header.
-   Requesting the description document explicitly.

The client is able to request the description document by passing `application/vnd.eventstore.streamdesc+json` in the `accept` header, for example:

### [Request](#tab/tabid-1)

[!code-bash[http-api-get-dd-request](~/code-examples/http-api/get-dd.sh?range=1-1)]

### [Response](#tab/tabid-2)

[!code-http[http-api-get-dd-response](~/code-examples/http-api/get-dd.sh?range=3-)]

* * *

In the example above, the client requested the description document for the stream called `newstream` which has a set of links describing the supported methods and content types. The document also includes additional methods available such as the `streamSubscription`. If there are no subscriptions to the `newstream`, the `streamSubscription` key is absent.
