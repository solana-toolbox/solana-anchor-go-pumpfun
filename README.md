# solana-anchor-go

Generate go bindings for Anchor IDLs.


## Usage

```bash
$ go build
$ ./solana-anchor-go -src=./example/dummy_idl.json -pkg=dummy -dst=./generated/dummy
```

Generated Code will be generated and saved to `./generated/`.
And check `./example/dummy_test.go` for generated code usage.

```

## TODO
- [x] instructions
- [x] accounts
- [x] types
- [x] events
- [x] errors
- [~] handle all possible seed inputs (`[32]u8`, const, `PublicKey` handled as single nested input fields)
- [ ] handle tuple types
- [ ] constants (?)
