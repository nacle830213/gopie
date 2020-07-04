

# latest
`import "github.com/andy2046/gopie/pkg/latest"`

* [Overview](#pkg-overview)
* [Index](#pkg-index)
* [Examples](#pkg-examples)

## <a name="pkg-overview">Overview</a>
Package latest provides latest value.




## <a name="pkg-index">Index</a>
* [func New(receiver chan&lt;- interface{}) chan&lt;- interface{}](#New)
* [func NewN(receiver chan&lt;- []interface{}, n int) chan&lt;- interface{}](#NewN)

#### <a name="pkg-examples">Examples</a>
* [New](#example_New)
* [NewN](#example_NewN)

#### <a name="pkg-files">Package files</a>
[latest.go](/src/github.com/andy2046/gopie/pkg/latest/latest.go) 





## <a name="New">func</a> [New](/src/target/latest.go?s=121:177#L5)
``` go
func New(receiver chan<- interface{}) chan<- interface{}
```
New send latest value from returned chan to `receiver` chan.



## <a name="NewN">func</a> [NewN](/src/target/latest.go?s=586:652#L34)
``` go
func NewN(receiver chan<- []interface{}, n int) chan<- interface{}
```
NewN send latest `n` values from returned chan to `receiver` chan.








- - -
Generated by [godoc2md](http://godoc.org/github.com/davecheney/godoc2md)