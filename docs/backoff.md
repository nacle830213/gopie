

# backoff
`import "github.com/andy2046/gopie/pkg/backoff"`

* [Overview](#pkg-overview)
* [Index](#pkg-index)

## <a name="pkg-overview">Overview</a>
Package backoff implements Backoff pattern.
<a href="http://www.awsarchitectureblog.com/2015/03/backoff.html">http://www.awsarchitectureblog.com/2015/03/backoff.html</a>




## <a name="pkg-index">Index</a>
* [type Backoff](#Backoff)
  * [func New(baseDelay, capDelay time.Duration, strategy Strategy) *Backoff](#New)
  * [func (bk *Backoff) Backoff(retries int) time.Duration](#Backoff.Backoff)
* [type Strategy](#Strategy)


#### <a name="pkg-files">Package files</a>
[backoff.go](/src/github.com/andy2046/gopie/pkg/backoff/backoff.go) 






## <a name="Backoff">type</a> [Backoff](/src/target/backoff.go?s=292:332#L18)
``` go
type Backoff struct {
    // contains filtered or unexported fields
}
```
Backoff holds the backoff logic.







### <a name="New">func</a> [New](/src/target/backoff.go?s=1474:1545#L75)
``` go
func New(baseDelay, capDelay time.Duration, strategy Strategy) *Backoff
```
New returns a Backoff instance with provided delay and strategy.





### <a name="Backoff.Backoff">func</a> (\*Backoff) [Backoff](/src/target/backoff.go?s=2114:2167#L104)
``` go
func (bk *Backoff) Backoff(retries int) time.Duration
```
Backoff returns the amount of time to wait before the next retry.
`retries` starts from zero.




## <a name="Strategy">type</a> [Strategy](/src/target/backoff.go?s=237:252#L15)
``` go
type Strategy string
```
Strategy type.


``` go
const (
    Exponential        Strategy = "Exponential"
    FullJitter         Strategy = "FullJitter"
    EqualJitter        Strategy = "EqualJitter"
    DecorrelatedJitter Strategy = "DecorrelatedJitter"
)
```
predefined Strategy types.














- - -
Generated by [godoc2md](http://godoc.org/github.com/davecheney/godoc2md)
