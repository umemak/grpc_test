# grpc_test

Connectと通常のgRPCの相互接続を確認する

- Connectのコード参考
  - [Getting started | Connect](https://connect.build/docs/go/getting-started/)

- gRPCのコード参考
  - [作ってわかる！ はじめてのgRPC](https://zenn.dev/hsaki/books/golang-grpc-starting)


## 実行結果
- server_grpc
```sh
$ go run cmd/client_grpc/main.go 
start gRPC Client.
Hello, Jane!
$ go run cmd/client_connect/main.go 
2023/05/24 14:10:49 unavailable: net/http: HTTP/1.x transport connection broken: malformed HTTP response "\x00\x00\x06\x04\x00\x00\x00\x00\x00\x00\x05\x00\x00@\x00"
```

- server_connect
```sh
$ go run cmd/client_grpc/main.go 
start gRPC Client.
Hello, Jane!
$ go run cmd/client_connect/main.go 
2023/05/24 14:11:10 Hello, Jane!
```
