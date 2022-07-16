## Proto files

build protobuffers in client and service

```
"proto:install": "npm i git+https://github.com/YOUR_USERNAME/grpc-nest-proto.git",
"proto:auth": "protoc --plugin=node_modules/.bin/protoc-gen-ts_proto -I=./node_modules/grpc-nest-proto/proto --ts_proto_out=src/auth/ node_modules/grpc-nest-proto/proto/auth.proto --ts_proto_opt=nestJs=true --ts_proto_opt=fileSuffix=.pb",
"proto:order": "protoc --plugin=node_modules/.bin/protoc-gen-ts_proto -I=./node_modules/grpc-nest-proto/proto --ts_proto_out=src/order/ node_modules/grpc-nest-proto/proto/order.proto --ts_proto_opt=nestJs=true --ts_proto_opt=fileSuffix=.pb",
"proto:product": "protoc --plugin=node_modules/.bin/protoc-gen-ts_proto -I=./node_modules/grpc-nest-proto/proto --ts_proto_out=src/product/ node_modules/grpc-nest-proto/proto/product.proto --ts_proto_opt=nestJs=true --ts_proto_opt=fileSuffix=.pb",
"proto:all": "npm run proto:auth && npm run proto:order && npm run proto:product"
```
