# ulid-rs

[![Build Status](https://travis-ci.org/dylanhart/ulid-rs.svg?branch=master)](https://travis-ci.org/dylanhart/ulid-rs)
[![Crates.io](https://img.shields.io/crates/v/ulid.svg)](https://crates.io/crates/ulid)
[![docs.rs](https://docs.rs/ulid/badge.svg)](https://docs.rs/ulid)

This is a Rust implementation of the [ulid][ulid] project which provides
Universally Unique Lexicographically Sortable Identifiers.

## Quickstart

```rust
// Generate a ulid
let ulid = Ulid::new();

// Generate a string for a ulid
let s = ulid.to_string();

// Create from a String
let res = Ulid::from_string(&s);

assert_eq!(ulid, res.unwrap());
```

[ulid]: https://github.com/alizain/ulid

## Benchmark

Benchmarks were run on my laptop. Run them yourself with `cargo bench`.

```
test bench_from_string        ... bench:          41 ns/iter (+/- 16)
test bench_from_time          ... bench:          24 ns/iter (+/- 6)
test bench_generator_generate ... bench:          61 ns/iter (+/- 12)
test bench_new                ... bench:          73 ns/iter (+/- 17)
test bench_to_string          ... bench:          89 ns/iter (+/- 11)
```
