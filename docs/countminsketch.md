

# countminsketch
`import "github.com/andy2046/gopie/pkg/countminsketch"`

* [Overview](#pkg-overview)
* [Index](#pkg-index)

## <a name="pkg-overview">Overview</a>
Package countminsketch implements Count-Min Sketch.




## <a name="pkg-index">Index</a>
* [type CountMinSketch](#CountMinSketch)
  * [func New(width, depth uint) (*CountMinSketch, error)](#New)
  * [func NewGuess(epsilon, delta float64) (*CountMinSketch, error)](#NewGuess)
  * [func (c *CountMinSketch) Add(data []byte, count ...uint64)](#CountMinSketch.Add)
  * [func (c *CountMinSketch) AddString(data string, count ...uint64)](#CountMinSketch.AddString)
  * [func (c *CountMinSketch) Count() uint64](#CountMinSketch.Count)
  * [func (c *CountMinSketch) Depth() uint](#CountMinSketch.Depth)
  * [func (c *CountMinSketch) Estimate(data []byte) uint64](#CountMinSketch.Estimate)
  * [func (c *CountMinSketch) EstimateString(data string) uint64](#CountMinSketch.EstimateString)
  * [func (c *CountMinSketch) Merge(other *CountMinSketch) error](#CountMinSketch.Merge)
  * [func (c *CountMinSketch) Reset()](#CountMinSketch.Reset)
  * [func (c *CountMinSketch) Width() uint](#CountMinSketch.Width)


#### <a name="pkg-files">Package files</a>
[countmin.go](/src/github.com/andy2046/gopie/pkg/countminsketch/countmin.go) 






## <a name="CountMinSketch">type</a> [CountMinSketch](/src/target/countmin.go?s=174:400#L13)
``` go
type CountMinSketch struct {
    // contains filtered or unexported fields
}
```
CountMinSketch struct.







### <a name="New">func</a> [New](/src/target/countmin.go?s=613:665#L25)
``` go
func New(width, depth uint) (*CountMinSketch, error)
```
New returns new Count-Min Sketch with the given `width` and `depth`.


### <a name="NewGuess">func</a> [NewGuess](/src/target/countmin.go?s=1080:1142#L44)
``` go
func NewGuess(epsilon, delta float64) (*CountMinSketch, error)
```
NewGuess returns new Count-Min Sketch with the given error rate `epsilon` and confidence `delta`.





### <a name="CountMinSketch.Add">func</a> (\*CountMinSketch) [Add](/src/target/countmin.go?s=1645:1703#L64)
``` go
func (c *CountMinSketch) Add(data []byte, count ...uint64)
```
Add add the `data` to the sketch. `count` default to 1.




### <a name="CountMinSketch.AddString">func</a> (\*CountMinSketch) [AddString](/src/target/countmin.go?s=1995:2059#L80)
``` go
func (c *CountMinSketch) AddString(data string, count ...uint64)
```
AddString add the `data` string to the sketch. `count` default to 1.




### <a name="CountMinSketch.Count">func</a> (\*CountMinSketch) [Count](/src/target/countmin.go?s=1525:1564#L59)
``` go
func (c *CountMinSketch) Count() uint64
```
Count returns the number of items added to the sketch.




### <a name="CountMinSketch.Depth">func</a> (\*CountMinSketch) [Depth](/src/target/countmin.go?s=3309:3346#L138)
``` go
func (c *CountMinSketch) Depth() uint
```
Depth returns the matrix depth.




### <a name="CountMinSketch.Estimate">func</a> (\*CountMinSketch) [Estimate](/src/target/countmin.go?s=2146:2199#L85)
``` go
func (c *CountMinSketch) Estimate(data []byte) uint64
```
Estimate estimate the frequency of the `data`.




### <a name="CountMinSketch.EstimateString">func</a> (\*CountMinSketch) [EstimateString](/src/target/countmin.go?s=2511:2570#L102)
``` go
func (c *CountMinSketch) EstimateString(data string) uint64
```
EstimateString estimate the frequency of the `data` string.




### <a name="CountMinSketch.Merge">func</a> (\*CountMinSketch) [Merge](/src/target/countmin.go?s=2888:2947#L118)
``` go
func (c *CountMinSketch) Merge(other *CountMinSketch) error
```
Merge combines the sketch with another.




### <a name="CountMinSketch.Reset">func</a> (\*CountMinSketch) [Reset](/src/target/countmin.go?s=2658:2690#L107)
``` go
func (c *CountMinSketch) Reset()
```
Reset reset the sketch to its original state.




### <a name="CountMinSketch.Width">func</a> (\*CountMinSketch) [Width](/src/target/countmin.go?s=3403:3440#L143)
``` go
func (c *CountMinSketch) Width() uint
```
Width returns the matrix width.








- - -
Generated by [godoc2md](http://godoc.org/github.com/davecheney/godoc2md)
