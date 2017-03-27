# ts-protoc-gen
> Protoc Plugin for TypeScript Declarations


[![Master Build](https://travis-ci.org/improbable-eng/ts-protoc-gen.svg?branch=master)](https://travis-ci.org/improbable-eng/ts-protoc-gen)
[![NPM](https://img.shields.io/npm/v/ts-protoc-gen.svg)](https://www.npmjs.com/package/ts-protoc-gen)
[![Apache 2.0 License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
![quality: alpha](https://img.shields.io/badge/quality-beta-orange.svg)

This repository contains a [protoc](https://github.com/google/protobuf) plugin that generates TypeScript declarations 
(`.d.ts` files) that match the JavaScript output of `protoc --js_out`.

## Usage
* Install this repository using `npm install ts-protoc-gen` or clone this repository and run `npm install && npm run build`
* Invoke `protoc` with the `bin` directory of this package and the `ts_out` argument:
    ```
    PATH=./node_modules/ts-protoc-gen/bin:$PATH protoc \
    --js_out=import_style=commonjs,binary:generated \
    --ts_out=generated \
    -I ./proto \
    proto/*.proto
    ```

## TODO
* Add tests for extensions
* Setup CI 