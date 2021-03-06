[![Build Status](https://travis-ci.org/codeb2cc/gomemcache.png)](https://travis-ci.org/codeb2cc/gomemcache)
[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/codeb2cc/gomemcache/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

## About

This is a memcache client library for the Go programming language
(http://golang.org/).

## Installing

### Using *go get*

    $ go get github.com/codeb2cc/gomemcache/memcache

After this command *gomemcache* is ready to use. Its source will be in:

    $GOPATH/src/pkg/github.com/codeb2cc/gomemcache/memcache

You can use `go get -u -a` for update all installed packages.

### Using *git clone* command:

    $ git clone git://github.com/codeb2cc/gomemcache
    $ cd gomemcache/memcache
    $ make install

## Example

    import (
            "github.com/codeb2cc/gomemcache/memcache"
    )

    func main() {
         mc := memcache.New("10.0.0.1:11211", "10.0.0.2:11211", "10.0.0.3:11212")
         mc.Set(&memcache.Item{Key: "foo", Value: []byte("my value")})

         it, err := mc.Get("foo")
         ...
    }

## Full docs, see:

    $ godoc github.com/codeb2cc/gomemcache/memcache

