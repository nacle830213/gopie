

# tlv
`import "github.com/andy2046/gopie/pkg/tlv"`

* [Overview](#pkg-overview)
* [Index](#pkg-index)

## <a name="pkg-overview">Overview</a>
Package tlv implements Type-Length-Value encoding.




## <a name="pkg-index">Index</a>
* [type ByteSize](#ByteSize)
* [type Codec](#Codec)
* [type Reader](#Reader)
  * [func NewReader(reader io.Reader, codec *Codec) *Reader](#NewReader)
  * [func (r *Reader) Next() (*Record, error)](#Reader.Next)
* [type Record](#Record)
* [type Writer](#Writer)
  * [func NewWriter(w io.Writer, codec *Codec) *Writer](#NewWriter)
  * [func (w *Writer) Write(rec *Record) error](#Writer.Write)


#### <a name="pkg-files">Package files</a>
[tlv.go](/src/github.com/andy2046/gopie/pkg/tlv/tlv.go) 






## <a name="ByteSize">type</a> [ByteSize](/src/target/tlv.go?s=321:333#L21)
``` go
type ByteSize int
```
ByteSize is the size of a field in bytes.
Used to define the size of the type and length field in a message.


``` go
const (
    Bytes1 ByteSize = 1 << iota
    Bytes2
    Bytes4
    Bytes8
)
```
ByteSize const.










## <a name="Codec">type</a> [Codec](/src/target/tlv.go?s=521:717#L30)
``` go
type Codec struct {
    // TypeBytes defines the size in bytes of the message type field.
    TypeBytes ByteSize

    // LenBytes defines the size in bytes of the message length field.
    LenBytes ByteSize
}
```
Codec is the configuration for a TLV encoding/decoding task.










## <a name="Reader">type</a> [Reader](/src/target/tlv.go?s=959:1012#L45)
``` go
type Reader struct {
    // contains filtered or unexported fields
}
```
Reader decodes records from TLV format using a Codec from the provided io.Reader.







### <a name="NewReader">func</a> [NewReader](/src/target/tlv.go?s=1863:1917#L92)
``` go
func NewReader(reader io.Reader, codec *Codec) *Reader
```
NewReader creates a new Reader.





### <a name="Reader.Next">func</a> (\*Reader) [Next](/src/target/tlv.go?s=2019:2059#L97)
``` go
func (r *Reader) Next() (*Record, error)
```
Next reads a single Record from the io.Reader.




## <a name="Record">type</a> [Record](/src/target/tlv.go?s=403:453#L24)
``` go
type Record struct {
    Payload []byte
    Type    uint
}
```
Record represents a record of data encoded in the TLV message.










## <a name="Writer">type</a> [Writer](/src/target/tlv.go?s=817:870#L39)
``` go
type Writer struct {
    // contains filtered or unexported fields
}
```
Writer encodes records into TLV format using a Codec and writes into the provided io.Writer.







### <a name="NewWriter">func</a> [NewWriter](/src/target/tlv.go?s=1051:1100#L52)
``` go
func NewWriter(w io.Writer, codec *Codec) *Writer
```
NewWriter creates a new Writer.





### <a name="Writer.Write">func</a> (\*Writer) [Write](/src/target/tlv.go?s=1251:1292#L60)
``` go
func (w *Writer) Write(rec *Record) error
```
Write encodes records into TLV format using a Codec and writes into the provided io.Writer.








- - -
Generated by [godoc2md](http://godoc.org/github.com/davecheney/godoc2md)