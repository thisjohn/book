# fetch is the new xhr, fetch-er is the new $.ajax
by othree

## *fetch*, [@github](https://github.com/whatwg/fetch)

- Promise based
- JSON support
- Simple naming, options object
- Designed as low level API

## mode

- no-cors
    - Do not check CORS
    - Get **opaque** response, 無法拿到 raw data
    - For ServiceWorker
    - XHR cannot do this

## Response

- ok is true while return status code 2xx
- Fetch promise will resolve event when server respond 404, 500
- Request is complete so Promise is resolved
- Reject on exception, ex network timeout

## Request

- body cannot be reused
- request cannot be reused

## Polyfill, [@github](https://github.com/github/fetch)

## Fact

- Debug
    - Chrome: at 'other tab', request body not shown
    - Firefox: depend on response type
- Safety flag for CORS not affect fetch
    - Affect Electron app: use XHR + polyfill instead
- Not able to cancel a fetch
    - No solution now
- Not support progress now
- fetch-with-streams
- Future spec

## Current Status

- Lots of new stuff is on the way
    - Streams, cancel
    - Browser integration
    - Cache, HTTP/2, CSP, subresource integrity, GET with body, busy indicator

## Ref

- [fetch-er](https://github.com/othree/fetcher)
- webpack + [babeljs](https://babeljs.io/)

## sendBeacon

- POST data to analytic service
- Do not care response

