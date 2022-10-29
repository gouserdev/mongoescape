# mongo_escape

[Escape MongoDB keys](http://docs.mongodb.org/manual/faq/developers/#faq-dollar-sign-escaping) for characters . , $ , & , + ,  * , ? , ] , [ , ) , ( , | , . , } and { .

## Example

```go
package main

import {
me "github.com/gouserdev/mongo_escape"
}
func main() {
    me.Escape("event.thing")
    // event\uFF0Ething
    me.Unescape("event\uFF0Ething")
    // event.thing

    me.Escape("event$thing")
    // event\uFF04thing
    me.Unescape("event\uFF04thing")
    // event$thing
}
```

### Thanks 

https://github.com/segment-boneyard/go-mongo-key-escape

## License

MIT
