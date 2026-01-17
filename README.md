# Introduction

demo is a Rust project that implements an AWS Lambda function in Rust.

## Prerequisites

- [Rust](https://www.rust-lang.org/tools/install)
- [Cargo Lambda](https://www.cargo-lambda.info/guide/installation.html)
- `serde_json`, use `cargo add serde_json` to add it to your `Cargo.toml`

## Building

Prod build (without arm64, by default x86_64): `cargo lambda build --release --arm64`.

Dev build: `cargo lambda build`.

## Testing

Unit tests: `cargo test`.

Integration tests: `cargo lambda watch`.

Invoke (example): `cargo lambda invoke --data-example apigw-request`.

Invoke (file): `cargo lambda invoke --data-file ./data.json`.

Invoke (HTTP): `curl http://localhost:9000`.

## Deploying

Set variable: `export AWS_PROFILE=your-profile`.

Echo variable: `echo $AWS_PROFILE`.

Build: `cargo lambda build`.

Deploy: `cargo lambda deploy`.

You can also upload the bootstrap.zip file to AWS Lambda manually.
