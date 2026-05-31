# pleme-kindbyte-derive

Paired string+byte round-trip over a unit-variant enum: the KindStr pair plus pub fn as_byte(&self) -> u8 + pub fn from_byte(u8) -> Option<Self>. Every variant must carry #[kind(byte = N)]; for wire formats like OSC52 clipboard selectors. Honors #[kind(name/alias/byte)].

[![Build](https://github.com/pleme-io/pleme-kindbyte-derive/actions/workflows/auto-release.yml/badge.svg)](#)
[![crates.io](https://img.shields.io/crates/v/pleme-kindbyte-derive.svg)](https://crates.io/crates/pleme-kindbyte-derive)

## Install

```toml
[dependencies]
pleme-kindbyte-derive = "*"
```

## Generation

This crate is mechanically emitted by [`tatara-rust-ast`](https://github.com/pleme-io/tatara-rust-ast). The author surface is a typed `(defmacro …)` Spec — the proc-macro implementation, tests, Nix flake, caixa wrapper, and CI workflow are all generated. See the catalog at `catalog.json` in the parent registry.
