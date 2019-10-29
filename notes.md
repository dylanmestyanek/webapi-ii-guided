# Routing Notes

[ client ] == makes a request to an == [ api ] == sends a response back to the == [ client ]

What is the interface for a web api? 

- URI (Uniform Resource Identifier)
- URL (Universal Resource Locator)
- Endpoint (very related to a URI)
- HTTP === Network Protocol, a set of rules for communication

REST(ish)

- Everything is a `Resource`
- single URI per resource - Example: `http://web23.com/channels`, `http://web23.com/users`
- Use HTTP methods to perform operations on resources.
- Hypermedia (at this level we are fully REST)

| Non REST           | REST              |
|:-------------------|:------------------|
|/listAllChannels    | GET /channels     |
|/createChannel      | POST /chanells    |
|/updateChannel      | PUT /channels     |
|/deleteChannel      | DELETE /channels  |
|/findChannel?id=123 | GET /channels/123 |

What is an Express Router? Why is it useful?

An Express Router can have route/request handlers and middleware

## Query Strings

https://www.google.com/search?q=expressjs&rlz=1C1CHBF_enUS859US859&oq=expressjs&aqs=chrome..69i57j0l5.1224j0j4&sourceid=chrome&ie=UTF-8

https://www.google.com - `DOMAIN`

/search - `PATH`

? - `QUERY`

q=expressjs - `KEY VALUE PAIR`

&

rlz=1C1CHBF_enUS859US859 - `KEY VALUE PAIR`

&

oq=expressjs - `KEY VALUE PAIR`

&

aqs=chrome..69i57j0l5.1224j0j4 - `KEY VALUE PAIR`

&

sourceid=chrome - `KEY VALUE PAIR`

&

ie=UTF-8 - `KEY VALUE PAIR`

```js
req.query = {
    q: 'expressjs',
    rlz: '1C1CHBF_enUS859US859',
    oq: 'expressjs',
    aqs: 'chrome..69i57j0l5.1224j0j4',
    sourceid: 'chrome',
    ie: 'UTF-8'
}
```