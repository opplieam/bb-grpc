# Buy-Better Proto

## Overview
Buy-Better Proto is a centralized proto repository. It's auto generate stub files by GitHub action using `protoc` 
when merge a pull request or push to master. Also, it's auto increment a tag version.

## Project structure
```
├── Makefile
├── README.md
├── go.mod
├── go.sum
├── proto               # define proto file in this directory
│   └── product
│       └── product.proto
└── protogen            # auto generate by Github actions
    └── go
        └── product
            ├── product.pb.go
            └── product_grpc.pb.go
```

## Steps

1. Define proto service
2. Create pull request to validate schema
3. Merge pull request. GitHub actions will auto generate stubs files and increment a version tag

The consumer can now run `go get github.com/opplieam/bb-grpc/protogen/go/product`

Please visit `.github/workflows` for more information