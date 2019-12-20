

# bitflag
`import "github.com/andy2046/gopie/pkg/bitflag"`

* [Overview](#pkg-overview)
* [Index](#pkg-index)

## <a name="pkg-overview">Overview</a>
Package bitflag implements bit flag.




## <a name="pkg-index">Index</a>
* [type Flag](#Flag)
  * [func (f Flag) AreAllSet(opts ...Flag) bool](#Flag.AreAllSet)
  * [func (f *Flag) Clear(n uint8)](#Flag.Clear)
  * [func (f *Flag) ClearAll(opts ...Flag)](#Flag.ClearAll)
  * [func (f Flag) IsAnySet(opts ...Flag) bool](#Flag.IsAnySet)
  * [func (f Flag) IsSet(n uint8) bool](#Flag.IsSet)
  * [func (f *Flag) Reset()](#Flag.Reset)
  * [func (f *Flag) Set(n uint8)](#Flag.Set)
  * [func (f *Flag) SetAll(opts ...Flag)](#Flag.SetAll)
  * [func (f *Flag) Toggle(n uint8)](#Flag.Toggle)
  * [func (f *Flag) ToggleAll(opts ...Flag)](#Flag.ToggleAll)


#### <a name="pkg-files">Package files</a>
[bitflag.go](/src/github.com/andy2046/gopie/pkg/bitflag/bitflag.go) 






## <a name="Flag">type</a> [Flag](/src/target/bitflag.go?s=84:98#L5)
``` go
type Flag byte
```
Flag is an 8 bits flag.










### <a name="Flag.AreAllSet">func</a> (Flag) [AreAllSet](/src/target/bitflag.go?s=515:557#L31)
``` go
func (f Flag) AreAllSet(opts ...Flag) bool
```
AreAllSet check if all the flags are set.




### <a name="Flag.Clear">func</a> (\*Flag) [Clear](/src/target/bitflag.go?s=1342:1371#L79)
``` go
func (f *Flag) Clear(n uint8)
```
Clear clear a single bit at `n`.
`n` should be less than `8`.




### <a name="Flag.ClearAll">func</a> (\*Flag) [ClearAll](/src/target/bitflag.go?s=387:424#L24)
``` go
func (f *Flag) ClearAll(opts ...Flag)
```
ClearAll clear all the flags.




### <a name="Flag.IsAnySet">func</a> (Flag) [IsAnySet](/src/target/bitflag.go?s=683:724#L41)
``` go
func (f Flag) IsAnySet(opts ...Flag) bool
```
IsAnySet check if any one flag is set.




### <a name="Flag.IsSet">func</a> (Flag) [IsSet](/src/target/bitflag.go?s=880:913#L52)
``` go
func (f Flag) IsSet(n uint8) bool
```
IsSet check if the bit at `n` is set.
`n` should be less than `8`.




### <a name="Flag.Reset">func</a> (\*Flag) [Reset](/src/target/bitflag.go?s=1445:1467#L87)
``` go
func (f *Flag) Reset()
```
Reset reset the flag.




### <a name="Flag.Set">func</a> (\*Flag) [Set](/src/target/bitflag.go?s=1045:1072#L61)
``` go
func (f *Flag) Set(n uint8)
```
Set set a single bit at `n`.
`n` should be less than `8`.




### <a name="Flag.SetAll">func</a> (\*Flag) [SetAll](/src/target/bitflag.go?s=150:185#L10)
``` go
func (f *Flag) SetAll(opts ...Flag)
```
SetAll set all the flags.




### <a name="Flag.Toggle">func</a> (\*Flag) [Toggle](/src/target/bitflag.go?s=1196:1226#L70)
``` go
func (f *Flag) Toggle(n uint8)
```
Toggle toggle (XOR) a single bit at `n`.
`n` should be less than `8`.




### <a name="Flag.ToggleAll">func</a> (\*Flag) [ToggleAll](/src/target/bitflag.go?s=271:309#L17)
``` go
func (f *Flag) ToggleAll(opts ...Flag)
```
ToggleAll toggle (XOR) all the flags.








- - -
Generated by [godoc2md](http://godoc.org/github.com/davecheney/godoc2md)