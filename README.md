# Penny

Penny is the main interface both for gadgets and users.

## Install

### Go
```
go get github.com/ice1n36/penny
```

See below on how to build and run

### Docker
```
docker pull ice1n36/penny:latest
```

## Run
```
docker run --rm -it -d -p80:80 ice1n36/penny
```

### Docker Compose
In this directory:
```
docker-compose up -d
```

and to teardown:
```
docker-compose down
```

## Development
### Build & Run

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
docker run --rm -it -d -p80:80 bazel:penny_container_image
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
