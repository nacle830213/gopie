

# drf
`import "github.com/andy2046/gopie/pkg/drf"`

* [Overview](#pkg-overview)
* [Index](#pkg-index)

## <a name="pkg-overview">Overview</a>
Package drf implements Dominant Resource Fairness.




## <a name="pkg-index">Index</a>
* [Constants](#pkg-constants)
* [Variables](#pkg-variables)
* [type DRF](#DRF)
  * [func New(clusterResource map[Typ]float64, clusterNodes ...*Node) (DRF, error)](#New)
  * [func (drf DRF) AddNode(n *Node)](#DRF.AddNode)
  * [func (drf DRF) Consumed() map[Typ]float64](#DRF.Consumed)
  * [func (drf DRF) NextTask() error](#DRF.NextTask)
  * [func (drf DRF) RemoveNode(n *Node)](#DRF.RemoveNode)
  * [func (drf DRF) Resource() map[Typ]float64](#DRF.Resource)
  * [func (drf DRF) UpdateResource(delta map[Typ]float64)](#DRF.UpdateResource)
* [type Node](#Node)
  * [func NewNode(demand ...map[Typ]float64) *Node](#NewNode)
  * [func (n *Node) Allocated() map[Typ]float64](#Node.Allocated)
  * [func (n *Node) UpdateDemand(delta map[Typ]float64)](#Node.UpdateDemand)
* [type Typ](#Typ)


#### <a name="pkg-files">Package files</a>
[drf.go](/src/github.com/andy2046/gopie/pkg/drf/drf.go) [types.go](/src/github.com/andy2046/gopie/pkg/drf/types.go) 


## <a name="pkg-constants">Constants</a>
``` go
const (
    // CPU resource.
    CPU = Typ("CPU")

    // MEMORY resource.
    MEMORY = Typ("MEMORY")
)
```

## <a name="pkg-variables">Variables</a>
``` go
var (
    // ErrResourceSaturated when there is not enough resource to run next task.
    ErrResourceSaturated = fmt.Errorf("Fatal: resource has been saturated")

    // ErrEmptyResource when cluster resource is empty.
    ErrEmptyResource = fmt.Errorf("Fatal: empty cluster resource")

    // ErrEmptyNodes when cluster nodes is empty.
    ErrEmptyNodes = fmt.Errorf("Fatal: empty cluster nodes")

    // EmptyDRF is empty DRF.
    EmptyDRF = DRF{}
)
```



## <a name="DRF">type</a> [DRF](/src/target/types.go?s=416:563#L26)
``` go
type DRF struct {
    // contains filtered or unexported fields
}
```
DRF represents a DRF Cluster.







### <a name="New">func</a> [New](/src/target/drf.go?s=134:211#L10)
``` go
func New(clusterResource map[Typ]float64, clusterNodes ...*Node) (DRF, error)
```
New create a DRF Cluster.





### <a name="DRF.AddNode">func</a> (DRF) [AddNode](/src/target/drf.go?s=2067:2098#L98)
``` go
func (drf DRF) AddNode(n *Node)
```
AddNode add new Node to DRF Cluster.




### <a name="DRF.Consumed">func</a> (DRF) [Consumed](/src/target/drf.go?s=2995:3036#L139)
``` go
func (drf DRF) Consumed() map[Typ]float64
```
Consumed return all the consumed resource by cluster.




### <a name="DRF.NextTask">func</a> (DRF) [NextTask](/src/target/drf.go?s=1418:1449#L69)
``` go
func (drf DRF) NextTask() error
```
NextTask run next task with lowest dominant share.




### <a name="DRF.RemoveNode">func</a> (DRF) [RemoveNode](/src/target/drf.go?s=2390:2424#L113)
``` go
func (drf DRF) RemoveNode(n *Node)
```
RemoveNode remove Node from DRF Cluster.




### <a name="DRF.Resource">func</a> (DRF) [Resource](/src/target/drf.go?s=3271:3312#L150)
``` go
func (drf DRF) Resource() map[Typ]float64
```
Resource return all the cluster resource.




### <a name="DRF.UpdateResource">func</a> (DRF) [UpdateResource](/src/target/drf.go?s=1847:1899#L89)
``` go
func (drf DRF) UpdateResource(delta map[Typ]float64)
```
UpdateResource add delta to Cluster Resource.




## <a name="Node">type</a> [Node](/src/target/types.go?s=149:300#L14)
``` go
type Node struct {
    // contains filtered or unexported fields
}
```
Node represents a Cluster Node.







### <a name="NewNode">func</a> [NewNode](/src/target/drf.go?s=945:990#L46)
``` go
func NewNode(demand ...map[Typ]float64) *Node
```
NewNode create a Cluster Node.





### <a name="Node.Allocated">func</a> (\*Node) [Allocated](/src/target/drf.go?s=2732:2774#L128)
``` go
func (n *Node) Allocated() map[Typ]float64
```
Allocated return all the allocated resource for node.




### <a name="Node.UpdateDemand">func</a> (\*Node) [UpdateDemand](/src/target/drf.go?s=1212:1262#L60)
``` go
func (n *Node) UpdateDemand(delta map[Typ]float64)
```
UpdateDemand add delta to existing demand.




## <a name="Typ">type</a> [Typ](/src/target/types.go?s=100:110#L11)
``` go
type Typ string
```
Typ represents resource type.














- - -
Generated by [godoc2md](http://godoc.org/github.com/davecheney/godoc2md)