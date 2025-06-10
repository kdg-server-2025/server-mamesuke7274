# ベースイメージに軽量なgolang:alpineを使う

FROM golang:alpine AS builder

# 作業するディレクトリの移動
WORKDIR /

# Goのソースコードをコピー
COPY main.go go.mod ./

# バイナリをビルド（go build は main.go をビルドして ./main を作る）
RUN go build -o /main

FROM scratch

COPY --from=builder /main /

# デフォルトコマンドでバイナリを実行
CMD ["/main"]