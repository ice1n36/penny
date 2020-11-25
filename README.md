# Penny

Penny is the main interface both for gadgets and users. 

## Install

```
go get github.com/ice1n36/penny
```

## Build & Run

### Locally

update dependencies
```
./update-deps.sh
```

build and run

```
bazel run :penny
```

### Docker
```
bazel run --platforms=@io_bazel_rules_go//go/toolchain:linux_amd64 :penny_container_image
docker run --rm -it -p80:80 bazel:penny_container_image
```

## Publish

### Docker

```
bazel run --platforms=@io_bazel_rules_go//go/toolchain:linux_amd64 :penny_container_image_push
```

## Test

### Unit
TODO

### Locally
```
curl -X GET localhost/hello
```

# LICENSE

[![MIT License](http://img.shields.io/badge/license-MIT-blue.svg)](http://www.opensource.org/licenses/MIT)

This is distributed under the [MIT License](http://www.opensource.org/licenses/MIT).
