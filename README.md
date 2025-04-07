# solana-anchor-go

Generate go bindings for Anchor IDLs.


## Usage

```bash
$ go install github.com/daog1/solana-anchor-go@latest
$ solana-anchor-go -src=./example/dummy_idl.json -pkg=dummy -dst=./generated/dummy
```
or

```bash
$ go build
$ ./solana-anchor-go -src=./example/dummy_idl.json -pkg=dummy -dst=./generated/dummy
```

Generated Code will be generated and saved to `./generated/`.
And check `./example/dummy_test.go` for generated code usage.



## TODO
- [x] instructions
- [x] accounts
- [x] types
- [x] events
- [x] errors
- [ ] handle all possible seed inputs (`[32]u8`, const, `PublicKey` handled as single nested input fields)
- [ ] handle tuple types
- [ ] constants (?)

## 小发现
发现部分老的idl文件需要先进行转换，再使用

不然会出现：
```
panic(`not implemented - only IDL from ("anchor": ">=0.30.0") is available`)
```
这样转换：
```
anchor idl convert  6EF8rrecthR5Dkzon8Nwu78hRvfCKubJ14M5uBEwF6P_266791762.json >pump.json
```

## 使用方法

参考 https://github.com/daog1/pumpgo
