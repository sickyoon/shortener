# URL shortener

Fast URL shortener service written in Go

# API

Get shortened URL

```bash
curl -sX POST -H 'Content-Type: application/json' 'localhost:9000/shorten' -d '{"url":"https://sickyoon.com"}'

> HTTP 200
> '{"short":"http://localhost/abcdef"}'
```

Get original URL

```bash
curl -sX GET -H 'Content-Type: application/json' 'localhost:9000/original' -d '{"short":"http://localhost/abcdef"}'

> HTTP 200
> {"original":"https://sickyoon.com"}
```

## Features

* no revoke/update
* MRU

## Dependencies

* httprouter
* groupcache
* mgo

# License

MIT

