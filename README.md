# Write a REST API (JSON) in Golang

Must has the following endpoints:

## GET /foo/
    - Output: {"bars": [{"uuid": $uuid, "bar": $number}]}

## GET /foo/:uuid
    - Output Not found: {"msg": "bar not found"}
    - Output Success: {"bar": $number}

## DELETE /foo/:uuid
    - Output Not found: {"msg": "bar not found"}
    - Output Success: 

## POST /foo/
    - Input: {"bar": 1}
      - must validate bar is a number
    - Output Success: {"id": $uuid} 
      - autogenerate the uuid 

## GET /foo/sum
    - Output: {"sum": $sum_of_all_bar_numbers}

--- 
## Notes 

No need to persist to disk (store in memory). 

Data structure might look something like this:
```
type Foo struct {
  UUID string `json:"uuid"`
  Bar int `json:"bar"`
}
```

Keep it simple, don't overthink it.

Frameworks not required (standard library is 100% capable).

Proper HTTP status codes should be returned and correct content-type should be set. 

## Bonus points:

- Unit tests with > 80% coverage
- Live swagger docs when the program is running

---

## Resources:
- https://golang.org/
- https://en.wikipedia.org/wiki/List_of_HTTP_status_codes
- https://restfulapi.net/rest-api-design-tutorial-with-example/
- https://goplay.space/
- https://tour.golang.org/
- https://www.pluralsight.com/paths/go-core-language
- https://blog.questionable.services/article/testing-http-handlers-go/
 
