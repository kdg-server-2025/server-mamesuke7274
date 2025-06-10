# ベースイメージに軽量なgolang:alpineを使う

FROM golang:alpine

# 作業するディレクトリの移動
WORKDIR /

# Goのソースコードをコピー
COPY main.go go.mod 

# バイナリをビルド（go build は main.go をビルドして ./main を作る）
RUN go build -o main

# デフォルトコマンドでバイナリを実行
CMD ["/main"]

FROM scratch

